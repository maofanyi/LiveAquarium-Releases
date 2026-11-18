# Changelog

[简体中文](CHANGELOG.md) | [English](CHANGELOG.en-US.md)

## 1.16.0 (2026-11-18)

### Portrait groups and layouts

- Drag to group up to 3 portrait streams with shared chat, whole-group moves and member swaps.
- Watch up to 20 streams with portrait groups, or 16 ordinary streams. Groups persist in schemes and across restarts.
- The smallest groups temporarily reduce stream quality; enlarging, fullscreen or detaching restores your preference.
- A hands-on guide supports Later, Skip and interruption recovery. Closing a member removes its membership so it returns independently when added again.

### Independent recording

- Record up to 4 streams without transcoding, in 15-minute MKV segments.
- Remember the save location and name folders and recordings after the streamer and recording start time.
- Optional merging after normal recording stop is off by default. Failed merges preserve segments and can be retried.
- Recording failure notifications are on by default. Adjust both options in the recording panel. Closing the panel or removing a monitored room does not stop recording; exiting the app does.

### Configuration transfer

- Export and import follows, aliases, groups, transferable settings, recording preferences, monitoring schemes, layouts and portrait groups.
- Preview imports and apply them on the next startup with backup and rollback. Older follow-only files remain supported. Credentials, recordings and caches are excluded.

### Douyu playback and chat

- Restore and verify sign-in on startup without opening the account panel. Try available same-quality alternate streams after recognized input failures.
- Filter Douyu chat by user level in both the chat panel and overlay; messages with unknown levels remain visible.
- Choose the default chat color or blue, green, pink, gold, purple and red swatches, subject to platform permissions.

### Interface and stability

- Narrow rooms use a single-row floating bottom toolbar with fades and drag following. Long titles use an ellipsis and show the full name on hover.
- Audio focus uses a thicker border in the group member color. Fixes drag interruptions, target highlight layering, detaching and toolbar-related issues.

### Known issue

- Twitch may freeze video while audio continues after a quality change. This remains under investigation and is not fixed in this version.
