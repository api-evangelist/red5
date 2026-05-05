---
title: "How to Connect Your Drone or IP Camera Feeds to Red5"
url: "https://www.red5.net/blog/how-to-connect-drone-or-ip-camera-feeds-to-red5/"
date: "Tue, 28 Apr 2026 19:41:05 +0000"
author: "Paul Gregoire"
feed_url: "https://www.red5.net/feed/"
---
<div class="wp-block-greenshift-blocks-container gspb_container gspb_container-gsbp-2e55073 blog_parent" id="gspb_container-id-gsbp-2e55073">
<div class="wp-block-greenshift-blocks-container gspb_container gspb_container-gsbp-5d8fe22 blog_left" id="gspb_container-id-gsbp-5d8fe22">
<div class="wp-block-rank-math-toc-block" id="rank-math-toc"><h2>Table of Contents</h2><nav><ul><li><a href="#using-gstreamer-for-stream-processing">Using GStreamer for Stream Processing</a></li><li><a href="#discovering-your-stream-format">Discovering Your Stream Format</a></li><li><a href="#64db">Video-Only Streams</a></li><li><a href="#undefined-2">Audio-Only Streams</a></li><li><a href="#undefined-3">Combined Audio and Video Streams</a></li><li><a href="#alternative-red5-restream-api">Alternative: Red5 Restream API</a></li><li><a href="#16fe">Final Notes</a></li></ul></nav></div>
</div>



<div class="wp-block-greenshift-blocks-container gspb_container gspb_container-gsbp-13564b4 blog_right" id="gspb_container-id-gsbp-13564b4">
<p>Since it comes up so often during the course of my week, I want to share a few simple options with interested parties for publishing your streams to Red5. This covers all the <a href="https://www.red5.net/blog/drone-live-streaming/">drones</a> and <a href="https://www.red5.net/blog/ip-camera-live-streaming-rtsp-to-webrtc">IP cameras</a> that I’ve had exposure to over the years that do not already have a means to egress via <a href="https://www.red5.net/blog/what-is-rtmp-streaming-protocol/" rel="noreferrer noopener" target="_blank">RTMP</a>. While Flash Player is “dead,” <a href="https://www.red5.net/blog/what-is-rtmp-streaming-protocol/">RTMP as a protocol</a> certainly is not.</p>



<h2 class="wp-block-heading" id="using-gstreamer-for-stream-processing">Using GStreamer for Stream Processing</h2>



<p>First up is to download the <a href="https://gstreamer.freedesktop.org/" rel="noreferrer noopener" target="_blank">GStreamer</a> application, a powerful multimedia framework that can handle the conversion and streaming process. To learn more about it, read our previous blog on using <a href="https://www.red5.net/blog/gstreamer-for-low-latency-streaming/">GStreamer for low-latency streaming</a>.</p>



<h2 class="wp-block-heading" id="discovering-your-stream-format">Discovering Your Stream Format</h2>



<p>If you don’t know the format of the video and/or audio (if present) on your drone, the <code>discoverer</code> application can be used to see what you&#8217;re working with:</p>


<div class="wp-block-syntaxhighlighter-code "><pre class="brush: bash; title: ; notranslate">
gst-discoverer-1.0 rtsp://10.0.0.10:554/stream
</pre></div>


<p>Replace 10.0.0.10:554 in the RTSP stream URL with your drone or camera IP address and port.</p>



<h2 class="wp-block-heading" id="64db">Video-Only Streams</h2>



<p id="25ea">When the source only provides video, this is the <code>pipeline</code> you&#8217;d use (assuming <a href="https://www.red5.net/h264/">H.264</a>):</p>


<div class="wp-block-syntaxhighlighter-code "><pre class="brush: bash; title: ; notranslate">
gst-launch-1.0 rtspsrc location=&quot;rtsp://10.0.0.10:554/stream&quot; latency=0 name=rtsp ! rtph264depay ! h264parse ! video/x-h264 ! queue ! flvmux name=mux ! rtmpsink location=&quot;rtmp://10.0.0.35:1935/live/drone1 live=1&quot;
</pre></div>


<h2 class="wp-block-heading" id="undefined-2">Audio-Only Streams</h2>



<p id="undefined-2">If the source is just audio, use this pipeline assuming an AAC <a href="https://www.red5.net/blog/what-is-a-codec/">codec</a>:</p>


<div class="wp-block-syntaxhighlighter-code "><pre class="brush: bash; title: ; notranslate">
gst-launch-1.0 rtspsrc location=&quot;rtsp://10.0.0.221:554/stream&quot; latency=0 name=rtsp ! rtpmp4gdepay ! aacparse ! audio/mpeg ! queue ! flvmux name=mux ! rtmpsink location=&quot;rtmp://10.0.0.35:1935/live/remotemic1 live=1&quot;
</pre></div>


<h2 class="wp-block-heading" id="undefined-3">Combined Audio and Video Streams</h2>



<p id="3e12">Finally, for sources providing both audio and video:</p>


<div class="wp-block-syntaxhighlighter-code "><pre class="brush: bash; title: ; notranslate">
gst-launch-1.0 -v rtspsrc location=&quot;rtsp://10.0.0.10:554/stream&quot; latency=0 name=rtsp rtsp. ! rtph264depay ! h264parse ! video/x-h264 ! queue ! mux.video rtsp. ! rtpmp4gdepay ! aacparse ! audio/mpeg ! queue ! mux.audio flvmux name=mux ! rtmpsink location=&quot;rtmp://10.0.0.35:1935/live/audvid1 live=1&quot;
</pre></div>


<h2 class="wp-block-heading" id="alternative-red5-restream-api">Alternative: Red5 Restream API</h2>



<p id="666d">This example demonstrates the simplest means to get your source devices providing egress via <a href="https://www.red5.net/blog/4-reasons-rtsp-streaming-is-still-relevant/">RTSP</a> into Red5 without <a href="https://www.red5.net/blog/what-is-rtmp-streaming-protocol/">RTMP</a>, using the <a href="https://www.red5.net/docs/red5-pro/development/api/restreamer/" rel="noreferrer noopener" target="_blank">Red5 Restream API</a> via curl:</p>


<div class="wp-block-syntaxhighlighter-code "><pre class="brush: bash; title: ; notranslate">
curl -X POST http://10.0.0.35:5080/live/restream \
  -H &quot;Content-Type: application/json&quot; \
  -d &#039;{
    &quot;guid&quot;:&quot;live/audvid1&quot;,
    &quot;context&quot;:&quot;live&quot;,
    &quot;name&quot;:&quot;audvid1&quot;,
    &quot;level&quot;:0,
    &quot;parameters&quot;:{
      &quot;type&quot;:&quot;ipcam&quot;,
      &quot;action&quot;:&quot;create&quot;,
      &quot;remoteContextPath&quot;:&quot;stream&quot;,
      &quot;remoteStreamName&quot;:&quot;&quot;,
      &quot;host&quot;:&quot;10.0.0.10&quot;,
      &quot;port&quot;:554
    }
  }&#039;

</pre></div>


<p id="833a"><em>Note: Postman may also be used for this API call, but that’s not covered here.</em></p>



<h2 class="wp-block-heading" id="16fe">Final Notes</h2>



<p id="dacb">These examples use a non-routable network, and you can change the fields to fit your devices and environment. For more detailed information and advanced configurations, see <a href="https://www.red5.net/docs/" rel="noreferrer noopener" target="_blank">our documentation</a>. Whether you’re working with consumer drones, professional camera equipment, or IP security cameras, these methods should help you get your RTSP streams flowing into Red5 for further distribution and processing.<a href="https://medium.com/write?source=promotion_paragraph---post_body_banner_jsw_blocks--0f3ff64c369d---------------------------------------" rel="noopener" target="_blank"></a></p>
</div>
</div>
<p>The post <a href="https://www.red5.net/blog/how-to-connect-drone-or-ip-camera-feeds-to-red5/" rel="nofollow">How to Connect Your Drone or IP Camera Feeds to Red5</a> appeared first on <a href="https://www.red5.net" rel="nofollow">Red5</a>.</p>
