---
title: "MOQ at the NAB Show 2026: What to Look For Across the Show"
url: "https://www.red5.net/blog/moq-at-the-nab-show-2026/"
date: "Thu, 16 Apr 2026 14:59:48 +0000"
author: "Chris Allen"
feed_url: "https://www.red5.net/feed/"
---
<div class="wp-block-greenshift-blocks-container gspb_container gspb_container-gsbp-2e55073 blog_parent" id="gspb_container-id-gsbp-2e55073">
<div class="wp-block-greenshift-blocks-container gspb_container gspb_container-gsbp-5d8fe22 blog_left" id="gspb_container-id-gsbp-5d8fe22">
<div class="wp-block-rank-math-toc-block" id="rank-math-toc"><h2>Table of Contents</h2><nav><ul><li><a href="#moq-demos">MOQ Demos</a></li><li><a href="#moq-discussions">MOQ Discussions</a></li><li><a href="#conclusion">Conclusion</a></li></ul></nav></div>
</div>



<div class="wp-block-greenshift-blocks-container gspb_container gspb_container-gsbp-13564b4 blog_right" id="gspb_container-id-gsbp-13564b4">
<p><a href="https://www.red5.net/media-over-quic-moq/">Media over QUIC</a> is quickly becoming one of the most discussed topics in streaming, and it is showing up across multiple booths, not just in theory, but in working demos. If you are heading to the NAB Show, it is worth spending time exploring how different companies are approaching it. </p>



<h2 class="wp-block-heading" id="moq-demos">MOQ Demos</h2>



<p>My advice is simple. Do not just check out one demo. Compare implementations. Ask how each team handles scale, latency, and interoperability. How close are they to having production ready MOQ enabled solutions? That is where the real differences show up.</p>



<figure class="wp-block-table"><table class="has-fixed-layout"><tbody><tr><td><strong>Company</strong></td><td><strong>Booth Number</strong></td><td><strong>Demo Description</strong></td></tr><tr><td>Ant Media</td><td>W3317</td><td>MOQ streaming alongside WebRTC and other protocols on self-managed and auto-scalable infrastructure.</td></tr><tr><td>AWS</td><td>W1701</td><td>Red5-powered MOQ demo running in cloud infrastructure.</td></tr><tr><td>Bitmovin</td><td>W3323</td><td>MOQ playback via Player Web X, including joint demos with Oracle and Cloudflare.</td></tr><tr><td>Broadpeak</td><td>W3034</td><td>Contribution to joint MOQ ecosystem demo across the delivery and packaging workflow.</td></tr><tr><td>CacheFly</td><td>W3129</td><td>Red5-powered MOQ demo running on local and edge network environments.</td></tr><tr><td>Cloudflare</td><td>W2300G</td><td>1. Demo with Bitmovin: Live MOQ stream delivered over global relay network with real-time playback.<br />2. Demo with Wowza: OBS feeding to Wowza origin infrastructure, with CMAF packaged over MoQT in the CMSF format to a relay server acting as the CDN.</td></tr><tr><td>Nomad Media</td><td>W2357</td><td>Red5-powered MOQ demo in closed network environments.<br /><br />Demos presented by Cisco and other OpenMOQ Consortium members will showcase the open-source work developed by both our team and other contributors, including the open-source MOQ player and relay.</td></tr><tr><td>Oracle</td><td>W1073HS</td><td>Part of joint MOQ demo showing interoperability across ingest, packaging, delivery, and playback.</td></tr><tr><td>Red5</td><td>(multiple booths via partners)</td><td>Live camera feed demo comparing MOQ, WebRTC, LL-HLS, and HLS side by side for real-time latency and performance.</td></tr><tr><td>Norsk</td><td>W3113</td><td>Live media delivered at sub-second latency over Cloudflare’s global MOQ relay network, highlighting a production media workflow engine and a worldwide delivery network using the same next-generation protocol end to end.</td></tr><tr><td>Synamedia</td><td>W2851</td><td>Two demos:  targeted ad insertion in MOQ and B2B distribution workflows with backward compatibility with MPEG2-TS.</td></tr></tbody></table></figure>



<p class="has-text-align-center"><em>MOQ Demos at the NAB Show 2026</em>.</p>



<ol class="wp-block-list">
<li>At <a href="https://antmedia.io/join-ant-media-at-nab-2026-las-vegas-w3317/" rel="noopener" target="_blank">Ant Media</a> (Booth <strong>W3317</strong>), you can see MOQ streaming alongside WebRTC and other delivery protocols run on self-managed or fully auto-scalable live streaming services.</li>



<li>Oracle, Bitmovin, and Broadpeak are <a href="https://broadpeak.tv/blog/joint-demos-at-nab-show-2026-for-video-streaming/" rel="noopener" target="_blank">showcasing a joint MOQ demo</a> across multiple booths (<strong>W1073HS, W3323, W3034</strong>). The interesting part here is not just the demo itself, but the fact that multiple vendors are working together across ingest, packaging, delivery, and playback. That is what it takes to move a protocol forward.</li>



<li>Another example comes from <a href="https://bitmovin.com/blog/media-over-quic-bitmovin-cloudflare/" rel="noopener" target="_blank">Bitmovin and Cloudflare</a> (<strong>W3323 and W2300G</strong>), where a live MOQ stream is delivered over a global relay network and played back in real time through a web player. No custom integrations, no proprietary handshakes. Just an open approach working end-to-end.</li>



<li>Red5’s (my team’s) video streaming infrastructure <a href="https://www.red5.net/blog/meet-red5-at-nab-show-2026/#red5-team-at-nab-show-2026-in-april">will power several demos</a>. One of them features a live camera feed from the show floor streamed back to the booth using multiple protocols simultaneously. You will see MOQ, <a href="https://www.red5.net/webrtc-server/">WebRTC</a>, LL-HLS, and <a href="https://www.red5.net/hls-server/">HLS</a> side by side, making it easy to compare latency and performance in real-time. If you want to see how this runs across environments: <a href="https://www.red5.net/partners/nomad/">Nomad Media</a> <strong>booth W2357</strong> for closed networks, <a href="https://www.red5.net/partners/aws/">AWS</a> <strong>booth W1701</strong> for cloud deployment, <a href="https://www.red5.net/partners/cachefly/">CacheFly</a> <strong>booth W3129</strong> for showcasing the planned integrated <a href="https://www.red5.net/blog/meet-red5-at-nab-show-2026/#become-a-beta-tester-of-moq-streaming-powered-by-red5-and-cachefly">Red5 Cloud and CacheFly solution</a>. Other demos from other OpenMOQ contributors, including Cisco and others, showcasing shared components like the MOQ player and relay will be at these locations as well. That collaborative work is what is pushing this forward.</li>



<li>Norsk will <a href="https://norsk.video/norsk-studio-moq-nab2026/" rel="noopener" target="_blank">showcase its latest MOQ capabilities</a> at <strong>booth W3113</strong>, demonstrating live media delivered at sub-second latency over Cloudflare’s global MOQ relay network. This highlights a production media workflow engine and a worldwide delivery network using the same next-generation protocol end to end.</li>



<li>Synamedia will showcase two demos at booth <strong>W2851</strong>: targeted ad insertion in MOQ and B2B distribution workflows with backward compatibility with MPEG2-TS.</li>



<li>Wowza, in partnership with Cloudflare, will <a href="https://www.wowza.com/blog/wowza-demos-ai-workflows-at-nab-show-2026" rel="noopener" target="_blank">demonstrate a Media over QUIC workflow at the Cloudflare booth</a> <strong>W2300G</strong>, featuring CMAF packaging over MOQ, CDN relay delivery, and low-latency playback via an experimental Shaka Player.</li>
</ol>



<h2 class="wp-block-heading" id="moq-discussions">MOQ Discussions</h2>


<div class="wp-block-image">
<figure class="aligncenter size-large"><img alt="OpenMOQ and MOQ speaking session at NAB Show 2026" class="wp-image-225759" height="538" src="https://www.red5.net/wp-content/uploads/2026/03/OpenMOQ-and-MOQ-speaking-session-at-NAB-Show-2026-1024x538.png" title="OpenMOQ and MOQ speaking session at NAB Show 2026" width="1024" /></figure>
</div>


<ol class="wp-block-list">
<li>If you want a deeper look at where things are heading, there is also a <a href="https://www.nabshow.com/session/openmoq-and-moq-a-collaborative-effort-to-push-the-next-evolution-in-streaming/" rel="noopener" target="_blank">free session</a> at the NAB Streaming Summit bringing together founding members of the <a href="https://openmoq.org/" rel="noopener" target="_blank">OpenMOQ Software Consortium</a>. The discussion focuses on the collaborative work behind high-performance MOQ software and what it takes to move from an RFC to real-world deployments. It will cover where MOQ creates new opportunities, what innovation it enables, and the challenges that still need to be addressed, along with demos and audience Q&amp;A. Unlike other sessions at the Streaming Summit this one is free and open to anyone with a show floor badge. </li>



<li>Be sure to stop by and then head to the Streaming Summit Mixer Party right afterwards to talk with the speakers.</li>
</ol>



<h2 class="wp-block-heading" id="conclusion">Conclusion</h2>



<p>Media over QUIC stops being a theoretical concept at the NAB Show 2026 and becomes something you can see, test, and question in real demos. Across multiple booths, you can compare how different teams implement MOQ and then continue the conversation directly with the developers behind it. The session and Mixer Party give you a practical way to understand where the protocol stands today and where it is heading next.</p>



<p>Be sure to check the official NAB exhibitor directory to find these booths and plan your time across the floor: <a href="https://nab26.mapyourshow.com/8_0/exhview/index.cfm" rel="noopener" target="_blank">https://nab26.mapyourshow.com/8_0/exhview/index.cfm</a></p>



<p>And if you are interested in meeting me at the show, you can get on our meeting schedule here: </p>



<div class="gspb_button_wrapper gspb_button-id-gsbp-59e0af8" id="gspb_button-id-gsbp-59e0af8"><a class="wp-block-greenshift-blocks-buttonbox gspb-buttonbox wp-element-button" href="https://www.red5.net/contact/?text=Hi%2C%20I%20would%20like%20to%20meet%20you%20at%20the%20NAB%20Show%202026" rel="noopener" target="_blank"><span class="gspb-buttonbox-textwrap"><span class="gspb-buttonbox-text"><span class="gspb-buttonbox-title">Book a meeting</span></span></span></a></div>
</div>
</div>
<p>The post <a href="https://www.red5.net/blog/moq-at-the-nab-show-2026/" rel="nofollow">MOQ at the NAB Show 2026: What to Look For Across the Show</a> appeared first on <a href="https://www.red5.net" rel="nofollow">Red5</a>.</p>
