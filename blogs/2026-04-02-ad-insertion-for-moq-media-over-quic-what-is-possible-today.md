---
title: "Ad Insertion for MOQ (Media over QUIC): What Is Possible Today and What Comes Next"
url: "https://www.red5.net/blog/ad-insertion-for-media-over-quic/"
date: "Thu, 02 Apr 2026 07:33:33 +0000"
author: "Chris Allen"
feed_url: "https://www.red5.net/feed/"
---
<p>To continue my coverage of all things <a href="https://www.red5.net/media-over-quic-moq/">MOQ</a>, today I want to touch on something that keeps coming up in MOQ discussions: ad insertion.</p>



<p><a href="https://www.red5.net/blog/what-is-ultra-low-latency-why-does-it-matter/">Ultra-low latency</a> delivery is only part of the equation. For MOQ to be viable in real production environments, monetization has to work too. That means clean ad signaling, measurable delivery, and architectures that scale without breaking synchronization.</p>



<div class="wp-block-rank-math-toc-block" id="rank-math-toc"><h2>Table of Contents</h2><nav><ul><li><a href="#ietf-moq-interim-at-google-s-boulder-campus">IETF MOQ interim at Google’s Boulder campus</a></li><li><a href="#does-red5-support-ad-insertion-for-moq">Does Red5 Support Ad Insertion for MOQ? </a></li><li><a href="#become-a-beta-tester-of-moq-streaming-powered-by-red5-and-cachefly">Become a Beta Tester of MOQ Streaming Powered by Red5 and CacheFly</a></li><li><a href="#conclusion">Conclusion</a></li></ul></nav></div>



<h2 class="wp-block-heading" id="ietf-moq-interim-at-google-s-boulder-campus">IETF MOQ interim at Google’s Boulder campus</h2>



<p>This was one of the topics at the recent IETF MOQ interim at Google’s Boulder campus in February 2026. Watch the video below, where I discuss this event with my teammate <a href="https://www.red5.net/author/paul-gregoire/">Paul Gregoire</a>, Red5 Solutions Architect, who attended it.&nbsp;</p>



<figure class="wp-block-embed is-type-video is-provider-youtube wp-block-embed-youtube wp-embed-aspect-16-9 wp-has-aspect-ratio"><div class="wp-block-embed__wrapper">

</div></figure>



<p class="has-text-align-center"><em>Watch my recent #ChrisAllenTalks video about the MOQ Interim at Google Boulder.&nbsp;</em></p>



<p>To better understand how these concepts apply in practice, here are the key definitions used in ad insertion workflows for MOQ:</p>



<ul class="wp-block-list">
<li><strong>Server-Side Ad Insertion</strong> (SSAI): ads are stitched directly into the video stream on the server before the stream is delivered to viewers.</li>



<li><strong>Server-Guided Ad Insertion</strong> (SGAI): the server signals ad opportunities and decides when and which ads to request and play.</li>



<li><strong>Client-Side Ad Insertion</strong> (CSAI): the video player on the viewer’s device requests, loads, and inserts ads during playback instead of receiving a prestitched stream.</li>



<li><strong>Regional blackout</strong>: a restriction that blocks or replaces live content for viewers in certain geographic areas due to licensing or local broadcast rights.</li>
</ul>



<p><a href="https://www.linkedin.com/in/gwendalsimon/" rel="noopener" target="_blank">Gwendal Simon</a> from <a href="https://www.synamedia.com/" rel="noopener" target="_blank">Synamedia</a> and <a href="https://www.linkedin.com/in/wilaw/" rel="noopener" target="_blank">Will Law</a> from <a href="https://www.akamai.com/" rel="noopener" target="_blank">Akamai Technologies</a> presented how MOQ and the MOQ Transport Streaming Format (MSF) can carry SCTE-35 signaling for Server-Guided Ad Insertion (SGAI) as well as other control scenarios such as regional blackout enforcement.</p>


<div class="wp-block-image">
<figure class="aligncenter size-large"><img alt="Dynamic ad insertion and Regional blackout use cases in a MOQ environment" class="wp-image-226263" height="571" src="https://www.red5.net/wp-content/uploads/2026/04/Dynamic-ad-insertion-and-Regional-blackout-use-cases-in-a-MOQ-environment-1024x571.png" title="Dynamic ad insertion and Regional blackout use cases in a MOQ environment" width="1024" /></figure>
</div>


<p class="has-text-align-center"><em>Dynamic ad insertion and blackout management use cases in a MOQ environment.</em></p>



<p>Figuring out how content works with advertising and blackout use cases in a MOQ environment is critical for the technology to support real-world media and entertainment applications. Because of that, the topic is receiving significant attention across the MOQ community. The problem is not fully solved yet, but progress is moving quickly as new approaches and demonstrations continue to emerge.</p>



<p>Gwendal and Will presented what is possible today: a working architecture where ad decisioning systems publish SCTE-35 signaling as structured events on a dedicated Event Timeline track, while media and advertising streams remain separate and independently distributed over MOQ. Subscribers can follow these signals in real-time to switch between media and ad tracks, fetch ad content dynamically using identifiers such as MOQ URLs, and return to the primary program stream at the correct playback moment.&nbsp;</p>



<p>Learn more from the files they presented at the event.</p>



<div class="wp-block-file aligncenter"><a href="https://www.red5.net/wp-content/uploads/2026/04/Ad-Insertion-in-MOQ-Interim-Meeting-Boulder.pdf" id="wp-block-file--media-555831fd-0998-4c4b-93e1-61e4a8b21438">Ad Insertion in MOQ &#8212; Interim Meeting Boulder</a><a class="wp-block-file__button wp-element-button" href="https://www.red5.net/wp-content/uploads/2026/04/Ad-Insertion-in-MOQ-Interim-Meeting-Boulder.pdf">Download</a></div>



<div class="wp-block-file aligncenter"><a href="https://www.red5.net/wp-content/uploads/2026/04/SGAI-Over-MOQ_-SCTE35-Based-Event-Timeline-Type-Definition.pdf" id="wp-block-file--media-87acc1c1-cfcd-4406-8e2e-62dba6a19ed3">SGAI Over MOQ_ SCTE35-Based Event Timeline Type Definition</a><a class="wp-block-file__button wp-element-button" href="https://www.red5.net/wp-content/uploads/2026/04/SGAI-Over-MOQ_-SCTE35-Based-Event-Timeline-Type-Definition.pdf">Download</a></div>



<p>The approach demonstrates how existing broadcast signaling models can operate over MOQ without embedding cues directly inside the video stream, allowing signaling and media delivery to scale independently while preserving the timing relationships needed for live playback.&nbsp;</p>



<h2 class="wp-block-heading" id="does-red5-support-ad-insertion-for-moq">Does Red5 Support Ad Insertion for MOQ?&nbsp;</h2>


<div class="wp-block-image">
<figure class="aligncenter size-large"><img alt="Meet Red5 at Nab 2026" class="wp-image-225440" height="580" src="https://www.red5.net/wp-content/uploads/2026/03/Meet-Red5-at-Nab-2026-1024x580.png" title="Meet Red5 at Nab 2026" width="1024" /></figure>
</div>


<p>We are actively working on this area with partners like <a href="https://www.google.com/aclk?sa=L&amp;pf=1&amp;ai=DChsSEwit6qTSzM6TAxW2yHkEHdpcJ80YACICCAEQABoCd2Y&amp;co=1&amp;ase=2&amp;gclid=Cj0KCQjwp7jOBhDGARIsABe7C4dwBA-WQb-cUPyVfTrFCkCHvZu1sf56nWfg3SjMwLrZWcMuKgxdz7waAjAOEALw_wcB&amp;cid=CAASWuRoKNZ4Kktya8p1ipa6Xwwb7At7elKahQ6-Ow3ueOwqMemt4y_LlLyvJCbdETdnSow74eUpYN8FompKre7tieSmOfIIQc9kmlfIB6VlrOCpgXxNhMdKuNBRlw&amp;cce=2&amp;category=acrcp_v1_32&amp;sig=AOD64_3U-Sercsd5t1w9ulUcIaAzniKTqg&amp;q&amp;nis=4&amp;adurl=https://showfer.com?gad_source%3D1%26gad_campaignid%3D23321922150%26gbraid%3D0AAAAACzRizUJqa2hcsk0UWdZApXQ63rbi%26gclid%3DCj0KCQjwp7jOBhDGARIsABe7C4dwBA-WQb-cUPyVfTrFCkCHvZu1sf56nWfg3SjMwLrZWcMuKgxdz7waAjAOEALw_wcB&amp;ved=2ahUKEwi46J3SzM6TAxWrgP0HHR-XCiQQ0Qx6BAgMEAE" rel="noopener" target="_blank">Showfer Media</a>, integrating ad workflows into real-time streaming pipelines so MOQ can move from experimental to production-ready systems. If you are interested in learning more, visit us at the <a href="https://www.red5.net/blog/meet-red5-at-nab-show-2026/">NAB Show 2026</a>, where we will showcase MOQ and <a href="https://www.red5.net/truetime/">TrueTime Solutions™</a> in action at the Nomad Media booth W2357 and AWS booth W1701. Reach out to us <a href="https://www.red5.net/contact/?text=Hi,%20I%20would%20like%20to%20meet%20you%20at%20the%20NAB%20Show%202026">here</a> to schedule a meeting at NAB. Our schedule is filling up quickly, so it is best to plan ahead.</p>



<h2 class="wp-block-heading" id="become-a-beta-tester-of-moq-streaming-powered-by-red5-and-cachefly">Become a Beta Tester of MOQ Streaming Powered by Red5 and CacheFly</h2>


<div class="wp-block-image">
<figure class="aligncenter size-full"><img alt="Red5 Cloud and CacheFly streaming solution overview" class="wp-image-184093" height="400" src="https://www.red5.net/wp-content/uploads/2025/09/Red5-Cloud-and-CacheFly-streaming-solution.png" title="Red5 Cloud and CacheFly streaming solution" width="800" /></figure>
</div>


<p>Beyond the live demos, we will introduce how <a href="https://www.red5.net/red5-cloud-low-latency-live-streaming-platform/">Red5 Cloud</a> will deliver MOQ at scale through our partnership with <a href="https://www.red5.net/partners/cachefly/">CacheFly</a>. In this workflow, live streams are ingested into Red5, processed through our video packaging layer, and delivered via CacheFly using either MOQ or HTTP-based protocols like <a href="https://www.red5.net/hls-server/">HLS</a> and LL-HLS. This gives customers flexibility. You can deliver ultra-low latency streams with MOQ where real-time performance matters most, while still supporting traditional formats for broader device compatibility. It is not about replacing one protocol with another. It is about choosing what works best for your use case.</p>



<p>Our teams will be collecting beta testers at NAB for our globally deployed MOQ network. It allows Red5 Cloud users to leverage CacheFly CDN for MOQ delivery. If you want in on this early or just want some more details on how it might work for your business, reach out to us using <a href="https://www.red5.net/contact/?text=Hi%2C%20I%E2%80%99d%20like%20to%20join%20your%20globally%20deployed%20MOQ%20network%20beta">this link</a>.</p>



<h2 class="wp-block-heading" id="conclusion">Conclusion</h2>



<p>Ad insertion for MOQ is evolving quickly as the industry works to make real-time streaming monetizable without sacrificing synchronization or scale. While approaches like SCTE-35–based signaling and SGAI over MOQ already show strong potential, the ecosystem is still maturing as partners continue building production-ready workflows. With ongoing collaboration and real-world testing, MOQ is moving closer to supporting reliable, scalable ad-supported streaming. For a deeper look at how MOQ compares to existing transport approaches, read our &#8220;<a href="https://www.red5.net/blog/srt-vs-moqt/">SRT vs MOQT</a>&#8221; blog.</p>
<p>The post <a href="https://www.red5.net/blog/ad-insertion-for-media-over-quic/" rel="nofollow">Ad Insertion for MOQ (Media over QUIC): What Is Possible Today and What Comes Next</a> appeared first on <a href="https://www.red5.net" rel="nofollow">Red5</a>.</p>
