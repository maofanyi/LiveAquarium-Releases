# Changelog

[简体中文](CHANGELOG.md) | [English](CHANGELOG.en-US.md)

## 1.9.2 (2026-09-09)

### YouTube Live Status Fix

- Fixed YouTube streams appearing offline while live. Live, scheduled, replay, and offline pages are now distinguished, while an indeterminate page preserves the existing status.

### YouTube Playback at Every Quality

- Fixed periodic stutter across YouTube HLS qualities by keeping separate audio and video tracks on independent decode inputs instead of amplifying segment-arrival and timestamp variation through one synthetic master playlist.
- Independent video tracks now catch up to the audio live edge after a late segment instead of treating the delayed position as a new playback origin, preventing A/V offset from accumulating over time.
- Long DVR playlists are trimmed to a stable live-edge window, preventing oversized manifests from blocking room activation and avoiding stalls caused by rebuilding thousands of dual-track segment mappings.
- YouTube chat batches are now paced within the polling interval instead of entering the danmaku lanes all at once.
- Added low-cardinality HLS relay diagnostics and a dual-input versus synthetic-master probe, with coverage for 360p30, 1080p60, audio-focus transitions, and sustained playback.

### Consistent Offline State

- Once a streamer is confirmed offline, quarantined player cards now match the room list, clear recovery notices, and avoid calling the failed player again.

### Anonymous Telemetry Reliability

- Fixed duplicate daily anonymous telemetry uploads when the delivery acknowledgement could not be persisted after midnight, with stronger startup snapshot and multi-process file-write protection.
