# Redmi AX6000 固件

适用于 **Redmi AX6000 / RB06，普通 110m 布局**的 ImmortalWrt 固件，提供 21.02 和 24.10 两个系列。

**两个系列均只发布普通 110m 固件。** 小米 AX6000 / RA72 及其他机型不适用。首次安装或不确定设备布局时，先阅读[安装指南](docs/flashing.md#layout-comparison)。

## 选择版本

| 固件系列 | 系统与内核 | 防火墙 / 软件包 | 适合的需求 |
|---|---|---|---|
| [21.02 / 5.4](docs/21.02-5.4.md) | ImmortalWrt 21.02-SNAPSHOT / Linux 5.4 | FW3 / iptables / OPKG（IPK） | 沿用 FW3 插件和现有使用习惯 |
| [24.10 / 6.6](docs/24.10-6.6.md) | ImmortalWrt 24.10-SNAPSHOT / Linux 6.6 | FW4 / nftables / OPKG（IPK） | 使用较新的系统、内核及 FW4 插件；目前按**预发布版本**提供 |

两版均使用 MTK 厂商 Wi-Fi 驱动，提供中文管理界面与 Argon 主题。已有可用系统时，可先在同一系列内更新；跨系列切换前，请确认常用插件支持目标防火墙。

## 下载

### 21.02 / 5.4

<!-- AX6000:21.02-5.4:START -->
- [下载最新版本与查看说明](https://github.com/SundayRX/OpenWrt_Firmware_Redmi_AX6000/releases/tag/OpenWrt-21.02-Kernel-5.4-0f34b1a-20261015T141111Z) · 2026-10-15 14:11:11（编译） UTC
- [此系统的全部版本与历史固件](https://github.com/SundayRX/OpenWrt_Firmware_Redmi_AX6000/releases?q=%2221.02-5.4%22)
<!-- AX6000:21.02-5.4:END -->

[功能与使用说明](docs/21.02-5.4.md)

### 24.10 / 6.6

<!-- AX6000:24.10-6.6:START -->
- [下载最新版本与查看说明](https://github.com/SundayRX/OpenWrt_Firmware_Redmi_AX6000/releases/tag/OpenWrt-24.10-Kernel-6.6-66c329a-20261016T065356Z) · 2026-10-16 06:53:56（编译） UTC
- [此系统的全部版本与历史固件](https://github.com/SundayRX/OpenWrt_Firmware_Redmi_AX6000/releases?q=%2224.10-6.6%22)
<!-- AX6000:24.10-6.6:END -->

[功能与使用说明](docs/24.10-6.6.md)

1. 打开发行页，查看该版本的默认设置、预装插件及版本说明。
2. 下载附件中的固件 ZIP，按[校验说明](docs/flashing.md#verify-download)核对 SHA-256 后解压。
3. 已刷机用户使用 `firmware/` 中的 `*squashfs-sysupgrade.bin`，按[网页更新与回退](docs/flashing.md#web-upgrade)操作。

下载包示例：`ImmortalWrt-21.02-5.4-Redmi_AX6000-110m-20261016T052802Z.zip`。名称依次标明系统、内核、设备、布局和编译时间；末尾 `Z` 表示 UTC 时间。

ZIP 中的 `release-notes.md` 介绍该版本，`packages.txt` 列出预装软件及版本，`SHA256SUMS` 用于校验包内文件。历史附件按各自发行说明使用。**GitHub 的 Source code (zip/tar.gz) 是文档快照，不能用于刷机。**

## 默认设置

| 项目 | 默认值 |
|---|---|
| 管理地址 | `192.168.31.1` |
| 用户名 / 密码 | `root`；未预设密码，首次登录后自行设置 |
| 主机名 | `Redmi_AX6000` |
| 时区 | `Asia/Singapore`，UTC+8 |
| LAN IPv6 | 默认关闭；保留 WAN IPv6 |

以上用于全新安装或不保留配置升级，具体以下载版本的说明为准。保留配置升级沿用已有地址、密码和网络设置，包括用户手动开启的 LAN IPv6。

首次登录后设置管理密码，再配置上网和 Wi-Fi。预装插件不代表服务已经开启；OpenClash 需另行下载代理核心并导入自己的配置。

<a id="安装与使用"></a>

## 安装与回退

已安装本仓库固件且管理页面可用时，优先从“系统 → 备份/升级”上传 `*squashfs-sysupgrade.bin`。普通 110m 设备在 21.02 与 24.10 之间升级或回退时，**两个方向都取消保留配置**，完成后重新设置网络和 Wi-Fi，无需重新刷写 U-Boot。

- [网页更新与回退](docs/flashing.md#web-upgrade)：升级步骤、配置保留及插件恢复。
- [首次安装与恢复](docs/flashing.md#原厂首次安装)：原厂设备的安装准备和恢复方式。
- [来源与许可](docs/sources-and-licenses.md)：上游项目、版本识别及源码获取状态。

## 反馈

在 [Issues](https://github.com/SundayRX/OpenWrt_Firmware_Redmi_AX6000/issues) 中提供完整 Release Tag 或 ZIP 文件名、升级方式、是否保留配置，以及问题出现的步骤。提交截图或日志前，请移除密码、订阅地址、令牌和个人网络信息。

<!-- AX6000:DOCUMENTS:{"build":{"commit":"cbdf74306a6260f7df2520bdb77be0bc91b12dcc","run_attempt":"1","run_id":"38991015503"},"schema":1,"templates_sha256":"70d88b6fb228ce3b7a9cc1d82b6b1f37db92234cf154c36db99638555460e5b9"} -->
