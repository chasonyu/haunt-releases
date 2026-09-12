# Haunt Releases

Haunt 是一款适用于 macOS 的终端和 SSH 客户端，支持下拉终端、凭据库、双栏 SFTP、端口转发和加密备份恢复。

## 下载

前往 [最新版本](https://github.com/chasonyu/haunt-releases/releases/latest)，下载 `Haunt-<版本>-arm64.dmg`。

- 系统要求：**macOS 14 或更新版本、Apple Silicon（arm64）**。不支持 Intel Mac。
- 更新前请结束会话和文件传输、正常退出 Haunt，再将 DMG 中的应用拖入“应用程序”替换旧版。
- **从 v0.2.2 开始**，“设置 → 关于”或 Haunt 菜单支持应用内检查、下载、签名校验、安装和重启，无需 GitHub 登录或跳转网页。
- **v0.2.1 及更早版本需要手动下载并安装新版一次**，之后即可使用应用内安装功能。
- 默认不自动后台下载，由你决定何时更新；退出前会确认活动终端、SFTP 传输和端口转发。

## 安全与校验

当前免费发布包采用 ad-hoc 签名，未经 Apple Developer ID 签名或公证。macOS 可能阻止首次启动；请先确认下载来源，再按系统提示在“系统设置 → 隐私与安全性”中允许打开，无需全局关闭 Gatekeeper。

同时下载 `SHA256SUMS` 后，可在下载目录运行：

```sh
shasum -a 256 -c SHA256SUMS
```

校验和用于核验文件完整性，不代表 Apple 已认证发布者身份。

应用内更新额外验证 `appcast.xml` 和安装包的 Ed25519 签名，无需用户提供签名密钥。此签名独立于 Apple 公证。为了在 ad-hoc 签名下加载内嵌 Sparkle，Haunt 仅对自身放宽动态库验证，Hardened Runtime 仍开启，不修改系统 Gatekeeper。

本仓库仅用于分发安装包、校验文件和发布说明，不包含应用源码。GitHub 自动生成的 Source code 压缩包仅包含本仓库的说明文件；安装请下载 DMG。应用包内附第三方许可与组件清单。
