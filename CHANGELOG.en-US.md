# Changelog

[简体中文](CHANGELOG.md) | [English](CHANGELOG.en-US.md)

## 1.9.0 (2026-09-06)

### Replay Highlight GIFs and Videos

- The replay highlight panel now exports either a looping GIF or an MP4 video with audio. GIF ranges remain 2–10 seconds; video ranges can use the full 2–120 second rolling cache.
- Historical danmaku and the current title are optional layers; missing or failed layers safely fall back to a video-only GIF, with no separate PNG export.

### Local Cache and Reliability

- Keyframe-aligned rolling history reuses compressed packets already read by playback without another network stream, with a live tail, leases, per-room/global quotas, and startup cleanup.
- GIF generation uses an adaptive palette and bounds frame rate, dimensions, memory, and file size, with cancellation, explicit over-budget guidance, atomic saving, file copy, and no silent specification downgrade.

### Editing and Preview Experience

- The timeline now uses a thicker editing-style track with ticks, a playhead, unrestricted preview playback, and a separate Play Selection action. Moving the selected range no longer changes the current playback position.
- Preview playback reads directly from the frozen local cache and renders historical danmaku through the normal player overlay. Danmaku styling, size, outline, and motion scale correctly with the selected output resolution.

### Entry Points, Storage, and Help

- A scissors action and live-view context-menu entry open Replay Highlights. Settings can enable the feature and manage cache and export folders, which default beside the installed app for installer deployments.
- Onboarding and the offline user guide now explain Replay Highlights, with both Simplified Chinese and English guides included in the installer.

### Anonymous Feature Metrics

- Daily aggregates cover Replay Highlights, the side chat panel, and GIF/video generation outcomes to help assess reliability. Room IDs, streamer names, titles, danmaku content, and local paths are never uploaded.
