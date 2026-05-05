---
title: "What’s New In Red5 Pro v15.4.0? MOQ Protocol Support, DASH Support in the Video Packager, Autoscaling Controls & APIs, And More!"
url: "https://www.red5.net/blog/whats-new-in-red5-pro-v15-4-0/"
date: "Thu, 23 Apr 2026 15:19:02 +0000"
author: "Maria Artamonova"
feed_url: "https://www.red5.net/feed/"
---
<div class="wp-block-greenshift-blocks-container gspb_container gspb_container-gsbp-2e55073 blog_parent" id="gspb_container-id-gsbp-2e55073">
<div class="wp-block-greenshift-blocks-container gspb_container gspb_container-gsbp-5d8fe22 blog_left" id="gspb_container-id-gsbp-5d8fe22">
<div class="wp-block-rank-math-toc-block" id="rank-math-toc"><h2>Table of Contents</h2><nav><ul><li><a href="#what-s-new-in-red5-pro-v15-4-0">What’s New in Red5 Pro v15.4.0?</a><ul><li><a href="#undefined-1">New Features</a></li><li><a href="#undefined-2">Improvements</a></li><li><a href="#undefined-3">Bug Fixes</a></li></ul></li><li><a href="#undefined-4">Conclusion</a></li></ul></nav></div>
</div>



<div class="wp-block-greenshift-blocks-container gspb_container gspb_container-gsbp-13564b4 blog_right" id="gspb_container-id-gsbp-13564b4">
<p>Let’s take a look at the latest Red5 Pro release since our previous blogs about <a href="https://www.red5.net/blog/what-is-new-in-red5-cloud-v1-13-0-and-pro-v15-3-0/">Red5 Pro v15.3.0</a>. Red5 Pro v15.4.0 introduces powerful new features, including <a href="https://www.red5.net/media-over-quic-moq/">MOQ protocol </a>support, &nbsp;DASH support in the Video Packager, autoscaling controls &amp; APIs, along with improvements and bug fixes to help you build stronger real-time streaming workflows.</p>



<p><strong>Need a custom Red5 Pro feature developed</strong> or want to <strong>prioritize a development request</strong>? We’re known for our flexibility – <a href="https://www.red5.net/contact/">contact us</a> to discuss your needs.</p>



<h2 class="wp-block-heading" id="what-s-new-in-red5-pro-v15-4-0">What’s New in Red5 Pro v15.4.0?</h2>



<p>Here is what you need to know about the <a href="https://www.red5.net/docs/red5-pro/resources/release-notes/red5-pro-release-notes-15.4.0/">Red5 Pro v15.4.0</a> update announced on April 17, 2026.&nbsp;</p>



<h3 class="wp-block-heading" id="undefined-1">New Features</h3>



<ul class="wp-block-list">
<li><strong>Introducing MOQ protocol support</strong>. Select Media over QUIC as your ingest protocol. Connect the CDN of your choice that supports MOQ to enable global scalability. <a href="https://www.red5.net/contact/">Contact us</a> if you have any questions. If you would like to try our end-to-end, production-ready MOQ streaming solution that operates at global scale,<a href="https://www.red5.net/blog/join-red5-moq-beta/"> sign up for the MOQ beta</a> available in Red5 Cloud.</li>



<li><strong>Video packager for specific streams</strong>. Introduces a Video Packager API that can target specific input streams for HLS and/or DASH output, enabling custom packaging workflows for select content (e.g. conferences, premium events).</li>



<li><strong>Added event scaling expectations scheduling API: </strong>Adds an API for configuring expected autoscale capacity over time (for example, pre-scaling for known events). This allows you to define scaling expectations and reduce cold-start latency for large events.</li>



<li><strong>Added testbed example of DC only connection: </strong>Adds a testbed example for DataChannel-only connections, helping developers test and validate pure data flows without media tracks.</li>



<li><strong>Added webhook support to Video Packager: </strong>The Video Packager can now trigger webhooks on relevant events (e.g., job start/complete, failures), making it easier to integrate with external workflows and monitoring systems.</li>



<li><strong>Video Packager can now generate master playlists from ABR variant streams: </strong>Video Packager can now generate HLS master playlists from multiple ABR variants, simplifying configuration for multi-bitrate playback.</li>



<li><strong>HLS output now features automatic time-based partitioning: </strong>HLS outputs now support automatic time-based partitioning, allowing you to segment long recordings into predictable time windows for easier management, distribution, and lifecycle control.</li>



<li><strong>Video Packager can now output S3 and local files simultaneously:</strong> Video Packager now supports writing HLS outputs to both S3 and local storage simultaneously, providing redundancy and flexible archive options.</li>



<li><strong>Added pause/resume autoscaling to debug UI: </strong>Adds the ability to pause and resume autoscaling directly from the debug UI, useful for maintenance windows or troubleshooting autoscale behavior.&nbsp;</li>
</ul>



<h3 class="wp-block-heading" id="undefined-2">Improvements</h3>



<ul class="wp-block-list">
<li><strong>Update Pro server to Red5 2.0.30</strong>: Red5 Pro server now incorporates Red5 2.0.30, bringing the latest core improvements and fixes from the underlying Red5 project.</li>



<li><strong>Added new ‘disabled’ state for Stream Manager nodes:</strong> Stream Manager nodes can now be placed into a disabled state, preventing new assignments while keeping historical and monitoring data intact. This makes it safer to drain or retire nodes without disrupting existing sessions.</li>



<li><strong>Updated jjwt library to the latest version: </strong>The JSON Web Token library has been updated to the latest version, providing security and compatibility enhancements for JWT-based authentication flows.</li>



<li><strong>Added API to start stream endpoint to accept recording configuration as JSON structure: </strong>The start‑stream endpoint can now accept a recording configuration as a JSON structure. This makes it easier to define per-stream recording options programmatically (e.g., formats, destinations, partitioning).</li>
</ul>



<h3 class="wp-block-heading" id="undefined-3">Bug Fixes</h3>



<ul class="wp-block-list">
<li>JSON metadata file is not created properly when recording streams.</li>



<li>JSON metadata file is not getting created with recordings in some circumstances.</li>



<li>Occasional high CPU usage with no clients connected.</li>



<li>Videon SRT encoder ingest.</li>



<li>Passthrough now works properly for RTMP/WebRTC in Video Packager.</li>



<li>Audio glitch in some circumstances with WHEP playback.</li>



<li>Stream Manager subscriptions to Twitch streams.</li>



<li>HLS-MP4-MKV recording now working properly for WebRTC.</li>



<li>Missing retention specifications in as-admin and as-autoscale.</li>



<li>Occasional Cauldron crashes with AAC multi-channel.</li>



<li>Some Video Packager node configurations could get into fault state unexpectedly.</li>



<li>Repaired a memory leak in session reaper.</li>



<li>Occasional edge faults when autoscaling is blocked.&nbsp;</li>
</ul>



<h2 class="wp-block-heading" id="undefined-4">Conclusion</h2>



<p>Red5 Pro v15.4.0 brings significant updates that enhance performance, reliability, and flexibility for <a href="https://www.red5.net/solutions/">real-time streaming workflows</a>. Featuring new capabilities such as Media over QUIC protocol support, DASH support in the Video Packager, autoscaling controls &amp; APIs, this release<br />expands streaming capabilities and enhances video delivery. Along with key improvements and important bug fixes, version 15.4.0 delivers a smoother and more efficient experience for developers, startup, and enterprises.&nbsp;</p>
</div>
</div>
<p>The post <a href="https://www.red5.net/blog/whats-new-in-red5-pro-v15-4-0/" rel="nofollow">What’s New In Red5 Pro v15.4.0? MOQ Protocol Support, DASH Support in the Video Packager, Autoscaling Controls &amp; APIs, And More!</a> appeared first on <a href="https://www.red5.net" rel="nofollow">Red5</a>.</p>
