# Changelog

[简体中文](CHANGELOG.md) | [English](CHANGELOG.en-US.md)

## 1.8.1 (2026-08-30)

### Anonymous Metrics and Privacy Transparency

- Added one-time anonymous installation and daily active counts so cumulative installations, daily users, and daily usage duration can be measured separately.
- Improved metric units, deduplication, and retry behavior. Ordinary errors are still uploaded only when the user explicitly sends a diagnostic report, with a clearly limited automatic path for serious failures.

### Language and Installation Experience

- First launch now selects Simplified Chinese or English from the Windows UI language without overriding an existing language preference.
- The installer now shows a bilingual anonymous statistics notice covering summary data, IP-based country or region reporting, prohibited data, and error-reporting behavior.
