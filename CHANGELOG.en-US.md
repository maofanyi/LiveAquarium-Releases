# Changelog

[简体中文](CHANGELOG.md) | [English](CHANGELOG.en-US.md)

## 1.14.2 (2026-10-12)

### Douyu watching presence

- Adds a global automatic online switch in the Douyu watching panel. Choose automatic connections or manage room presence manually.
- Chat remains available when automatic online is disabled. Temporary connections close after sending; when all ten slots are occupied, chat borrows a connection and restores the original room first afterward.
- Improves Douyu watching-time reporting and connection management when changing quality, refreshing or switching accounts.

### Window controls

- Improves monitor resizing and reduces waits for other rooms to change quality.
- Fixes the streamer list unexpectedly opening when adjusting volume in F11 fullscreen.
