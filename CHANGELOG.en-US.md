# Changelog

[简体中文](CHANGELOG.md) | [English](CHANGELOG.en-US.md)

## 1.11.0 (2026-09-18)

### Douyu Account and Chat

- Added a Douyu account entry for signing in on an isolated official page, viewing account status and follows, and manually importing followed rooms into the local list.
- Signed-in users can send plain-text chat in Douyu rooms. Public-room viewing and chat display still work without signing in.

### Monitoring and Window Controls

- Added a boss key that mutes before hiding windows and can be reversed from a global hotkey or the tray. The custom title bar includes software fullscreen.
- Long-press to move monitored tiles and use Ctrl + wheel to resize them. The volume slider has a larger target, and each audible room can be adjusted independently.

### Replay and Getting Started

- Replay preview now has audio. Eligible MP4 selections export faster; other selections continue through precise export.
- Added interactive onboarding and improved layout transitions, drag feedback, and update notices.

### Reliability and Feedback

- Fixed replay generation when codec parameters change and duplicate daily-active telemetry across process restarts.
- Added feedback entry points in Settings and Diagnostics, with better redacted summaries, error categories, and feature usage metrics.
- When WebView2 Runtime is missing, the installer and Douyu sign-in and Douyin verification pages offer Microsoft's official download and installation; other features remain available.
