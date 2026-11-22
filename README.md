# NetVplayer Provider Distribution

Official signed playback extensions and update indexes for the [NetVplayer macOS application](https://github.com/spudhero/NetVplayer).

## 中文

截至 **2026-11-22**，配套正式应用为 **NetVplayer 2.0.8（build 59）**。目前提供 Python 目录 **1.1.19** 和 Java 目录 **1.1.6**。组件面向 **macOS 14+ / Apple Silicon arm64**，支持用户自行提供的配置与服务。主程序、各扩展和 Android 完整环境分别使用独立版本号。

| Provider | 版本 | 最低主程序版本 |
| --- | --- | --- |
| [Java 目录](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.java-v1.1.6-arm64) | 1.1.6 | 1.0.0 |
| [JavaScript 目录](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.javascript-v1.1.2-arm64) | 1.1.2 | 1.0.0 |
| [Python 目录](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.python-v1.1.19-arm64) | 1.1.19 | 1.1.0 |
| [QuickJS 目录](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.quickjs-v1.1.2-arm64) | 1.1.2 | 1.0.0 |
| [可配置 Python](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.configurable.python-v1.1.0-arm64) | 1.1.0 | 1.0.0 |

应用通常自动安装和更新兼容组件。在“设置 → 扩展支持”选择“重新检查”可查看更新。最低主程序版本取自各包 manifest，可用组件以签名索引和兼容性检查为准。Java 1.1.6 改善韩迷、花生和有声小说配置的目录及播放。稳定应用下载及版本说明见[最新应用 Release](https://github.com/spudhero/NetVplayer/releases/latest)。

**Android 原版完整环境保持 [1.2.4](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/android-original-runtime-v1.2.4-arm64)**，通过独立的 [android/runtime/index.json](https://spudhero.github.io/NetVplayer-Provider-Distribution/android/runtime/index.json) 分发。它与 Mac 原生扩展分别选择，不自动互相回退。

- [stable/index.json](https://spudhero.github.io/NetVplayer-Provider-Distribution/stable/index.json)：官方签名更新索引，包含 **31 项发行记录**。
- [diagnostics/index.json](https://spudhero.github.io/NetVplayer-Provider-Distribution/diagnostics/index.json)：需主动选择的离线传输诊断通道，不由 stable 自动安装。
- [public-keys.json](public-keys.json)：公开验签密钥。Provider 实现源码与签名私钥保留在私有边界中。

Java 1.1.6 复用已实测的签名清单和 JAR，公开下载的 SHA-256 与验收归档一致。包和索引使用 Ed25519 签名。macOS 可执行文件使用 `community-adhoc` 配置，首次运行按系统提示授权。

## English

As of **2026-11-22**, the companion application is **NetVplayer 2.0.8 (build 59)**. Python catalog **1.1.19** and Java catalog **1.1.6** are available for **macOS 14+ / Apple Silicon arm64**. Components support configurations and services supplied by users. The application, each extension, and the complete Android runtime use independent versions.

| Provider | Version | Minimum application version |
| --- | --- | --- |
| [Java catalog](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.java-v1.1.6-arm64) | 1.1.6 | 1.0.0 |
| [JavaScript catalog](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.javascript-v1.1.2-arm64) | 1.1.2 | 1.0.0 |
| [Python catalog](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.python-v1.1.19-arm64) | 1.1.19 | 1.1.0 |
| [QuickJS catalog](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.quickjs-v1.1.2-arm64) | 1.1.2 | 1.0.0 |
| [Configurable Python](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.configurable.python-v1.1.0-arm64) | 1.1.0 | 1.0.0 |

The application normally installs and updates compatible components automatically. Use Settings → Verified Extensions → Check Again to check for updates. Minimum application versions come from package manifests. Signed indexes and compatibility checks determine availability. Java 1.1.6 improves browsing and playback for Hanquan, Huashu, and audiobook configurations. Application downloads and version notes are available from the [latest application Release](https://github.com/spudhero/NetVplayer/releases/latest).

The **complete Android original runtime remains [1.2.4](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/android-original-runtime-v1.2.4-arm64)**, distributed through the separate [android/runtime/index.json](https://spudhero.github.io/NetVplayer-Provider-Distribution/android/runtime/index.json). Android original and Mac native execution are selected independently, without automatic fallback between them.

- [stable/index.json](https://spudhero.github.io/NetVplayer-Provider-Distribution/stable/index.json): the official signed update index, containing **31 release entries**.
- [diagnostics/index.json](https://spudhero.github.io/NetVplayer-Provider-Distribution/diagnostics/index.json): a separate opt-in channel for offline transport diagnostics, never automatically selected from stable.
- [public-keys.json](public-keys.json): pinned public verification keys. Provider implementation sources and private signing keys remain private.

Java 1.1.6 reuses the tested signed manifest and JAR. Anonymous downloads match the verified archive SHA-256. Packages and indexes are Ed25519-signed. macOS executables use the `community-adhoc` profile and may require user approval on first launch.

Content configurations, service accounts, and access rights are supplied by users. See the [project website](https://spudhero.github.io/NetVplayer/#providers) and [Provider SDK](https://github.com/spudhero/NetVplayer/blob/main/provider-sdk/README.md) for more information.
