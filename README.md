# Red5

Red5 provides real-time streaming infrastructure for live video and audio delivery at scale. The Red5 Pro platform includes a media server, Stream Manager 2.0 for autoscaling cloud deployments, the Brew Mixer for composite stream production, a Restreamer for pushing live streams to social media and RTMP destinations, and WebRTC and native SDKs for browser and mobile integration. Red5 APIs enable programmatic management of streams, mixers, restreaming, cluster orchestration, and node monitoring.

**URL:** [https://raw.githubusercontent.com/api-evangelist/red5/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/red5/refs/heads/main/apis.yml)

## Tags

Live Streaming, Media, Real-Time, RTMP, Streaming, Video, WebRTC

## APIs

### [Red5 Pro Server API](openapi/red5-server-api-openapi.yml)
The Red5 Pro Server API is an HTTP-based REST API for gathering server, application, client, and stream statistics from a running Red5 Pro instance. It exposes endpoints for server health checks, application scope statistics, active stream enumeration and control, connection management, and log access.

**Base URL:** `http://localhost:5080/api/v1`

- [Documentation](https://www.red5.net/docs/red5-pro/development/api/server/red5-pro-server-api-overview/)
- [OpenAPI](openapi/red5-server-api-openapi.yml)

### [Red5 Pro Stream Manager 2.0 API](openapi/red5-stream-manager-2-openapi.yml)
The Red5 Pro Stream Manager 2.0 API orchestrates autoscaling clusters of Red5 Pro streaming nodes across cloud infrastructure. It provides REST endpoints for managing live stream publishing and playback sessions, provisioning stream configurations, monitoring node metrics, and proxying WHIP and WHEP WebRTC connections.

**Base URL:** `https://streammanager.example.com/as/v1`

- [Documentation](https://www.red5.net/docs/red5-pro/development/api/stream-manager-2-0/)
- [OpenAPI](openapi/red5-stream-manager-2-openapi.yml)

### [Red5 Pro Brew Mixer API](openapi/red5-brew-mixer-api-openapi.yml)
The Red5 Pro Brew Mixer API is a REST interface for the Cauldron Media Engine that enables dynamic composition of multiple live video and audio streams into a single mixed output stream. It supports creating and managing mixers, controlling input sources and layout, and producing composite streams suitable for broadcasting.

**Base URL:** `https://api.example.com/brewmixer/2.0`

- [Documentation](https://www.red5.net/docs/red5-pro/development/api/mixer/brew-mixer-api/)
- [OpenAPI](openapi/red5-brew-mixer-api-openapi.yml)

### [Red5 Pro Restreamer API](openapi/red5-restreamer-api-openapi.yml)
The Red5 Pro Restreamer API controls live stream retransmission to external RTMP, RTMPS, SRT, and Zixi destinations including social media platforms like Facebook, YouTube, and Twitch. It supports file-based pseudo-live restreaming and real-time forwarding of live ingest streams.

**Base URL:** `https://api.example.com`

- [Documentation](https://www.red5.net/docs/red5-pro/development/api/restreamer/)
- [OpenAPI](openapi/red5-restreamer-api-openapi.yml)

### Red5 Pro WebRTC SDK
The Red5 Pro WebRTC SDK is a JavaScript library for integrating low-latency live streaming publish and subscribe capabilities into web applications. It supports WHIP for WebRTC publishing and WHEP for WebRTC playback, enabling sub-second latency streaming directly in the browser.

- [Documentation](https://www.red5.net/docs/red5-pro/development/sdks/red5-webrtc-sdk/)
- [GitHub](https://github.com/red5pro/red5pro-webrtc-sdk)
- [NPM](https://www.npmjs.com/package/red5pro-webrtc-sdk)
- [AsyncAPI](asyncapi/red5-webrtc-streaming-asyncapi.yml)

### Red5 Core SDK
The Red5 Core SDK is a native client library for building real-time streaming applications on Linux, Windows, and macOS desktop platforms. It offers interfaces for server connection management, media capture and processing, audio and video source configuration, and integration with Stream Manager.

- [Documentation](https://www.red5.net/docs/red5-pro/development/sdks/red5-core-sdk/)
- [SDKs](https://www.red5.net/live-streaming-sdks/)

### Red5 Pro iOS Streaming SDK
The Red5 Pro iOS Streaming SDK is a native iOS library for integrating real-time live streaming publish and subscribe capabilities into iOS applications. It supports H.264 video and AAC/Opus audio encoding, WebRTC-based streaming with WHIP/WHEP, and integration with Stream Manager.

- [Documentation](https://www.red5.net/docs/red5-pro/development/sdks/)
- [GitHub](https://github.com/red5pro/streaming-ios)

### Red5 Pro Android Streaming SDK
The Red5 Pro Android Streaming SDK is a native Android library for integrating real-time live streaming publish and subscribe capabilities into Android applications. It supports H.264/H.265 video encoding, AAC audio, WebRTC-based streaming, and adaptive bitrate control.

- [Documentation](https://www.red5.net/docs/red5-pro/development/sdks/)
- [GitHub](https://github.com/red5pro/streaming-android)

## Capabilities

### Workflow Capabilities

| Capability | Description |
|-----------|-------------|
| [Live Streaming](capabilities/live-streaming.yaml) | Stream lifecycle management including publishing, monitoring, and control operations (8 MCP tools) |

### Shared Definitions

| File | API |
|------|-----|
| [server-api.yaml](capabilities/shared/server-api.yaml) | Red5 Pro Server API |

## Artifacts

| Type | File |
|------|------|
| OpenAPI | [Server API](openapi/red5-server-api-openapi.yml) |
| OpenAPI | [Stream Manager 2.0 API](openapi/red5-stream-manager-2-openapi.yml) |
| OpenAPI | [Brew Mixer API](openapi/red5-brew-mixer-api-openapi.yml) |
| OpenAPI | [Restreamer API](openapi/red5-restreamer-api-openapi.yml) |
| AsyncAPI | [WebRTC Streaming](asyncapi/red5-webrtc-streaming-asyncapi.yml) |
| JSON Schema | [Stream](json-schema/red5-stream-schema.json) |
| JSON Schema | [Restream Provision](json-schema/red5-restream-provision-schema.json) |
| JSON Structure | [Stream Structure](json-structure/red5-stream-structure.json) |
| JSON-LD Context | [Red5 Context](json-ld/red5-context.jsonld) |
| Spectral Rules | [Red5 Rules](rules/red5-rules.yml) |
| Vocabulary | [Red5 Vocabulary](vocabulary/red5-vocabulary.yml) |

## Examples

- [List Streams](examples/red5-list-streams-example.json)
- [Create Provision](examples/red5-create-provision-example.json)

## Common Properties

- [Website](https://www.red5.net/)
- [Documentation](https://www.red5.net/docs/red5-pro/)
- [GitHub Organization](https://github.com/red5pro)
- [GitHub Organization](https://github.com/Red5)
- [SDKs](https://www.red5.net/live-streaming-sdks/)
- [Pricing](https://www.red5.net/pricing/)
- [Blog](https://www.red5.net/blog/)
- [Contact](https://www.red5.net/contact/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
