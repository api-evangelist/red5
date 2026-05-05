---
title: "Consensus on a MOQ Media Layer Player Framework Should Speed Market Adoption"
url: "https://www.red5.net/blog/consensus-on-a-moq-media-layer-player-framework/"
date: "Thu, 30 Apr 2026 06:55:11 +0000"
author: "Red5 Team"
feed_url: "https://www.red5.net/feed/"
---
<div class="wp-block-greenshift-blocks-container gspb_container gspb_container-gsbp-2e55073 blog_parent" id="gspb_container-id-gsbp-2e55073">
<div class="wp-block-greenshift-blocks-container gspb_container gspb_container-gsbp-5d8fe22 blog_left" id="gspb_container-id-gsbp-5d8fe22">
<div class="wp-block-rank-math-toc-block" id="rank-math-toc"><h2>Table of Contents</h2><nav><ul><li><a href="#introduction">Introduction</a></li><li><a href="#the-state-of-play-in-moq-evolution">The State of Play in MOQ Evolution</a></li><li><a href="#playa-and-moq-player-development">Playa and MOQ Player Development</a><ul><li><a href="#six-known-options">Six Known Options</a></li><li><a href="#the-playa-connection">The Playa Connection</a></li></ul></li><li><a href="#red5-s-role-in-enabling-use-of-moq-over-partner-cdns">Red5’s Role in Enabling Use of MOQ over Partner CDNs</a></li><li><a href="#red5-s-support-for-optimal-hybrid-use-of-moqt-with-webrtc">Red5’s Support for Optimal Hybrid Use of MOQT with WebRTC</a></li><li><a href="#conclusion">Conclusion</a></li></ul></nav></div>
</div>



<div class="wp-block-greenshift-blocks-container gspb_container gspb_container-gsbp-13564b4 blog_right" id="gspb_container-id-gsbp-13564b4">
<p><strong><em>Modular Red5 Template Is Open-Source Path to Multiple Streaming Formats</em></strong></p>



<h2 class="wp-block-heading" id="introduction">Introduction</h2>



<p>Amid intensifying demand for the interoperable approach to next-generation streaming specified by the emerging MOQ standard there’s a lot riding on the market’s ability to determine how payloads will be formatted in the MOQ Media Layer for distribution and playback.</p>



<p>Happily, we can report that Red5 has garnered significant support for a way forward that relies on a MOQ player template we’re calling Playa. As a freely available open-source solution, Playa has the flexibility to accommodate configurations of players for device playback of virtually any MOQ-compatible streaming format operating over the MOQ Media Layer, which in International Standards Organization (ISO) parlance is the application layer that rides on the transport layer in internet communications.</p>



<p>This has been a top priority in our work as a founding member of the OpenMOQ Software Consortium, an ad hoc body separated from but closely aligned with the Internet Engineering Task Force (<a href="https://datatracker.ietf.org/group/moq/about/" rel="noopener" target="_blank">IETF</a>), which is overseeing MOQ standardization. Now, with <a href="https://github.com/red5pro/moq-playa" rel="noopener" target="_blank">Playa</a> emerging as the OpenMOQ Consortium’s leading candidate for formatting MOQ stream playback, the stage is set for widespread experimentation that will expedite commercial rollouts once the MOQ Transport (MOQT) standard is finalized later this year.</p>



<p>There’s been a lot of confusion about what MOQ is owing to its origins as an acronym for Media over QUIC, which has alternative meanings related to emerging proprietary platforms that rely on QUIC transport and to use of the QUIC protocol as the default transport mode with version 3 of conventional Hypertext Transfer Protocol (HTTP/3) streaming. IETF hopes to distinguish what it’s doing by using MOQ as a free-standing label for a new platform, which, as explained in our <a href="https://www.red5.net/blog/what-is-moq-media-over-quic/">What is MOQ blog</a>, avoids the complexity and error-prone request-response method used with the dominant HTTP streaming system while eliminating the set-up and other complications intrinsic to real-time streaming via <a href="https://www.red5.net/blog/what-is-webrtc/">WebRTC</a>.</p>



<p>Moreover, the new standard provides a way to automatically tune end-to-end latencies to whatever levels meet user requirements, including real-time interactive streaming use cases that need support for latencies registering at or below 300ms. And, already, MOQ has been made compatible with leading Web browsers, currently including Google Chrome, Microsoft Edge, Mozilla Firefox and Apple Safari, which largely eliminates the need for client plug-in software.&nbsp;</p>



<p>Red5 and the <a href="https://www.red5.net/blog/red5-joined-openmoq/">other OpenMOQ Consortium founders</a>, including Akamai, CDN77, Cisco, Synamedia and YouTube, are among a growing host of streaming providers and users worldwide who are wholeheartedly behind MOQ. We all recognize that an interoperable, tunable approach to structuring a new streaming network foundation is the fastest path to unleashing the full power of market forces seeking to exploit real-time video streaming at mass scales on an as-needed basis.</p>


<div class="wp-block-image">
<figure class="aligncenter size-large"><img alt="Get access to Red5 MOQ live streaming Beta" class="wp-image-227532" height="576" src="https://www.red5.net/wp-content/uploads/2026/04/Get-access-to-Red5-MOQ-live-streaming-Beta-1024x576.png" title="Get access to Red5 MOQ live streaming Beta" width="1024" /></figure>
</div>


<p>The industry is moving rapidly toward proving the point with preparations for MOQ underway on many fronts. We’ve officially launched our MOQ capabilities and are starting with a <a href="https://www.red5.net/blog/join-red5-moq-beta/">limited beta</a> that is not publicly available yet. Access is granted on an individual basis to make sure each deployment is aligned with a specific use case. This initial phase is intentionally selective so we can fine-tune the solution around the scenarios that matter most right now, including real-time latency and delivering to geographically distributed audiences at one-to-many scale. More about this in <a href="https://www.linkedin.com/feed/update/urn:li:activity:7455609456068825088/" rel="noopener" target="_blank">Chris Allen’s LinkedIn post</a>. This will lead to full commercial rollout by mid-summer.</p>



<div class="gspb_button_wrapper gspb_button-id-gsbp-d2ff09d" id="gspb_button-id-gsbp-d2ff09d"><a class="wp-block-greenshift-blocks-buttonbox gspb-buttonbox wp-element-button" href="https://www.red5.net/contact/?text=Hi%2C%20I%E2%80%99d%20like%20to%20join%20your%20globally%20deployed%20MOQ%20network%20beta" rel="noopener" target="_blank"><span class="gspb-buttonbox-textwrap"><span class="gspb-buttonbox-text"><span class="gspb-buttonbox-title">Join our MOQ Beta</span></span></span></a></div>



<p>At the same time, we’re proceeding full steam ahead with serving real-time streaming customers with our global implementations of <a href="https://www.red5.net/webrtc-server/">WebRTC</a> transport utilizing <a href="https://www.red5.net/blog/xdn-architecture-traditional-cdns-need-not-apply/">XDN Architecture</a> in our Red5 Cloud service and in customer-mounted multi-cloud iterations supported by <a href="https://www.red5.net/live-streaming-sdks/">Red5 SDKs</a>. How all this works in bringing a broad array of use cases to life with our portfolio of <a href="https://www.red5.net/truetime/">TrueTime™ application toolsets</a> is well documented on our website.</p>



<p>In the discussion that follows we explore where things stand with MOQ player development. Along with explaining Playa, we’ll look at other early initiatives and share thoughts about how the ones we’re familiar with might work with Playa. And we explain the steps Red5 has taken with our partners to enable early implementations of MOQ at global scales.</p>



<p>The discussion concludes with consideration of what can be achieved with use of the standard based on current MOQ Transport specifications and whether some real-time use cases will be best left to continued reliance on WebRTC. As shall be seen, from where we sit today it looks like MOQ will play a major role in normalizing real-time streaming across the global consumer markets while leaving video calling along with many applications in the enterprise, <a href="https://www.red5.net/solutions/drone-public-safety/">public safety</a>, <a href="https://www.red5.net/solutions/air-gapped-live-streaming/">military</a> and other <a href="https://www.red5.net/solutions/">commercial domains</a> to execution over WebRTC transport.</p>



<h2 class="wp-block-heading" id="the-state-of-play-in-moq-evolution">The State of Play in MOQ Evolution</h2>



<p>Standards, especially those like MOQ built on open-source <a href="https://www.red5.net/video-streaming-technology/">technology</a>, ensure the interoperability among whole systems and their components that’s essential to expediting adoption of new approaches to operating over the internet. But, as a community-driven process involving an unlimited flow of tech contributions and opinions, standards-building typically takes a long time.</p>



<p>That hasn’t been the case with MOQ, which has reached an advanced stage of development in a remarkably short time, going from initiation to near completion in less than four years. MOQ Transport, the foundation for the new platform, is going through final revisions with expectations that the standard will be finalized by mid-summer.&nbsp;</p>



<p>As described in the <a href="https://www.red5.net/blog/what-is-moq-media-over-quic/">What is MOQ</a> blog we referenced in the introduction, MOQ Transport determines how sessions linking end users to servers are set up and terminated and how binary-coded descriptions of payload segment parameters, destination IDs, time stamps and routing directions are conveyed in transport packet headers at the front end of the payload segments. The platform relies on a system of relay nodes that allow any given stream to be fanned out from a single source to any number of end users with minimal use of processing resources along the way, which greatly expands the volume of streams that can be handled by relay servers.</p>



<p>Adding to the versatility, tunable latencies range from real-time at 200-400ms to what developers call “interactive live” at 2 seconds, which might be sufficient for some interactive applications, to “conservative live” maintaining persistent HD, 4K or, eventually, 8K quality at 5 seconds. Moreover, CDN operators can design their relay caches to support recording live content for short-term replay and catchup, and there’s also support for bringing long-term storage into play for sending live content to VOD archives and cloud DVR platforms.&nbsp;</p>



<p>At the media layer there’s no limit to the variety of streaming formats that can be devised for MOQ instances insofar as the MOQ Media Layer is decoupled from the Transport Layer, which allows CDN operators to offer MOQ Transport as a service while freeing their customers to configure streaming formats for any use cases they want to support. This opens opportunities not only for streaming formats targeting mass market applications but for niche formats as well, including video-free versions such as might be needed for chat services, autonomous vehicle operations, industrial IoT or smart city management.&nbsp;</p>



<p>In the case of mass market video streaming applications, MOQ Media Layer-compatible streaming formats will define how the streamed A/V and ancillary elements conveying captioning, personalized and commonly shared features and ads, and other applications are compressed, encrypted and packaged for playback by media players running on receiving devices. IETF is developing a two-pronged standard for one such streaming format, formerly encapsulated as a single format called the <a href="https://www.ietf.org/archive/id/draft-law-moq-warpstreamingformat-00.html?utm_source=chatgpt.com" rel="noopener" target="_blank">WARP Streaming Format</a> but now divided to accommodate two versions for use with and without the package framing known as Common Media Application Format (CMAF).</p>



<p>The different approaches to CMAF are the only thing that distinguishes what’s now known as MOQ Streaming Format (MSF) from the version dubbed <a href="https://datatracker.ietf.org/doc/html/draft-ietf-moq-cmsf-00?utm_source=chatgpt.com" rel="noopener" target="_blank">CMSF</a>, where the “C” stands for <a href="https://www.red5.net/blog/what-is-cmaf/">CMAF</a>. Both versions are meant to provide an IETF-standardized version of a MOQ streaming format that can support the preponderance of use cases that will be flowing over MOQ Transport.</p>



<p>As described by the IETF’s MOQ Working Group, MSF targets real-time and interactive levels of live payloads as well as VOD content by using the IETF’s <a href="https://datatracker.ietf.org/doc/html/draft-ietf-moq-loc-01" rel="noopener" target="_blank">Low Overhead Media Container</a> (LOC) protocol as a light-weight approach to stream-layer packaging that aligns with media formats using WebCodecs, which is a standard defining interfaces with encoders and decoders used in internet communications. CMSF adds CMAF as an optional alternative to relying on LOC.</p>



<p>Both define how what’s known as a catalog communicates information describing publishers’ output, and it specifies:&nbsp;</p>



<ul class="wp-block-list">
<li>how content should be packaged, encrypted and signaled;&nbsp;</li>



<li>the use of latencies and the level of prioritization accorded real-time transmissions;</li>



<li>details pertaining to broadcast workflows and how they’re initiated and terminated, and</li>



<li>the parameters directing devices’ execution of ABR profile switching.&nbsp;&nbsp;</li>
</ul>



<p>As to what other MOQ streaming formats might be in the offing, much will be revealed as participants in the development process introduce media players tailored to their constituents’ needs. The good news is that, at this point, Red5 and others can confidently implement infrastructure for testing MOQ applications at the transport level knowing that users will have access to MOQ media players that can execute playback of their payloads in an open-source, interoperable environment that maximizes their market reach.</p>



<h2 class="wp-block-heading" id="playa-and-moq-player-development">Playa and MOQ Player Development</h2>


<div class="wp-block-image">
<figure class="aligncenter size-large"><img alt="6 MOQ Players You Need To Know About" class="wp-image-205078" height="576" src="https://www.red5.net/wp-content/uploads/2026/01/6-MOQ-Players-You-Need-To-Know-About-1024x576.png" title="6 MOQ Players You Need To Know About" width="1024" /></figure>
</div>


<p>This is where the efforts of the OpenMOQ Software Consortium are paying off with its goal of fostering collaboration on development and accelerated deployment of open-source solutions tied to MOQ Transport. Along with the founding members listed in the introduction, consortium membership has expanded to include Bitmovin, qualabs, Vindral, Wowza, <a href="https://www.aau.at/en/" rel="noopener" target="_blank">Austria’s University of Klagenfurt</a>, and <a href="https://www.ozyegin.edu.tr/" rel="noopener" target="_blank">Özyeğin Üniversity</a> in Istanbul.&nbsp;</p>



<p>Majority consensus among these key players that our new Playa open-source software stack provides a flexible template for tailoring browser-supported players specific to various streaming formats signals there’s now a way forward to begin working with MOQ in the real world.&nbsp;</p>



<p>Consortium support fuels our work with MOQ developers within and outside the consortium who appreciate what the functionalities embodied in Playa architecture mean to their own player development goals.&nbsp;</p>



<h3 class="wp-block-heading" id="six-known-options">Six Known Options</h3>



<p>At present we’re aware of six initiatives that have produced or are close to completing MOQ players. Some are well known to us and others we’re still waiting to learn more about. As <a href="https://www.red5.net/blog/6-moq-players-you-need-to-know-about/">described in this blog</a>, the list includes:</p>



<ul class="wp-block-list">
<li><a href="https://github.com/moq-dev/moq/tree/main/js" rel="noopener" target="_blank">Moq-js</a>, which is the player for <a href="https://doc.moq.dev/concept/layer/moq-lite#compatibility" rel="noopener" target="_blank">MOQ Lite</a> – As its name implies, MOQ Lite is a subset of MOQ Transport developed by former Twitch and Discord engineer Luke Curley to accomplish MOQ calls with elimination of some requirements in the protocol stack without undermining basic functionalities supporting live multidirectional streaming. Most notably, it eliminates the MOQT Fetch process used for VOD and DVR scrubbing, falling back instead on HTTP streaming architecture for those applications. We’ve been working with Curley to ensure compatibility of the Moq-js player with Playa. It appears that CDN operators who want to take advantage of MOQ Lite and the full implementation of MOQT will need to dedicate resources specific to each.&nbsp;</li>



<li><a href="https://github.com/facebookexperimental/moq-encoder-player" rel="noopener" target="_blank">Moq-encoder-player</a> by Meta – This is another project Red5 has been working with, in this case to facilitate Meta’s development of a browser-supported player that’s devoted to implementing a live video and audio encoder to be used in creating and consuming MOQ streams. As currently constituted, the player is meant to provide a minimal platform to help with testing MOQ interoperability. But the project means Meta is likely to be putting its considerable clout behind MOQ.</li>



<li><a href="https://bitmovin.com/player-web-x/" rel="noopener" target="_blank">Player Web X</a> by Bitmovin – This is the player framework Bitmovin has created for developers to use as a way to build players with superior speed and performance efficiency in multiple streaming domains, including legacy HLS and Dash as well as MOQ. Bitmovin has announced Player Web X will be available for use with the MOQ relay system Cloudflare has implemented on its global CDN, presumably in compatibility with MSF and possibly other MOQ streaming formats as they emerge. While the OpenMOQ Consortium’s members, including Bitmovin, are committed to the open-source agenda pertaining to creating a streaming format running over MOQT, the mandate leaves room for use of proprietary players or other extensions that members bring to the table. At this point the long-standing Player Web X framework is not open-sourced, but it’s possible at least some aspects to the MOQ version could make use of the Playa template to streamline its interactions with MOQT.</li>



<li><a href="https://github.com/moqtail/moqtail" rel="noopener" target="_blank">MOQtail</a> by a team affiliated with consortium member Özyeğin University and led by Professor Ali C. Begen – Now on Draft 14, MOQtail, which works with CMSF,&nbsp; is one of the longest running MOQ player projects with a foundation in Apache 2.0 licensing. While it has not gained much traction with community adoption, it has benefitted from sponsorship provided by Akamai, AWS and Cisco. One of the player’s distinguishing characteristics is that it supports both MSF and a version of MSF known as CMSF, which utilizes the Common Media Application Format (CMAF). The IETF MOQ Working Group has dropped CMSF from its MSF specifications, but, as described below, we provide support for CMAF in Playa. It remains to be seen whether MOQtail ends up adopting the Playa framework.</li>



<li><a href="https://github.com/Eyevinn/warp-player" rel="noopener" target="_blank">WARP Player</a> by <a href="https://www.eyevinntechnology.se/" rel="noopener" target="_blank">Eyevinn Technology</a> – This is a fairly new project initiated by Eyevinn, an M&amp;E-focused video streaming technology consultancy and platform builder based in Stockholm. The player is designed to only work with CMAF-compatible streaming formats, including CMSF.&nbsp; We’ve not had any interactions with the Eyevinn development team to assess what the thinking there is about working within the Playa framework.</li>



<li><a href="https://github.com/shaka-project/shaka-player/commit/ef361ed03995b7591b4aa3210c4f9aed7e4fec67" rel="noopener" target="_blank">Shaka Player</a> – This is a general-purpose player initiative originally undertaken as an open-source project at Google centered on support for HLS and DASH in Web, Android and TV playback scenarios. With introduction of proprietary elements deemed beneficial to the player Google relinquished control to an independent community of engineers, who introduced support for MOQ in Q1 2026 in what is now known as the Shaka Project, which also includes the Shaka Packager and Streamer. The effort is aimed at ensuring cutting edge advancements like surround sound can be implemented with MOQ player support compatible with CMSF and licensed through Apache 2.0.</li>
</ul>



<p>We also note there’s work being done within the consortium on Media Layer components targeted specifically to the contribution segment of MOQ Transport involving publishers who are feeding their content to multiple affiliates for distribution to their audiences. This is an area of development unrelated to the distribution leg and client players that involves consortium co-founder Synamedia. They’re introducing a unified playout platform capable of delivering publishers’ content via MOQ Transport to affiliates in whatever mode they’re using to reach end users, whether it’s via MOQ, HLS and DASH streams or traditional MPEG TV channels.</p>



<h3 class="wp-block-heading" id="the-playa-connection">The Playa Connection</h3>



<figure class="wp-block-embed is-type-video is-provider-youtube wp-block-embed-youtube wp-embed-aspect-16-9 wp-has-aspect-ratio"><div class="wp-block-embed__wrapper">

</div></figure>



<p>Now with <a href="https://github.com/red5pro/moq-playa" rel="noopener" target="_blank">Playa</a> serving as the OpenMOQ Consortium-endorsed framework for MOQ player development all of these initiatives and any others that come along can benefit from a structure that modularly encompasses all the elements that might be needed to build a MOQ player. Developers can construct their pipelines using whatever components they need with a great deal of flexibility in the selection of external tools for execution of Playa-compatible functionalities.</p>



<p>In other words, there’s something for everyone, including developers of MOQ streaming formats that no one in the community is yet aware of. Following is a brief summary of how Playa makes this possible, all in the context of conforming to MOQT specifications.</p>



<p>Along with supporting modularly independent use of components, we adhered to design principles that include:</p>



<ul class="wp-block-list">
<li>Testability of processing and pipeline logic independent of platform-specific decoding and API rendering,&nbsp;</li>



<li>Framework compatibility with independent UIs and state-based frameworks used in providing rendering targets,</li>



<li>Extensibility through use of pluggable extension points for object transforms, recovery policies and handling application-specific events.</li>
</ul>



<p>The Playa architecture defines functional MOQ player blocks related to:&nbsp;</p>



<ul class="wp-block-list">
<li>Managing MOQ Transport with support for both QUIC and WebTransport as well as stream multiplexing,</li>



<li>Session management,&nbsp;</li>



<li>Catalog parsing and track enumeration,&nbsp;</li>



<li>Managing packaging,</li>



<li>Maintaining stable performance over the media pipeline through jitter buffering, gap detection, A/V synchronization and control over decoder states,</li>



<li>Rendering video and audio with frame timing,</li>



<li>Quality control with ABR track selection and switching,</li>



<li>Recovery involving prescribed modes of error detection, escalation and reconnection.</li>
</ul>



<p>Some other highlights include:</p>



<ul class="wp-block-list">
<li>Packaging – The player must support either LOC or CMAF but preferably both.</li>



<li>Access authentication – This should follow principles defined for MOQ Relay Requirements with support for CAT-4-MOQ token usage and/or Privacy Pass Authentication recommended as well.</li>



<li>Security – All connections must use TLS 1.3+ as required by QUIC, and there should be support for securing development modes, such as self-signed certificate hashes for WebTransport.</li>



<li>MOQT version support – The player must support at least version 14 or 16 of the latest MOQT drafts with both recommended to ensure maximum interoperability during specification evolution.</li>



<li>Observability – The player should expose operational metrics (time to first frame, stall count, latency, quality switches) and support event tracing per the MOQT qlog specification. Real-time delivery quality diagnostics (jitter, latency) are recommended for relay assessment and operational monitoring.</li>
</ul>



<h2 class="wp-block-heading" id="red5-s-role-in-enabling-use-of-moq-over-partner-cdns">Red5’s Role in Enabling Use of MOQ over Partner CDNs</h2>


<div class="wp-block-image">
<figure class="aligncenter size-full"><img alt="Red5 Cloud and CacheFly streaming solution overview" class="wp-image-184093" height="400" src="https://www.red5.net/wp-content/uploads/2025/09/Red5-Cloud-and-CacheFly-streaming-solution.png" title="Red5 Cloud and CacheFly streaming solution" width="800" /></figure>
</div>


<p>As of Q2 2026, the time has come for the beta testing ahead of MOQ Transport standard approval that will allow early adopters to quickly implement full-scale commercial operations. We can assume that any tweaks that might arise with finalization of the standard can be accommodated without disrupting what we and others are putting in place now.</p>



<p>As mentioned earlier, we’ve begun supplying global reach for MOQ operations over CacheFly’s CDN with an eye toward expanding the XDN-anchored MOQ CDN ecosystem over time. We’re employing XDN multiprotocol ingestion and <a href="https://www.red5.net/blog/what-is-transcoding/">transcoding</a> technology to enable MOQ-packaged payloads delivered from sources over Web, <a href="https://www.red5.net/srt-streaming/">SRT</a>, <a href="https://www.red5.net/zixi-protocol/">Zixi</a>, <a href="https://www.red5.net/rtmp-server/">RTMP</a>, <a href="https://www.red5.net/rtsp-protocol/">RTSP</a> or MPEG-TS streams to be ingested onto CDNs with multiple bitrate profiles matched to adaptive bitrate (ABR) ladders used in conventional streaming.&nbsp;</p>



<p>In CacheFly’s case the CDN is integrated with Red5-supplied MOQ relay nodes that enable multicasting of the payloads in real time to all session-targeted regions served by its network. Red5 Cloud MOQ customers’ end users will be served over access networks for playback by devices equipped with our MOQ player software.&nbsp;</p>



<p>MOQ Transport and Media Layer integrations with XDN Architecture on these and future partner CDNs make it possible for customers experimenting with MOQ to achieve the full range of multidirectional real-time streaming capabilities we’ve long supported with our use of WebRTC. <a href="https://www.red5.net/blog/keys-to-optimizing-end-to-end-latency-with-webrtc/">As explained at length in this blog</a> and elsewhere on our website, execution of WebRTC transport on XDN Architecture enables multidirectional streaming with end-to-end latencies registering at 250ms or less.&nbsp;</p>



<h2 class="wp-block-heading" id="red5-s-support-for-optimal-hybrid-use-of-moqt-with-webrtc">Red5’s Support for Optimal Hybrid Use of MOQT with WebRTC</h2>



<p>The need for such MOQ/WebRTC integrations reflects the fact that a fully standardized environment for working with MOQ remains a work in progress, including further clarification as to the range of use cases that MOQ will support. At this point, MOQ doesn’t support the echo and other noise cancellations essential to videoconferencing, and the mechanisms for bringing users’ video outputs into synchronized operation with the multicast MOQ streams have yet to be fully articulated in the MOQ Transport specifications.&nbsp;&nbsp;</p>



<p>By applying Red5’s mixer and transcoding solutions across the MOQ and WebRTC stream flows while enabling fallback to <a href="https://www.red5.net/hls-server/">HLS</a> when devices aren’t using browsers or plugins supporting the other protocols, XDN Architecture serves as the protocol-agnostic glue that maximizes streaming flexibility. Customers using CacheFly or any other CDNs we partner with can rely on MOQ instead of WebRTC for unidirectional real-time streaming at massive scales while seamlessly bringing WebRTC and our <a href="https://www.red5.net/truetime/meetings/">TrueTime Meetings™ </a>platform into play in any given session to enable synchronized real-time video calling among subsets of users.</p>



<p>This makes it easy, for example, to serve a mass audience with live-streamed sports payloads packaged in the MOQ Media Layer while adding seamlessly initiated and accessed watch party features supported by WebRTC. In fact, Red5 Cloud and Red5 Pro customers leveraging MOQ over these CDNs will have recourse to implementing any service strategy enabled by the wide range of real-time interactive streaming applications supported by all of our TrueTime Solutions™ and other innovations.&nbsp;</p>



<h2 class="wp-block-heading" id="conclusion">Conclusion</h2>



<p>The progress in MOQT standardization and support for payload configurations and playback over the MOQ Media Layer has set the stage for widescale testing in the runup to commercial rollouts. With no limit on the variety of streaming formats and players that can be developed using the framework embodied in the modularized Playa template, every segment of the vast video streaming ecosystem, from the mass consumer markets to the smallest enterprise and institutional niches, can now prepare to benefit from a standardized approach to next-generation streaming that removes the latency impediments of the past.</p>



<p>But there’s no denying it will take a good amount of time before support for MOQ-based streaming is as readily available as today’s HTTP-based streaming infrastructure. And it remains to be seen how far MOQ can go toward supporting seamless instantiation of real-time interactive video communications with unidirectional streaming on par with what can be done with Red5’s TrueTime Meeting<sup>™ </sup>or any other multidirectional video implementation over WebRTC on XDN infrastructure.</p>



<p>Our goal in throwing full support behind MOQ is to ensure that no customer has to await emergence of an optimal all-MOQ environment, if there ever is one, to achieve their goals with real-time streaming. Whatever the use case might be, the option to employ XDN Architecture through the Red5 Cloud service or use of Red5 SDKs at any scale is immediately at hand with the ability to launch testing with MOQ and eventually to transition to use of MOQ to whatever extent makes sense.&nbsp;</p>



<p>For now, with our multiprotocol streaming support extending to distribution over HTTP based protocols like HLS, DASH, LL-HLS and LL-DASH <a href="https://www.red5.net/case-studies/red5-cloud-and-cachefly-hls-streaming-solution-with-dvr-and-global-cdn-reach/">via our partnership with CacheFly</a>, XDN Architecture provides the protocol-agnostic platform that can be used to eliminate the operational silos of the past. And once ubiquitous availability of MOQ streaming infrastructure with support for tunable latencies makes it possible to meet that goal, XDN Architecture will continue to provide the optimal operational environment for getting the most out of MOQ.&nbsp;&nbsp;</p>
</div>
</div>
<p>The post <a href="https://www.red5.net/blog/consensus-on-a-moq-media-layer-player-framework/" rel="nofollow">Consensus on a MOQ Media Layer Player Framework Should Speed Market Adoption</a> appeared first on <a href="https://www.red5.net" rel="nofollow">Red5</a>.</p>
