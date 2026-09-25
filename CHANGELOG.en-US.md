# Changelog

[简体中文](CHANGELOG.md) | [English](CHANGELOG.en-US.md)

## 1.12.0 (2026-09-26)

### Search and Monitoring

- Added local room-list search by streamer name and room ID, including full Chinese pinyin and pinyin initials.
- Douyu carousel rooms can be monitored and played normally, are labeled as carousel content in lists and tiles, and do not trigger false live reminders.
- Single-room in-app live reminders can add the room when capacity is available. Windows system notifications are unchanged.
- Connected Douyu accounts can resolve available original-quality and high-frame-rate streams. Manual refresh, quality-specific refresh, and proactive renewal preserve the selected quality, with automatic fallback to anonymous playback when the authenticated session is unavailable.

### Audio and Fullscreen Controls

- Each monitored room now retains its own volume while the top-right control acts as master volume; single audio, multi-audio, and global mute remain consistent.
- Room toolbars auto-hide after inactivity, and F11 software fullscreen adds a top overlay for volume, audio mode, layout, and exit controls.
- Fixed background connection changes repeatedly waking fullscreen controls and exit hints, and confirmed Ctrl + wheel up enlarges tiles while wheel down shrinks them.

### Chat and Reading

- Added a hover +1 action to sendable Douyu text danmaku on the video, using the existing sign-in, rate-limit, send, and echo-confirmation path.
- The chat panel preserves the current reading view away from the bottom, counts new messages, and resumes a bounded latest-200 live view when requested.

### Reliability and Compatibility

- Fixed stale fullscreen background throttling that could leave video black, and safely degrades invalidated audio devices to mute without stopping video.
- Fixed saving 2×2 monitoring schemes and adding Douyin follow-page live links while preserving existing settings compatibility.
- User feedback now uses Sentry's native event association for redacted diagnostics without expanding the private-data boundary.
- Improved Douyu proactive refresh and playback recovery continuity, preserving the complete multi-audio selection and restoring secondary-room volume and audibility after source changes.
- Multi-platform requests now make a bounded attempt with the other address family when the preferred connection stalls, reducing room-add timeouts on broken IPv6 networks.
- Fixed display-area and related settings reverting to defaults after restart, and fixed overlapping empty-state messages when the chat panel has no rooms.
- Migrated the app name, default install directory, and user-data directory to Live Aquarium while preserving existing install locations and safely migrating saved settings.
- Added anonymous daily metrics for search, volume, danmaku +1, reminders, chat reading, fullscreen toolbar actions, danmaku speed, carousel time, and Douyu quality resolution/fallback. Room, account, cookie, quality, actual frame-rate, and stream-URL data are not collected.
