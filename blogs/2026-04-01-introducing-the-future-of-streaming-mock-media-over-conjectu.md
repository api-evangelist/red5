---
title: "Introducing the Future of Streaming: MOCK (Media Over Conjectural Kinetics)"
url: "https://www.red5.net/blog/introducing-mock-media-over-conjectural-kinetics/"
date: "Wed, 01 Apr 2026 11:27:41 +0000"
author: "Chris Allen"
feed_url: "https://www.red5.net/feed/"
---
<p>Our team has made tremendous progress with our <a href="https://www.red5.net/media-over-quic-moq/">MOQ</a> (Media over QUIC) implementation over the last year. Now that we are set to go live on <a href="https://www.red5.net/red5-cloud-low-latency-live-streaming-platform/">Red5 Cloud</a> with globally distributed MOQ relays running on <a href="https://www.red5.net/partners/cachefly/">CacheFly</a>, we are now ready to discuss what’s coming next. If any of you have followed how quickly we like to move and stay on top of the latest in <a href="https://www.red5.net/video-streaming-technology/">streaming technology</a>, you know that we simply can’t just stand still. </p>



<p>It so turns out that in parallel with our MOQ development and innovative AI VLM (Visual Language Model) work, we’ve been spending years of rigorous research where we&#8217;ve developed a completely new approach to video delivery. We’re proud to unveil MOCK — a groundbreaking protocol that redefines live media delivery using a surprisingly simple Newtonian physics equation.</p>



<p>We’ve spent years moving bits over UDP based protocols like RTP, and QUIC, but what wasn’t as obvious on the surface was that we weren’t looking at the actual movement of these bits. It turns out that applying one of the simplest physics concepts to bit delivery is the answer.&nbsp;</p>



<figure class="wp-block-embed is-type-video is-provider-youtube wp-block-embed-youtube wp-embed-aspect-16-9 wp-has-aspect-ratio"><div class="wp-block-embed__wrapper">

</div></figure>



<p class="has-text-align-center"><em>Watch my short talk on this topic on YouTube.</em></p>



<div class="wp-block-rank-math-toc-block" id="rank-math-toc"><h2>Table of Contents</h2><nav><ul><li><a href="#mock-a-kinetic-model-for-packetized-media-transport">MOCK: A Kinetic Model for Packetized Media Transport</a></li><li><a href="#the-conjectural-kinetics-layer-ckl">The Conjectural Kinetics Layer (CKL)</a></li><li><a href="#extremely-low-latency-through-predictive-momentum">Extremely Low Latency Through Predictive Momentum</a></li><li><a href="#entropy-normalized-bit-mass-enbm">Entropy-Normalized Bit Mass (ENBM)</a></li><li><a href="#transport-field-dynamics">Transport Field Dynamics</a></li><li><a href="#why-mock-matters">Why MOCK Matters</a></li><li><a href="#final-thoughts">Final Thoughts</a></li></ul></nav></div>



<h2 class="wp-block-heading" id="mock-a-kinetic-model-for-packetized-media-transport">MOCK: A Kinetic Model for Packetized Media Transport</h2>



<p>At the core of MOCK is a reinterpretation of packet transport not as discrete transmission events, but as continuous kinetic systems operating across a probabilistic network field.</p>



<p>Traditional protocols such as RTP over UDP or QUIC treat packets as atomic units subject to routing, buffering, and retransmission. MOCK instead models each media fragment as a <strong>kinetic particle</strong>, assigning it “mass” and “velocity” within a dynamically shifting transport medium.</p>



<p>This allows us to apply the classical equation:</p>



<p><strong>KE = ½mv²</strong></p>



<p>Where:</p>



<ul class="wp-block-list">
<li><strong>m (mass)</strong> represents the encoded complexity of a media fragment<br />(bitrate density × entropy coefficient × frame dependency index)</li>



<li><strong>v (velocity)</strong> represents propagation speed across the network<br />(inverse latency gradient adjusted for congestion vectors)</li>
</ul>



<h2 class="wp-block-heading" id="the-conjectural-kinetics-layer-ckl">The Conjectural Kinetics Layer (CKL)</h2>



<p>MOCK introduces a new transport abstraction: the <strong>Conjectural Kinetics Layer (CKL)</strong>, which sits above QUIC but below application-level streaming logic.</p>



<p>Rather than transmitting packets, CKL computes <strong>trajectory envelopes</strong> for media particles. These envelopes predict the most probable path a packet <em>would have taken</em>, allowing endpoints to reconstruct streams even before full delivery is completed.</p>



<p>Key components include:</p>



<ul class="wp-block-list">
<li><strong>Inertial Buffering</strong><strong><br /></strong> Replaces traditional jitter buffers by maintaining momentum continuity across frames. Instead of waiting for late packets, CKL extrapolates their expected arrival vector and pre-renders frames accordingly.</li>



<li><strong>Mass Rebalancing (MRB)</strong><strong><br /></strong> Dynamically adjusts packet “mass” to prioritize perceptual importance. I-frames carry significantly higher “mass” than B-frames, ensuring higher kinetic persistence under network turbulence.</li>



<li><strong>Velocity Shaping (VS)</strong><strong><br /></strong> Applies micro-adjustments to packet velocity based on real-time congestion gradients, effectively “steering” media flows through lower-resistance network paths.</li>
</ul>



<h2 class="wp-block-heading" id="extremely-low-latency-through-predictive-momentum">Extremely Low Latency Through Predictive Momentum</h2>



<p>One of the most significant breakthroughs in MOCK is its ability to achieve <strong>perceptual negative latency</strong>.</p>



<p>By combining CKL trajectory modeling with AI-assisted inference (leveraging our internal VLM pipelines), MOCK predicts the future state of a stream based on motion vectors, scene transitions, and user interaction patterns.</p>



<p>Instead of waiting for packets to arrive, clients reconstruct frames using projected kinetic states, then reconcile with actual packets upon arrival. This creates the effect of:</p>



<ul class="wp-block-list">
<li>Playback beginning before transmission completes.</li>



<li>Seamless continuity even under extreme packet loss.</li>



<li>Near-zero startup delay across global distances.</li>
</ul>



<p>The main issue we ran into in our initial tests is that to run the prediction algorithm on pure CPU proved to be too taxing, so instead we ended up rewriting the system to run on NVIDIA’s CUDA platform allowing us to predetermine the motion vectors, scene transitions, etc. with a dedicated GPU. Probably the most interesting thing about the use of the GPU in this way is that it also opens up the possibilities of running additional learning algorithms that can further optimize the predictions theoretically creating true negative latency.<br /><br />Once we had locked down our approach to our predictive algorithm, we then realized we needed to solve for stabilization of the stream state.</p>



<h2 class="wp-block-heading" id="entropy-normalized-bit-mass-enbm">Entropy-Normalized Bit Mass (ENBM)</h2>



<p>To stabilize the system, MOCK introduces <strong>Entropy-Normalized Bit Mass (ENBM)</strong>, a derived metric that ensures consistent kinetic behavior across varying codecs and resolutions.</p>



<p>ENBM is calculated as:</p>



<p>ENBM = (bits × entropy) / temporal coherence</p>



<p>This normalization allows MOCK to:</p>



<ul class="wp-block-list">
<li>Maintain consistent “mass” across <a href="https://www.red5.net/h264/">H.264</a>, <a href="https://www.red5.net/h-265-hevc/">HEVC</a>, <a href="https://www.red5.net/vp9-codec/">VP9</a>, <a href="https://www.red5.net/av1/">AV1</a>, and emerging codecs.</li>



<li>Optimize transport for both high-motion sports and low-motion talking heads.</li>



<li>Eliminate traditional ABR ladder switching in favor of continuous kinetic scaling.</li>
</ul>



<h2 class="wp-block-heading" id="transport-field-dynamics">Transport Field Dynamics</h2>



<p>Unlike static routing, MOCK treats the network as a <strong>dynamic field of resistance and acceleration</strong>.</p>



<p>Each edge node contributes to a shared field model that includes:</p>



<ul class="wp-block-list">
<li><strong>Congestion vectors</strong> (directional packet pressure).</li>



<li><strong>Latency gradients</strong> (spatial delay differentials).</li>



<li><strong>Thermal noise factors</strong> (randomized packet loss behavior).</li>
</ul>



<p>Using this model, CKL continuously recalculates optimal trajectories, allowing packets to “flow” rather than route.</p>



<p>This is particularly effective when deployed across globally distributed relays such as those running on CacheFly, where edge proximity and density amplify field accuracy.</p>



<figure class="wp-block-image size-large"><img alt="image" class="wp-image-226156" height="683" src="https://www.red5.net/wp-content/uploads/2026/04/image-1024x683.png" title="image" width="1024" /></figure>



<h2 class="wp-block-heading" id="why-mock-matters">Why MOCK Matters</h2>



<p>By reframing media delivery as a kinetic system rather than a transactional one, MOCK fundamentally changes how we think about real-time streaming:</p>



<ul class="wp-block-list">
<li>No more discrete packet retries — only trajectory correction.</li>



<li>No buffering — only momentum continuity.</li>



<li>No bitrate switching — only mass redistribution.</li>
</ul>



<p>The result is a system that behaves less like a network protocol and more like a physical law.</p>



<h2 class="wp-block-heading" id="final-thoughts">Final Thoughts</h2>



<p>MOCK represents a fundamental shift in how we think about media transport—not as packets moving through a network, but as energy propagating through a dynamic system. While it challenges long-held assumptions about delivery, buffering, and latency, the early results are difficult to ignore.</p>



<p>We’re actively exploring how MOCK can integrate alongside our existing MOQ and WebRTC workflows, and we look forward to sharing more as the research evolves.</p>



<p>As a <a href="https://www.red5.net/company/">company</a> dedicated to <a href="https://www.red5.net/open-source-live-streaming/">open-source development</a> and supporting our great community of developers, we plan to release our early research and implementation under an Apache 2 license. We are profoundly excited about welcoming your contributions to the future of MOCK. Stay tuned for the release in the near future, or get in touch sooner if you think you can contribute. </p>
<p>The post <a href="https://www.red5.net/blog/introducing-mock-media-over-conjectural-kinetics/" rel="nofollow">Introducing the Future of Streaming: MOCK (Media Over Conjectural Kinetics) </a> appeared first on <a href="https://www.red5.net" rel="nofollow">Red5</a>.</p>
