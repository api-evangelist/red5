# Red5 (red5)
Red5 is a real-time streaming media server platform that enables ultra-low latency live video and audio delivery at scale. The Red5 Pro platform provides a self-hosted or cloud-managed media server, Stream Manager for autoscaling across cloud providers, WebRTC and native SDKs, and REST APIs for managing streams, mixers, restreaming, and cluster orchestration. Red5 is used for live events, sports broadcasting, interactive video, gaming, surveillance, and enterprise communication applications.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/red5/refs/heads/main/apis.yml)

## Scope

- **Type:** Contract
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags:

 - Streaming, Media, Real-Time, WebRTC, RTMP, Video, Audio, Live Streaming

## Timestamps

- **Created:** 2026-03-18
- **Modified:** 2026-03-18

## APIs

### Red5 Pro Server API
The Red5 Pro Server API is an HTTP-based REST API for gathering server, application, client, and stream statistics from a running Red5 Pro instance. It exposes endpoints for server health checks, application scope statistics, active stream enumeration and control, and log access. The API uses token-based authentication and is accessible at port 5080 on any Red5 Pro server deployment. Developers can use it to monitor and manage live streaming infrastructure programmatically.

**Human URL:** [https://www.red5.net/docs/red5-pro/development/api/server/red5-pro-server-api-overview/](https://www.red5.net/docs/red5-pro/development/api/server/red5-pro-server-api-overview/)


#### Tags:

 - Streaming, Media, Real-Time, REST

#### Properties

- [Documentation](https://www.red5.net/docs/red5-pro/development/api/server/red5-pro-server-api-overview/)
- [APIReference](https://www.red5.net/docs/red5-pro/development/api/server/red5-pro-server-api/)
- [APIReference](https://www.red5.net/docs/red5-pro/development/api/server/red5-pro-server-applications-api/)
- [APIReference](https://www.red5.net/docs/red5-pro/development/api/server/red5-pro-server-streams-api/)
- [OpenAPI](openapi/red5-server-api-openapi.yml)

### Red5 Pro Stream Manager 2.0 API
The Red5 Pro Stream Manager 2.0 API orchestrates autoscaling clusters of Red5 Pro streaming nodes across cloud infrastructure. It provides REST endpoints for managing live stream publishing and playback sessions, provisioning stream configurations, monitoring node metrics, and proxying WHIP and WHEP WebRTC connections. The API supports dynamic scaling of streaming capacity and is documented with an interactive Swagger UI available on each Stream Manager deployment. It is the primary integration point for building scalable live streaming platforms on Red5 Pro.

**Human URL:** [https://www.red5.net/docs/red5-pro/development/api/stream-manager-2-0/](https://www.red5.net/docs/red5-pro/development/api/stream-manager-2-0/)


#### Tags:

 - Streaming, Media, Autoscaling, REST, WebRTC, WHIP, WHEP

#### Properties

- [Documentation](https://www.red5.net/docs/red5-pro/development/api/stream-manager-2-0/)
- [OpenAPI](https://www.red5.net/docs/red5-pro/development/api/stream-manager-2-0/stream-manager-2-openapi-api/)
- [APIReference](https://www.red5.net/docs/red5-pro/development/api/stream-manager-2-0/stream-manager-2-streams-api/)
- [APIReference](https://www.red5.net/docs/red5-pro/development/api/stream-manager-2-0/stream-manager-2-admin-api/)
- [APIReference](https://www.red5.net/docs/red5-pro/development/api/stream-manager-2-0/stream-manager-2-proxy-api/)
- [OpenAPI](openapi/red5-stream-manager-2-openapi.yml)

### Red5 Pro Brew Mixer API
The Red5 Pro Brew Mixer API is a REST interface for the Cauldron Media Engine that enables dynamic composition of multiple live video and audio streams into a single mixed output stream. It supports creating and managing mixers, controlling input sources and layout, and producing composite streams suitable for broadcasting. The API provides both v1 and v2 endpoints for mixer lifecycle management and image overlay control, making it useful for virtual events, live production, and multi-participant streaming scenarios.

**Human URL:** [https://www.red5.net/docs/red5-pro/development/api/mixer/brew-mixer-api/](https://www.red5.net/docs/red5-pro/development/api/mixer/brew-mixer-api/)


#### Tags:

 - Streaming, Media, Mixing, REST, Video, Audio

#### Properties

- [Documentation](https://www.red5.net/docs/red5-pro/development/api/mixer/brew-mixer-api/)
- [OpenAPI](openapi/red5-brew-mixer-api-openapi.yml)

### Red5 Pro Restreamer API
The Red5 Pro Restreamer API controls live stream retransmission to external RTMP, RTMPS, SRT, and Zixi destinations including social media platforms like Facebook and YouTube. It accepts JSON-based provisions via POST requests to configure push and pull restreaming sessions from a Red5 Pro server. The API supports file-based pseudo-live restreaming of FLV and MP4 files, as well as real-time forwarding of live ingest streams. It is commonly used for multi-destination broadcast workflows and content distribution to CDNs and social platforms.

**Human URL:** [https://www.red5.net/docs/red5-pro/development/api/restreamer/](https://www.red5.net/docs/red5-pro/development/api/restreamer/)


#### Tags:

 - Streaming, Media, RTMP, Restreaming, REST

#### Properties

- [Documentation](https://www.red5.net/docs/red5-pro/development/api/restreamer/)
- [APIReference](https://www.red5.net/docs/red5-pro/development/api/restreamer/red5-pro-restreamer-api-rtmp/)
- [OpenAPI](openapi/red5-restreamer-api-openapi.yml)

### Red5 Pro WebRTC SDK
The Red5 Pro WebRTC SDK is a JavaScript library for integrating low-latency live streaming publish and subscribe capabilities into web applications. It supports WHIP for WebRTC publishing and WHEP for WebRTC playback, enabling sub-second latency streaming directly in the browser without plugins. The SDK provides APIs for managing stream sessions, configuring media constraints, handling connection lifecycle events, and interacting with Stream Manager for scalable deployments. It is available via npm and CDN and includes extensive testbed examples on GitHub.

**Human URL:** [https://www.red5.net/docs/red5-pro/development/sdks/red5-webrtc-sdk/](https://www.red5.net/docs/red5-pro/development/sdks/red5-webrtc-sdk/)


#### Tags:

 - Streaming, Media, WebRTC, JavaScript, SDK, WHIP, WHEP

#### Properties

- [Documentation](https://www.red5.net/docs/red5-pro/development/sdks/red5-webrtc-sdk/)
- [APIReference](https://www.red5.net/docs/red5-pro/development/sdks/red5-webrtc-sdk/red5-webrtc-sdk-api-documentation/)
- [GitHub](https://github.com/red5pro/red5pro-webrtc-sdk)
- [NPM](https://www.npmjs.com/package/red5pro-webrtc-sdk)
- [AsyncAPI](asyncapi/red5-webrtc-streaming-asyncapi.yml)

### Red5 Core SDK
The Red5 Core SDK is a native client library that provides APIs for building real-time streaming applications on Linux, Windows, and macOS desktop platforms. It offers interfaces for server connection management, media capture and processing, audio and video source configuration, renderer control, and integration with Stream Manager for autoscaled deployments. The SDK is suited for applications requiring native performance such as broadcast encoders, kiosk systems, and professional production tools that need programmatic control over live streaming workflows.

**Human URL:** [https://www.red5.net/docs/red5-pro/development/sdks/red5-core-sdk/](https://www.red5.net/docs/red5-pro/development/sdks/red5-core-sdk/)


#### Tags:

 - Streaming, Media, SDK, Native, Desktop, Linux, Windows

#### Properties

- [Documentation](https://www.red5.net/docs/red5-pro/development/sdks/red5-core-sdk/)
- [SDKs](https://www.red5.net/live-streaming-sdks/)

## Common Properties

- [Website](https://www.red5.net/)
- [Developer Documentation](https://www.red5.net/docs/red5-pro/development/)
- [SDKs](https://www.red5.net/live-streaming-sdks/)
- [GitHub](https://github.com/red5pro)
- [Blog](https://www.red5.net/blog/)
- [Support](https://www.red5.net/contact/)
- [JSONLDContext](json-ld/red5-context.jsonld)
- [JSONSchema](json-schema/red5-stream-schema.json)
- [JSONSchema](json-schema/red5-restream-provision-schema.json)

## Maintainers

**FN:** API Evangelist

**Email:** info@apievangelist.com
