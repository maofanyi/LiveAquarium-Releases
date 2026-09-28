# Changelog

[简体中文](CHANGELOG.md) | [English](CHANGELOG.en-US.md)

## 1.12.1 (2026-09-28)

### Activity Lists and Quick Monitoring

- When the current audio-focus streamer has Douyu activity data, an independent activity section appears on the left with members, live status, and the current source.
- Activity lists support streamer name, room ID, full Chinese pinyin, and pinyin-initial search. Double-click or drag a member into the grid for temporary monitoring without changing the local streamer list.
- Activity streamers can be added to the local streamer list or a group; existing entries are deduplicated and show a consistent state.
- With multiple audio-focus rooms, only the current source is shown. A short first-use guide explains that activity data remains independent from local configuration.

### Caching, Filtering, and Interface

- Activity definitions and reusable room profiles use an independent persistent cache to reduce repeated requests when switching within one activity, while live status is still refreshed according to freshness rules.
- Activity sections and custom groups prefer the Online filter and automatically fall back to All when nobody is live, avoiding a misleading empty list.
- Custom-group headers remain visible while long lists scroll, activity refresh now shows progress, and list buttons, status icons, and the default activity icon use a consistent style.
- The global mute controls in the normal window and fullscreen navigation now share the same default, hover, and muted appearance.

### Notices and Privacy

- Adds controlled official notices with non-blocking banners and critical service dialogs. Content is plain text, and action buttons can open only allowlisted official HTTPS pages.
- Remote notices enforce response-size, item-count, version, time, frequency, caching, and per-process deduplication limits. Fetch or parse failures do not interrupt playback, update checks, or shutdown.
- Adds anonymous daily counters for activity sections and remote notices. Activity, room, streamer, message content, message IDs, and links are not collected.
