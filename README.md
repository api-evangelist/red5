# Red5 (red5)

Red5 provides real-time streaming infrastructure for live video and audio delivery at scale. The Red5 Pro platform includes a media server, Stream Manager 2.0 for autoscaling cloud deployments, the Brew Mixer for composite stream production, a Restreamer for pushing live streams to social media and RTMP destinations, and WebRTC and native SDKs for browser and mobile integration. Red5 APIs enable programmatic management of streams, mixers, restreaming, cluster orchestration, and node monitoring. Use cases include live events, sports broadcasting, interactive video, gaming, surveillance, and enterprise communications requiring ultra-low latency streaming.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/red5/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/red5/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Live Streaming
- Media
- Real-Time
- RTMP
- Streaming
- Video
- WebRTC

## Timestamps

- **Created:** 2026-03-01
- **Modified:** 2026-05-19

## APIs

### Red5 Pro Server API

The Red5 Pro Server API is an HTTP-based REST API for gathering server, application, client, and stream statistics from a running Red5 Pro instance. It exposes endpoints for server health checks, application scope statistics, active stream enumeration and control, connection management, and log access. The API uses token-based authentication via the accessToken parameter and is accessible at port 5080 on any Red5 Pro server deployment. Developers can use it to monitor and manage live streaming infrastructure programmatically.

- **Human URL:** [https://www.red5.net/docs/red5-pro/development/api/server/red5-pro-server-api-overview/](https://www.red5.net/docs/red5-pro/development/api/server/red5-pro-server-api-overview/)
- **Base URL:** `http://localhost:5080/api/v1`

#### Tags

- Media
- Real-Time
- REST
- Server Management
- Streaming

#### Properties

- [Documentation](https://www.red5.net/docs/red5-pro/development/api/server/red5-pro-server-api-overview/)
- [API Reference](https://www.red5.net/docs/red5-pro/development/api/server/red5-pro-server-api/)
- [API Reference](https://www.red5.net/docs/red5-pro/development/api/server/red5-pro-server-applications-api/)
- [API Reference](https://www.red5.net/docs/red5-pro/development/api/server/red5-pro-server-streams-api/)
- [OpenAPI](openapi/red5-server-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/red5-server-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-server-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Red5 Pro Stream Manager 2.0 API

The Red5 Pro Stream Manager 2.0 API orchestrates autoscaling clusters of Red5 Pro streaming nodes across cloud infrastructure. It provides REST endpoints for managing live stream publishing and playback sessions, provisioning stream configurations, monitoring node metrics, managing cluster node lifecycles, and proxying WHIP and WHEP WebRTC connections. The API supports dynamic scaling of streaming capacity and is documented with an interactive Swagger UI available on each Stream Manager deployment.

- **Human URL:** [https://www.red5.net/docs/red5-pro/development/api/stream-manager-2-0/](https://www.red5.net/docs/red5-pro/development/api/stream-manager-2-0/)
- **Base URL:** `https://streammanager.example.com/as/v1`

#### Tags

- Autoscaling
- Cluster Management
- Media
- REST
- Streaming
- WebRTC
- WHEP
- WHIP

#### Properties

- [Documentation](https://www.red5.net/docs/red5-pro/development/api/stream-manager-2-0/)
- [API Reference](https://www.red5.net/docs/red5-pro/development/api/stream-manager-2-0/stream-manager-2-streams-api/)
- [API Reference](https://www.red5.net/docs/red5-pro/development/api/stream-manager-2-0/stream-manager-2-admin-api/)
- [API Reference](https://www.red5.net/docs/red5-pro/development/api/stream-manager-2-0/stream-manager-2-proxy-api/)
- [OpenAPI](openapi/red5-stream-manager-2-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/red5-stream-manager-2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-stream-manager-2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Red5 Pro Brew Mixer API

The Red5 Pro Brew Mixer API is a REST interface for the Cauldron Media Engine that enables dynamic composition of multiple live video and audio streams into a single mixed output stream. It supports creating and managing mixers, controlling input sources and layout, configuring composite output parameters, and producing mixed streams suitable for broadcasting. The Brew Mixer is used for multi-presenter live events and production-quality stream composition.

- **Human URL:** [https://www.red5.net/docs/red5-pro/development/api/mixer/brew-mixer-api/](https://www.red5.net/docs/red5-pro/development/api/mixer/brew-mixer-api/)
- **Base URL:** `https://api.example.com/brewmixer/2.0`

#### Tags

- Audio
- Composition
- Media
- Mixing
- REST
- Streaming
- Video

#### Properties

- [Documentation](https://www.red5.net/docs/red5-pro/development/api/mixer/brew-mixer-api/)
- [OpenAPI](openapi/red5-brew-mixer-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/red5-brew-mixer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-brew-mixer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Red5 Pro Restreamer API

The Red5 Pro Restreamer API controls live stream retransmission to external RTMP, RTMPS, SRT, and Zixi destinations including social media platforms like Facebook, YouTube, and Twitch. It accepts JSON-based provisions via POST requests to configure push and pull restreaming sessions from a Red5 Pro server. The API supports file-based pseudo-live restreaming of FLV and MP4 files as well as real-time forwarding of live ingest streams.

- **Human URL:** [https://www.red5.net/docs/red5-pro/development/api/restreamer/](https://www.red5.net/docs/red5-pro/development/api/restreamer/)
- **Base URL:** `https://api.example.com`

#### Tags

- Media
- REST
- Restreaming
- RTMP
- Social Media
- Streaming

#### Properties

- [Documentation](https://www.red5.net/docs/red5-pro/development/api/restreamer/)
- [API Reference](https://www.red5.net/docs/red5-pro/development/api/restreamer/red5-pro-restreamer-api-rtmp/)
- [OpenAPI](openapi/red5-restreamer-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/red5-restreamer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-restreamer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Red5 Pro WebRTC SDK

The Red5 Pro WebRTC SDK is a JavaScript library for integrating low-latency live streaming publish and subscribe capabilities into web applications. It supports WHIP for WebRTC publishing and WHEP for WebRTC playback, enabling sub-second latency streaming directly in the browser without plugins. The SDK provides APIs for managing stream sessions, configuring media constraints, handling connection lifecycle events, and interacting with Stream Manager for scalable deployments.

- **Human URL:** [https://www.red5.net/docs/red5-pro/development/sdks/red5-webrtc-sdk/](https://www.red5.net/docs/red5-pro/development/sdks/red5-webrtc-sdk/)
- **Base URL:** `https://api.example.com`

#### Tags

- JavaScript
- Media
- SDK
- Streaming
- WebRTC
- WHEP
- WHIP

#### Properties

- [Documentation](https://www.red5.net/docs/red5-pro/development/sdks/red5-webrtc-sdk/)
- [API Reference](https://www.red5.net/docs/red5-pro/development/sdks/red5-webrtc-sdk/red5-webrtc-sdk-api-documentation/)
- [Git Hub](https://github.com/red5pro/red5pro-webrtc-sdk)
- [N P M](https://www.npmjs.com/package/red5pro-webrtc-sdk)
- [AsyncAPI](asyncapi/red5-webrtc-streaming-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/red5-brew-mixer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-brew-mixer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/red5-restreamer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-restreamer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/red5-server-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-server-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/red5-stream-manager-2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-stream-manager-2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Red5 Core SDK

The Red5 Core SDK is a native client library for building real-time streaming applications on Linux, Windows, and macOS desktop platforms. It offers interfaces for server connection management, media capture and processing, audio and video source configuration, renderer control, and integration with Stream Manager for autoscaled deployments. Bindings are available for C++, Python, and other native environments.

- **Human URL:** [https://www.red5.net/docs/red5-pro/development/sdks/red5-core-sdk/](https://www.red5.net/docs/red5-pro/development/sdks/red5-core-sdk/)
- **Base URL:** `https://api.example.com`

#### Tags

- Desktop
- Linux
- Media
- Native
- SDK
- Streaming
- Windows

#### Properties

- [Documentation](https://www.red5.net/docs/red5-pro/development/sdks/red5-core-sdk/)
- [S D Ks](https://www.red5.net/live-streaming-sdks/)
- [Postman Collection](collections/red5-brew-mixer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-brew-mixer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/red5-restreamer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-restreamer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/red5-server-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-server-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/red5-stream-manager-2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-stream-manager-2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Red5 Pro iOS Streaming SDK

The Red5 Pro iOS Streaming SDK is a native iOS library for integrating real-time live streaming publish and subscribe capabilities into iOS applications. It supports H.264 video and AAC/Opus audio encoding, WebRTC-based streaming with WHIP/WHEP, and integration with Stream Manager for cluster-aware streaming deployments. Example code and testbeds are available on GitHub.

- **Human URL:** [https://www.red5.net/docs/red5-pro/development/sdks/](https://www.red5.net/docs/red5-pro/development/sdks/)
- **Base URL:** `https://api.example.com`

#### Tags

- iOS
- Media
- Mobile
- SDK
- Streaming
- Swift

#### Properties

- [Documentation](https://www.red5.net/docs/red5-pro/development/sdks/)
- [Git Hub](https://github.com/red5pro/streaming-ios)
- [Postman Collection](collections/red5-brew-mixer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-brew-mixer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/red5-restreamer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-restreamer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/red5-server-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-server-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/red5-stream-manager-2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-stream-manager-2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Red5 Pro Android Streaming SDK

The Red5 Pro Android Streaming SDK is a native Android library for integrating real-time live streaming publish and subscribe capabilities into Android applications. It supports H.264/H.265 video encoding, AAC audio, WebRTC-based streaming, and adaptive bitrate control. SDK examples and testbeds are available on GitHub for common streaming use cases.

- **Human URL:** [https://www.red5.net/docs/red5-pro/development/sdks/](https://www.red5.net/docs/red5-pro/development/sdks/)
- **Base URL:** `https://api.example.com`

#### Tags

- Android
- Java
- Media
- Mobile
- SDK
- Streaming

#### Properties

- [Documentation](https://www.red5.net/docs/red5-pro/development/sdks/)
- [Git Hub](https://github.com/red5pro/streaming-android)
- [Postman Collection](collections/red5-brew-mixer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-brew-mixer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/red5-restreamer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-restreamer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/red5-server-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-server-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/red5-stream-manager-2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/red5-stream-manager-2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/red5pro)
- [Website](https://www.red5.net/)
- [Documentation](https://www.red5.net/docs/red5-pro/)
- [GitHub Organization](https://github.com/red5pro)
- [GitHub Organization](https://github.com/Red5)
- [S D Ks](https://www.red5.net/live-streaming-sdks/)
- [Pricing](https://www.red5.net/pricing/)
- [Blog](https://www.red5.net/blog/)
- [Contact](https://www.red5.net/contact/)
- [J S O N L D Context](json-ld/red5-context.jsonld)
- [JSON Schema](json-schema/red5-stream-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/red5-restream-provision-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [OpenAPI](openapi/red5-server-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [OpenAPI](openapi/red5-stream-manager-2-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [OpenAPI](openapi/red5-brew-mixer-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [OpenAPI](openapi/red5-restreamer-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [AsyncAPI](asyncapi/red5-webrtc-streaming-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [JSON Structure](json-structure/red5-stream-structure.json)
- [Spectral Ruleset](rules/red5-rules.yml)
- [Vocabulary](vocabulary/red5-vocabulary.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
