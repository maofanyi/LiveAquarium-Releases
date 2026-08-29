# Live Aquarium

[简体中文](README.md) | [English](README.en-US.md)

![Live Aquarium app icon](assets/app-icon.png)

> Multi-platform live monitoring

Live Aquarium is a multi-room live-stream monitoring app for 64-bit Windows 10 and Windows 11. It can display up to 16 publicly accessible live rooms in one window without requiring platform sign-in, making it useful for following multiple streamers, tournaments, or live events at the same time.

The current release supports Douyu, Bilibili, Douyin, Huya, Twitch, and YouTube.

> This is the official release repository for Live Aquarium. It contains installers, user documentation, and release verification data. The application source code is not published here.

## Download

Download the latest `LiveAquarium-Setup-1.7.1.exe` from [GitHub Releases](https://github.com/maofanyi/DouyuMonitor-Releases/releases/latest).

Current version: **1.7.1**

Only trust installers published by this repository. The application does not currently have an Authenticode code signature, so Windows may show an unknown-publisher warning on first launch. Verify the SHA-256 hash before running the installer.

```powershell
Get-FileHash -Algorithm SHA256 '.\LiveAquarium-Setup-1.7.1.exe'
```

Installer SHA-256:

```text
0085b1a75449d828d17a600c97e0fb98c5adbba038540738a8a7ef3052180c49
```

## Features

- Monitor up to 16 public live rooms at the same time.
- Add supported rooms by pasting a live-room link; the app detects the platform automatically.
- Drag, swap, and resize monitoring tiles, and save multiple monitoring presets.
- Use a single audio focus or Shift-select multiple rooms for simultaneous audio.
- Display real-time danmaku with global and per-room controls and Compact, Normal, and Max smart display strategies.
- Show live audience metrics, short-term audience-spike alerts, streamer-live notifications, and viewing-break reminders.
- Play streams through FFmpeg, D3D11VA, and WPF D3DImage. The installer includes the required .NET and FFmpeg runtimes.
- Store the room list, layout, volume, and window state locally without saving platform accounts, cookies, or passwords.

## User Guide

- [Illustrated online guide](https://maofanyi.github.io/DouyuMonitor-Releases/)
- [Chinese text guide](docs/使用说明.md)
- [Illustrated offline guide](docs/user-guide.html) — download the repository and open it in a browser

The same illustrated guide is available inside the app under **Settings → User Guide**.

The detailed guides are currently available in Chinese. English documentation will be expanded in future releases.

## System Requirements

- 64-bit Windows 10 or Windows 11.
- A GPU with D3D11VA support and a current stable graphics driver is recommended.
- Playing multiple live streams simultaneously consumes GPU, CPU, memory, and network bandwidth. Adjust the number of monitored rooms to match your system.

## Data and Privacy

- Settings: `%LocalAppData%\DouyuMonitor\settings.json`
- Logs: `%LocalAppData%\DouyuMonitor\logs\monitor-YYYYMMDD.log`
- Uninstalling the application does not automatically remove these settings or logs.
- The application does not store platform accounts, cookies, or passwords.

## Bug Reports and Security

When reporting an issue, include the application version, reproduction steps, and a diagnostics log that you have reviewed manually. Do not publish personal information or access credentials.

Do not repackage the installer, present modified builds as official, or distribute unofficial installers under the project name or icon without permission.

## Support the Author

If Live Aquarium is useful to you, you may voluntarily support the author through Alipay. Donations do not affect application functionality and do not constitute the purchase of a commercial license.

![Alipay QR code for supporting the author](assets/alipay-support-qr.png)
