# NetVplayer Provider Distribution

Official signed playback extensions and update indexes for the [NetVplayer macOS application](https://github.com/spudhero/NetVplayer).

## 中文

2026-10-07 已正式发布五种 **Provider 1.1.0**，面向 **macOS 14+ / Apple Silicon arm64**。这些扩展支持用户自行提供的配置与服务；应用安装包、主程序壳源码和扩展分别更新。

| Provider | 版本 | 最低主程序版本 |
| --- | --- | --- |
| [Java 目录](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.java-v1.1.0-arm64) | 1.1.0 | 1.0.0 |
| [JavaScript 目录](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.javascript-v1.1.0-arm64) | 1.1.0 | 1.0.0 |
| [Python 目录](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.python-v1.1.0-arm64) | 1.1.0 | 1.1.0 |
| [QuickJS 目录](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.quickjs-v1.1.0-arm64) | 1.1.0 | 1.0.0 |
| [可配置 Python](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.configurable.python-v1.1.0-arm64) | 1.1.0 | 1.0.0 |

应用通常自动安装和更新兼容组件。在“设置 → 扩展支持”选择“重新检查”可查看更新。Python 目录 1.1.0 需要主程序至少 1.1.0；当前稳定应用 1.0.12 可继续使用已安装且兼容的历史版本。主程序壳 1.1.0 源码已公开，稳定应用下载见[最新应用 Release](https://github.com/spudhero/NetVplayer/releases/latest)。

- [stable/index.json](https://spudhero.github.io/NetVplayer-Provider-Distribution/stable/index.json)：官方签名更新索引，当前包含 22 项发行记录，保留全部 17 项历史版本。
- [diagnostics/index.json](https://spudhero.github.io/NetVplayer-Provider-Distribution/diagnostics/index.json)：需主动选择的离线传输诊断通道，不由 stable 自动安装。
- [public-keys.json](public-keys.json)：公开验签密钥。Provider 实现源码与签名私钥保留在私有边界中。

本次五包在本机从最新私有 Provider 源码构建和签名，公开下载的 SHA-256 与本机产物一致。包和索引使用 Ed25519 签名；macOS 可执行文件使用 `community-adhoc` 配置，首次运行仍按系统提示授权。

## English

All five **Provider 1.1.0** bundles were published on 2026-10-07 for **macOS 14+ / Apple Silicon arm64**. They support configurations and services supplied by users. Application bundles, the public shell source, and extensions have separate release versions.

| Provider | Version | Minimum application version |
| --- | --- | --- |
| [Java catalog](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.java-v1.1.0-arm64) | 1.1.0 | 1.0.0 |
| [JavaScript catalog](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.javascript-v1.1.0-arm64) | 1.1.0 | 1.0.0 |
| [Python catalog](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.python-v1.1.0-arm64) | 1.1.0 | 1.1.0 |
| [QuickJS catalog](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.catalog.quickjs-v1.1.0-arm64) | 1.1.0 | 1.0.0 |
| [Configurable Python](https://github.com/spudhero/NetVplayer-Provider-Distribution/releases/tag/provider-netvplayer.configurable.python-v1.1.0-arm64) | 1.1.0 | 1.0.0 |

The application normally installs and updates compatible components automatically. Use Settings → Verified Extensions → Check Again to check for updates. Python catalog 1.1.0 requires application 1.1.0; the current stable application 1.0.12 can continue using installed, compatible historical packages. The 1.1.0 shell source is public; application downloads are available from the [latest application Release](https://github.com/spudhero/NetVplayer/releases/latest).

- [stable/index.json](https://spudhero.github.io/NetVplayer-Provider-Distribution/stable/index.json): the official signed update index, currently containing 22 release entries with all 17 historical entries preserved.
- [diagnostics/index.json](https://spudhero.github.io/NetVplayer-Provider-Distribution/diagnostics/index.json): a separate opt-in channel for offline transport diagnostics, never automatically selected from stable.
- [public-keys.json](public-keys.json): pinned public verification keys. Provider implementation sources and private signing keys remain private.

All five bundles were built and signed locally from the latest private Provider source. Anonymous public downloads match the local archive SHA-256 values. Packages and indexes are Ed25519-signed; macOS executables use the `community-adhoc` profile, which is not Apple notarization.

Content configurations, service accounts, and access rights are supplied by users. See the [project website](https://spudhero.github.io/NetVplayer/#providers) and [Provider SDK](https://github.com/spudhero/NetVplayer/blob/main/provider-sdk/README.md) for more information.
