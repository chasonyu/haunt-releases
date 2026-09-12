# Haunt Releases

Haunt 是一款适用于 macOS 的终端和 SSH 客户端，支持下拉终端、凭据库、双栏 SFTP、端口转发和加密备份恢复。

## 下载

前往 [最新版本](https://github.com/chasonyu/haunt-releases/releases/latest)，下载 `Haunt-<版本>-arm64.dmg`。

- 系统要求：**macOS 14 或更新版本、Apple Silicon（arm64）**。不支持 Intel Mac。
- 更新前请结束会话和文件传输、正常退出 Haunt，再将 DMG 中的应用拖入“应用程序”替换旧版。
- **从 v0.2.1 开始**，“设置 → 关于 → 检查更新”使用本公开仓库，不需要 GitHub 登录。更旧版本请手动下载并安装一次 v0.2.1 或更新版本。
- 更新检查仅提示新版本和下载入口，不会自动覆盖应用或中断连接。

## 安全与校验

当前免费发布包采用 ad-hoc 签名，未经 Apple Developer ID 签名或公证。macOS 可能阻止首次启动；请先确认下载来源，再按系统提示在“系统设置 → 隐私与安全性”中允许打开，无需全局关闭 Gatekeeper。

同时下载 `SHA256SUMS` 后，可在下载目录运行：

```sh
shasum -a 256 -c SHA256SUMS
```

校验和用于核验文件完整性，不代表 Apple 已认证发布者身份。

本仓库仅用于分发安装包、校验文件和发布说明，不包含应用源码。GitHub 自动生成的 Source code 压缩包仅包含本仓库的说明文件；安装请下载 DMG。应用包内附第三方许可与组件清单。
