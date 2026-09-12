# Changelog

[简体中文](CHANGELOG.md) | [English](CHANGELOG.en-US.md)

## 1.10.2 (2026-09-12)

### Douyin Access Reliability

- Room-status checks now use a low-frequency room API instead of loading the full live page, reducing the chance that background refreshes trigger another security verification.
- Douyin sessions are encrypted for the current Windows user with a 12-hour lifetime; audience tasks wait quietly during verification and resume together after it succeeds.

### Verification Window and Installation

- Fixed the verification button doing nothing when an in-app update left WebView2 files incomplete; the app now detects this condition and falls back to the system browser.
- The installer now verifies critical WebView2 files and reports an incomplete installation instead of leaving the app unable to open verification.

### First Run and Diagnostics

- Fixed the getting-started guide being compressed into the top bar after a clean installation, which prevented users from operating the app.
- Improved anonymous error-report ordering and UI-thread handling so recent verification and installation failures are easier to identify.
