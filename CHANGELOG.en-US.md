# Changelog

[简体中文](CHANGELOG.md) | [English](CHANGELOG.en-US.md)

## 1.8.2 (2026-08-30)

### Distribution and Downloads

- GitHub continues to provide the complete installer with yt-dlp bundled. Gitee now provides a lite installer under 100 MB that downloads and verifies the extractor when YouTube or Twitch is first used.
- In-app update checks now prefer the official GitHub release manifest, with the Gitee mirror and legacy GitHub repository as fallbacks.

### Reliable Component Upgrades

- Bundled, cached, and on-demand yt-dlp runtimes now use one pinned version and SHA-256 verification; switching between full and lite installers safely reuses matching files and ignores stale copies.
- The release pipeline records separate hashes for the full and lite installers and maintains a restricted yt-dlp component asset for Gitee.
