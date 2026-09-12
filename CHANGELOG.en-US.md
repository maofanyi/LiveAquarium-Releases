# Changelog

[简体中文](CHANGELOG.md) | [English](CHANGELOG.en-US.md)

## 1.10.1 (2026-09-12)

### Douyin Access Recovery

- Douyin background requests now pause when an interactive verification page is detected. An in-app official verification window can synchronize the protected session and recover rooms in both the catalog and monitoring area.
- Douyin danmaku now uses a realtime WebSocket connection instead of periodically polling the message-history endpoint.

### Diagnostics and Reliability

- Added privacy-safe telemetry dimensions for platform request failure type, fixed endpoint identifier, and HTTP status to distinguish network failures, access restrictions, rate limits, and response changes.
- Fixed monitored Douyin rooms remaining failed and ignoring manual refresh after verification was completed.
