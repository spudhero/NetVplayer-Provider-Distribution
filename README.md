# NetVplayer Provider Distribution

Official signed playback extensions and update indexes for the [NetVplayer macOS application](https://github.com/spudhero/NetVplayer).

## 中文

截至 **2026-11-20**，配套正式应用为 **NetVplayer 2.0.7（build 58）**，本轮已发布 Python 目录 **1.1.19** 和 Java 目录 **1.1.4**。组件面向 **macOS 14+ / Apple Silicon arm64**，支持用户自行提供的配置与服务；主程序、各扩展和 Android 完整环境分别使用独立版本号。

| Provider | 版本 | 最低主程序版本 |
| --- | --- | --- |
| [Java 目录](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.java-v1.1.4-arm64) | 1.1.4 | 1.0.0 |
| [JavaScript 目录](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.javascript-v1.1.2-arm64) | 1.1.2 | 1.0.0 |
| [Python 目录](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.python-v1.1.19-arm64) | 1.1.19 | 1.1.0 |
| [QuickJS 目录](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.quickjs-v1.1.2-arm64) | 1.1.2 | 1.0.0 |
| [可配置 Python](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.configurable.python-v1.1.0-arm64) | 1.1.0 | 1.0.0 |

应用通常自动安装和更新兼容组件。在“设置 → 扩展支持”选择“重新检查”可查看更新。最低主程序版本取自各包 manifest；可用组件以签名索引和兼容性检查为准。本轮原生扩展包含目录导航、请求签名、媒体地址提取和此前缺失的原生适配修复；具体变更与来源限制见[应用 2.0.7 发布说明](https://github.com/spudhero/NetVplayer/releases/tag/2.0.7)。稳定应用下载见[最新应用 Release](https://github.com/spudhero/NetVplayer/releases/latest)。

**Android 原版完整环境保持 [1.2.4](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/android-original-runtime-v1.2.4-arm64)**，通过独立的 [android/runtime/index.json](https://spudhero.github.io/NetVplayer-Provider-Distribution/android/runtime/index.json) 分发。它与 Mac 原生扩展分别选择，不自动互相回退。

- [stable/index.json](https://spudhero.github.io/NetVplayer-Provider-Distribution/stable/index.json)：官方签名更新索引，此次发布后包含 **30 项发行记录**，保留此前全部 28 项记录及吊销列表。
- [diagnostics/index.json](https://spudhero.github.io/NetVplayer-Provider-Distribution/diagnostics/index.json)：需主动选择的离线传输诊断通道，不由 stable 自动安装。
- [public-keys.json](public-keys.json)：公开验签密钥。Provider 实现源码与签名私钥保留在私有边界中。

本轮 Python 1.1.19／Java 1.1.4 复用已验收归档，公开下载的 SHA-256 与受测产物一致；其余表列组件保持原发行物。包和索引使用 Ed25519 签名；macOS 可执行文件使用 `community-adhoc` 配置，首次运行仍按系统提示授权。每个发行包使用上表链接中的独立 Git 标签，后续 README 更新不移动原标签或替换附件。

## English

As of **2026-11-20**, the companion application is **NetVplayer 2.0.7 (build 58)**. This release publishes Python catalog **1.1.19** and Java catalog **1.1.4** for **macOS 14+ / Apple Silicon arm64**. Components support configurations and services supplied by users. The application, each extension, and the complete Android runtime use independent versions.

| Provider | Version | Minimum application version |
| --- | --- | --- |
| [Java catalog](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.java-v1.1.4-arm64) | 1.1.4 | 1.0.0 |
| [JavaScript catalog](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.javascript-v1.1.2-arm64) | 1.1.2 | 1.0.0 |
| [Python catalog](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.python-v1.1.19-arm64) | 1.1.19 | 1.1.0 |
| [QuickJS catalog](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.quickjs-v1.1.2-arm64) | 1.1.2 | 1.0.0 |
| [Configurable Python](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.configurable.python-v1.1.0-arm64) | 1.1.0 | 1.0.0 |

The application normally installs and updates compatible components automatically. Use Settings → Verified Extensions → Check Again to check for updates. Minimum application versions come from package manifests; signed indexes and compatibility checks determine availability. These native updates include directory navigation, request signing, media extraction, and previously missing native adapters. See the [2.0.7 release notes](https://github.com/spudhero/NetVplayer/releases/tag/2.0.7) for changes and source limitations. Application downloads are available from the [latest application Release](https://github.com/spudhero/NetVplayer/releases/latest).

The **complete Android original runtime remains [1.2.4](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/android-original-runtime-v1.2.4-arm64)**, distributed through the separate [android/runtime/index.json](https://spudhero.github.io/NetVplayer-Provider-Distribution/android/runtime/index.json). Android original and Mac native execution are selected independently, without automatic fallback between them.

- [stable/index.json](https://spudhero.github.io/NetVplayer-Provider-Distribution/stable/index.json): the official signed update index, containing **30 release entries** after this publication, with all 28 previous entries and revocations preserved.
- [diagnostics/index.json](https://spudhero.github.io/NetVplayer-Provider-Distribution/diagnostics/index.json): a separate opt-in channel for offline transport diagnostics, never automatically selected from stable.
- [public-keys.json](public-keys.json): pinned public verification keys. Provider implementation sources and private signing keys remain private.

Python 1.1.19 and Java 1.1.4 reuse the accepted archives; anonymous downloads match their tested SHA-256 values. The other listed components retain their existing artifacts. Packages and indexes are Ed25519-signed; macOS executables use the `community-adhoc` profile, which is not Apple notarization. Each archive uses the separate Git tag linked in the tables. Later README updates preserve the original tags and release assets.

Content configurations, service accounts, and access rights are supplied by users. See the [project website](https://spudhero.github.io/NetVplayer/#providers) and [Provider SDK](https://github.com/spudhero/NetVplayer/blob/main/provider-sdk/README.md) for more information.
