# Redmi AX6000 定制固件

为 **Redmi AX6000 / RB06** 提供由 SundayRX 维护的 ImmortalWrt 固件、下载入口和使用说明。下载前请确认设备型号、当前分区布局，以及对应 Release 的版本说明。

## 选择版本

| 版本线 | 系统与内核 | 防火墙 / 软件包 | 布局与引导 | 说明 |
|---|---|---|---|---|
| [21.02 / 5.4](docs/21.02-5.4.md) | ImmortalWrt 21.02-SNAPSHOT / Linux 5.4 | FW3 / iptables / OPKG（IPK） | 普通 110m 或 stock，下载包附匹配 FIP | 基于 hanwckf 配套；无线版本见对应 Release |
| [24.10 / 6.6](docs/24.10-6.6.md) | ImmortalWrt 24.10-SNAPSHOT / Linux 6.6 | FW4 / nftables / OPKG（IPK） | 仅普通 110m，不附引导 | **Pre-release**；基于 padavanonly，由 SundayRX 维护设备适配与功能定制 |

**仅适用于 Redmi AX6000 / RB06。** 小米 AX6000 / RA72、其他设备及 `ubootmod` 布局不能使用这里的普通 110m 固件。`stock` 表示分区布局，不表示可直接在小米原厂管理页面升级。

## 下载

### 21.02 / 5.4

<!-- AX6000:21.02-5.4:START -->
[浏览 21.02 / 5.4 固件与版本说明](https://github.com/SundayRX/OpenWrt_Firmware_Redmi_AX6000/releases?q=OpenWrt-21.02-Kernel-5.4)
<!-- AX6000:21.02-5.4:END -->

### 24.10 / 6.6

<!-- AX6000:24.10-6.6:START -->
[浏览 24.10 / 6.6 预发布固件与版本说明](https://github.com/SundayRX/OpenWrt_Firmware_Redmi_AX6000/releases?q=OpenWrt-24.10-Kernel-6.6)
<!-- AX6000:24.10-6.6:END -->

两条版本线分别使用固定 Tag **`OpenWrt-21.02-Kernel-5.4`** 和 **`OpenWrt-24.10-Kernel-6.6`**。每次更新在同一个 Release 中保留旧文件、追加新的一组附件；标题显示最新一组附件的生成时间，正文提供最新配置和历次构建入口。选择历史固件时，打开对应日期的说明，核对该次布局、功能与下载文件。此前独立 Tag 的历史版本仍可在[全部 Releases](https://github.com/SundayRX/OpenWrt_Firmware_Redmi_AX6000/releases)查找。

固件位于 Release 的 **Assets** 中。请从正文已完成的构建入口下载同组文件：`ax6000-版本线-布局-构建标识.zip` 和 `SHA256SUMS-构建标识.txt`，校验并解压后选择匹配的系统镜像。构建标识格式为 `YYYYMMDDTHHMMSSZ-run编号-a尝试编号`，其中日期是附件生成的 UTC 时间；选择时同时核对布局与完整标识。页面自动生成的 **Source code (zip/tar.gz)** 是本仓库文档的快照，不是可刷入固件，也不是固件完整源码。

每次构建的说明记录布局、无线版本和验证状态；同标识的 `packages-构建标识.txt` 列出实际预装软件包及版本，`build-info-构建标识.json` 提供该固件的配置摘要与镜像校验信息。ZIP 内仍使用 `packages.txt`、`build-info.json` 和 `SHA256SUMS`。具体内核小版本、默认地址和预装功能以所下载构建的记录为准；Release 顶部的最新配置不代表所有旧附件都采用相同配置。

## 默认设置

| 项目 | 默认值 |
|---|---|
| 管理地址 | `192.168.31.1` |
| 用户名 | `root` |
| 管理密码 | 未预设，首次使用时自行设置 |
| 主机名 | `Redmi_AX6000` |
| 时区 | `Asia/Singapore`，UTC+8 |

以上适用于使用默认配置启动的固件；所下载构建另有说明时以该次记录为准。保留配置升级会沿用已有地址、密码和其他设置。首次登录后请设置管理密码，再按自己的网络配置 WAN、LAN 和 Wi-Fi。

## 安装与使用

- [110m 与 stock 布局怎么选](docs/flashing.md#layout-comparison)：存储空间、插件容量、适用版本和布局迁移注意事项。
- [安装、升级与恢复](docs/flashing.md)：首次安装、系统内保留配置升级、跨版本迁移和 U-Boot 恢复。
- [21.02 / 5.4 说明](docs/21.02-5.4.md)：无线版本、镜像与配套引导、功能使用。
- [24.10 / 6.6 说明](docs/24.10-6.6.md)：与 padavanonly 原版的区别、FW4 功能和迁移说明。
- [来源、版权与源码获取状态](docs/sources-and-licenses.md)：上游项目、组件许可及对应源码安排。

固件可包含 OpenClash、访问控制、设备限速、DDNS、流量统计、系统监控、UPnP、网页终端等功能，具体预装项见对应构建说明。含有 OpenClash 界面的版本仍需在首次使用时另行下载代理核心；ProxyFence、WOLink 程序需要独立安装。

24.10 系列早期候选已有启动及 Wi-Fi 上线反馈，当前候选的完整功能、保留配置升级和长时间稳定性仍需验证，继续按预发布版本提供。使用前请阅读该次构建的已验证项目和限制，并保留可恢复的旧固件与备份。

## 反馈

在 [Issues](https://github.com/SundayRX/OpenWrt_Firmware_Redmi_AX6000/issues) 中提供 Release Tag、完整构建标识或 ZIP 文件名、设备型号、布局、升级入口、是否保留配置及可重复的现象。日志先移除密码、订阅地址、令牌和个人网络信息。
