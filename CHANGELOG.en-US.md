# Changelog

[简体中文](CHANGELOG.md) | [English](CHANGELOG.en-US.md)

## 1.8.0 (2026-08-30)

### Anonymous Statistics and Reliability

- Added one daily anonymous usage summary. Ordinary errors stay aggregated locally; at most one clearly fatal error is sent automatically each day, and users can explicitly send a redacted report from Diagnostics.
- Statistics use a random installation identifier and the country/region code from Windows regional settings. Sentry may store the connection source IP to provide country/region information, but the app never sends room IDs, streamer names, titles, stream URLs, danmaku, Windows usernames, hardware identifiers, or full local paths.
- Unsent data is stored separately on the local device for up to 14 days; network, disk, or telemetry failures never block startup or playback.

### Playback Performance

- Cached catalog avatars to avoid repeated requests when switching tabs.
- Reduced background stream quality and throttled background playback while fullscreen, with automatic recovery after exiting fullscreen.
