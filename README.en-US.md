[简体中文](README.md) | [English](README.en-US.md)

<div align="center">
  <img src="assets/app-icon.png" width="96" alt="Live Aquarium app icon">
  <h1>Live Aquarium</h1>
  <p><strong>See multiple live rooms clearly in one window.</strong></p>
  <p>Windows 10 / 11 · Up to 16 rooms · Public rooms need no sign-in</p>
  <p>
    <a href="https://github.com/maofanyi/LiveAquarium-Releases/releases/latest"><strong>Download latest</strong></a>
    · <a href="https://maofanyi.github.io/LiveAquarium-Releases/">Illustrated guide</a>
    · <a href="#community-and-support">Community and feedback</a>
  </p>
</div>

![Live Aquarium multi-room monitoring interface](assets/product-overview-en.png)

Live Aquarium is a multi-platform live-stream monitoring app for Windows. It brings public rooms from Douyu, Bilibili, Douyin, Huya, Twitch, and YouTube into one workspace for following multiple streamers, tournaments, or live events at the same time.

> This is the official release repository for Live Aquarium. It contains installers, user documentation, and release verification data. The application source code is not published here.

## Highlights

| Multi-platform | Flexible layouts | Independent audio |
| --- | --- | --- |
| Paste a room URL to detect its platform and monitor up to 16 rooms | Use 1×1 through 4×4 layouts, a ready-to-fill 2×2 layout, drag-and-drop, and resizing | Use one audio focus or Shift-select multiple rooms, with independent volume and boost controls |
| **Live danmaku** | **Instant replay** | **Local-first** |
| Global and per-room controls; signed-in Douyu users can send plain-text chat | Keep roughly the latest 120 seconds, preview with audio, and export GIF or MP4 | Rooms and preferences stay local; Douyu session data is encrypted for the current Windows user |

Also included: manual import of Douyu follows, long-press tile moving, Ctrl + wheel tile resizing, independent volume, a mute-and-hide boss key, a custom title bar, fullscreen, live-status notifications, and saved monitoring presets. Eligible replay MP4 clips can export faster.

## Download and Install

Current version: **1.11.2**

| Channel | Installer | Notes |
| --- | --- | --- |
| [GitHub Releases](https://github.com/maofanyi/LiveAquarium-Releases/releases/latest) | `LiveAquarium-Setup-1.11.2.exe` | Full installer; recommended |
| [Gitee Releases](https://gitee.com/ntrmao/DouyuMonitor-Releases/releases) | `LiveAquarium-Setup-1.11.2-Lite.exe` | Lite installer; downloads and verifies `yt-dlp` when YouTube or Twitch is first used |

Requires 64-bit Windows 10 or Windows 11. A GPU with D3D11VA support and a current stable driver is recommended. Multiple simultaneous streams consume GPU, CPU, memory, and network bandwidth.

<details>
<summary><strong>Installer verification and Windows security notice</strong></summary>

The app does not currently have an Authenticode signature, so Windows may show an “Unknown publisher” warning on first launch. Download only from the official release pages above and verify SHA-256 when needed:

```powershell
Get-FileHash -Algorithm SHA256 '.\LiveAquarium-Setup-1.11.2.exe'
```

GitHub full installer:

```text
b7e11199d52150a3f6c50de46b9d3de7dc6f00a3cf54be2da002ab038b7e8be0
```

Gitee lite installer:

```text
ed5464c8457a0b5b5274974266b91a872c1faaa87ae285fa2523f8ecbc0d165f
```

</details>

## Get Started in Three Steps

1. Select **Add Streamer** and paste a supported live-room URL.
2. Choose or adjust a layout, then drag streamers into place.
3. Click a tile to switch audio focus; hold Shift to select multiple audio rooms.

Open **Settings → Personal account** to sign in through an isolated official Douyu page. Public-room viewing needs no sign-in. `Ctrl+Alt+B` mutes and hides the app; press it again or use the tray icon to restore the windows.

- [Illustrated online guide](https://maofanyi.github.io/LiveAquarium-Releases/)
- [Chinese text guide](docs/使用说明.md)
- [Illustrated offline guide](docs/user-guide-english.html) — download the repository and open it in a browser

The onboarding guide and keyboard shortcuts are also available under **Settings → Help**.

## Community and Support

<table>
  <tr>
    <td align="center" width="240">
      <strong>Official community and feedback</strong><br><br>
      <img src="assets/official-community-qq.png" width="180" alt="QR code for the official Live Aquarium QQ group"><br><br>
      QQ group: <code>796651138</code><br>
      Share feedback, report issues, or suggest improvements
    </td>
    <td align="center" width="240">
      <strong>Support the author</strong><br><br>
      <img src="assets/alipay-support-qr.png" width="180" alt="Alipay QR code for supporting the author"><br><br>
      Voluntary support only<br>
      No app features or commercial license are attached
    </td>
  </tr>
</table>

When reporting an issue, include the app version, reproduction steps, and a diagnostics summary you have reviewed. Do not publish accounts, passwords, cookies, verification codes, complete logs, or other personal information.

## Data and Privacy

<details>
<summary><strong>Local data, anonymous statistics, and replay-cache details</strong></summary>

- Settings are stored in `%LocalAppData%\DouyuMonitor\settings.json`.
- Logs are stored in `%LocalAppData%\DouyuMonitor\logs\monitor-YYYYMMDD.log`.
- Douyu session data and credentials needed to send chat are encrypted for the current Windows user and stored separately from ordinary settings; signing out clears them. The app does not request a platform password.
- Anonymous statistics use a randomly generated installation ID and send one daily summary of usage time, platform and layout features, and the country/region code from Windows regional settings. Unsent data is retained locally for up to 14 days.
- Ordinary errors remain aggregated locally. At most one clearly fatal error is sent automatically per installation per day, and users can explicitly send a redacted report from Diagnostics. Sentry may infer country/region from the connection source IP, but the app does not put the IP into telemetry fields.
- Room IDs, streamer names, live titles, stream URLs, danmaku, Windows usernames, hardware identifiers, full local paths, complete settings, and complete logs are not sent.
- Each playing room keeps roughly the latest 120 seconds of bounded compressed audio/video in process memory for local replay. The cache is never uploaded and is released when the app exits.
- Only preview and export create bounded temporary media files, which are cleaned afterward. GIF/MP4 output defaults to the app's `Highlights` folder and can be changed in Settings.
- Uninstalling does not automatically remove settings, logs, or exported media.

</details>

Do not repackage the installer, present modified builds as official, or distribute unofficial installers under the project name or icon without permission.
