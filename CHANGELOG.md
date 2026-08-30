# 更新记录

[简体中文](CHANGELOG.md) | [English](CHANGELOG.en-US.md)

## 1.8.2（2026-08-30）

### 发行与下载

- GitHub 继续提供内置 yt-dlp 的完整安装包；Gitee 新增小于 100 MB 的轻量安装包，首次使用 YouTube 或 Twitch 时按需下载并校验解析组件。
- 应用内更新优先读取 GitHub 正式发行清单，并以 Gitee 镜像和旧 GitHub 仓库作为回退。

### 组件升级可靠性

- 内置、缓存和按需下载的 yt-dlp 统一使用固定版本与 SHA-256 校验；完整包与轻量包互换升级时可安全复用匹配文件并忽略过期副本。
- 发布流程分别记录完整包和轻量包校验值，并为 Gitee 自动维护受限的 yt-dlp 组件资产。
