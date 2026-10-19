# Changelog

[简体中文](CHANGELOG.md) | [English](CHANGELOG.en-US.md)

## 1.15.0 (2026-10-20)

### Connections and playback

- Fixes Douyu chat and live data failing to update on some networks by automatically switching to an available connection when a connection fails.
- Improves fallback when a stream quality fails and window shutdown cleanup for more stable playback.
- Keeps the screen awake during playback and prompts previously signed-in users to sign in again when their platform session expires.

### Monitor layouts and alerts

- Adds independent portrait monitor layouts, with landscape and portrait schemes saved separately.
- Adds gift burst cards and animated borders, with a display toggle in Settings.
- Adds audio selection border styles with preview, save and cancel-to-restore controls.
- Gift alerts use estimated Fish Fin values. Gifts worth less than 1 Fish Fin per item do not contribute to alerts; gift statistics continue to record them.

### Chat and streamer list

- Adds Douyu @ replies in both the chat panel and the floating chat overlay.
- Improves Bilibili follow search, selected-follow syncing and carousel playback, and fixes carousel streamers disappearing from the online list.
- Shows the current broadcast duration in a dedicated row above chat and improves text-box focus clearing.
