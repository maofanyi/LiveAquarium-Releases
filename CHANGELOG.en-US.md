# Changelog

[简体中文](CHANGELOG.md) | [English](CHANGELOG.en-US.md)

## 1.9.1 (2026-09-09)

### Live Detection and Automatic Recovery

- Monitored offline streamers are now detected through lightweight status checks and connected automatically when they go live. Initial startup establishes a baseline without sending false live notifications.
- Playback stall and error recovery is more robust, with normal stream endings distinguished from playback failures. Retry notices now clear once a streamer is confirmed offline.

### Replay Preview and Export Reliability

- Fixed preview failures for selections exactly 120 seconds long, and improved video timestamp handling, audio/video finalization, and export failure diagnostics so full-length videos export reliably.
- Rolling-cache diagnostics now report write rate, segments, eviction, disk quotas, and operation latency. A failed segment write can recover automatically at the next keyframe.

### List, Layout, and Danmaku Continuity

- Fixed the streamer list jumping to the top, flashing later rows, or reloading the selected card while dragging or adding a streamer, including under active filters.
- Active danmaku now continues through window resizing, sidebar expansion or collapse, and room-card size changes instead of being cleared and restarted.

### Interface and Playback Stability

- Strengthened video presentation resource switching and lifecycle protection to reduce display failures and crashes during refreshes, layout changes, and recovery.
- Shortened the anonymous-usage explanation, moved author information above it, and refined the add-preset action to better match the current interface.
