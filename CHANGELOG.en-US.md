# Changelog

[简体中文](CHANGELOG.md) | [English](CHANGELOG.en-US.md)

## 1.14.0 (2026-10-11)

### Room online controls

- A new panel shows and controls Douyu watching connections, with up to 10 rooms online at once.
- Swap rooms in manually.
- Toggle online status directly from chat. Existing watching connections are preserved during normal stream handoffs.

### Chat and danmaku interaction

- Right-click chat messages to copy text or use +1. BV video IDs in chat and hovered danmaku can open the corresponding Bilibili video.
- Improves chat following and panel opening performance. Global mute preserves the selected chat source and reading position.

### Window and controls

- Pin the window on top and restore its size, position and maximized state.
- Press Space to toggle room fullscreen when the app has focus and you are not typing.
- Refines the room online entry, toggles and toolbar hints, and fixes missing icons on some computers.

### Playback and stability

- Muted background streams can use a lower bitrate and restore their original quality when you return, reducing background resource usage.
- Improves audio/video synchronization and stream handoffs, and fixes some stream-end status and load-failure recovery issues.
- Improves quality switching with result feedback and retries after failure, and reduces conflicts with automatic background stream refreshes.
- Preserves healthy playback when background stream refreshes fail, reduces repeated attempts and improves automatic recovery from stalls.
- Improves Bilibili session recovery at startup and follow-list refreshes, without treating a failed follow-list refresh as an expired login.
- Improves diagnostic logging and long-running stability, and moves diagnostic mode controls into the diagnostic log window.
