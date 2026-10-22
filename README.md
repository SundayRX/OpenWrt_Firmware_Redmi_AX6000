# Redmi AX6000 固件

面向 **Redmi AX6000 / RB06、普通 110m 布局**的 ImmortalWrt 固件，提供双频 Wi-Fi、网页管理、网络加速和插件扩展。三套系统各有侧重，可按常用插件和操作习惯选择。

**仅适用于 RB06 普通 110m。** 小米 AX6000 / RA72、原厂分区和其他布局不能直接刷入。第一次安装请先看[设备与布局要求](docs/flashing.md#layout-comparison)。

## 选择版本

| 系统系列 | 适合谁 | 防火墙与插件 | 管理界面 |
|---|---|---|---|
| [21.02 / Linux 5.4](docs/21.02-5.4.md) | **以日常稳定使用为先，偏好轻量，不追新功能** | FW3 / iptables；OPKG 安装 IPK | LuCI 21.02，Argon 2.3.1 |
| [24.10 / Linux 6.6](docs/24.10-6.6.md) | **需要 FW4，并继续使用适配的 IPK 插件** | FW4 / nftables；OPKG 安装 IPK | LuCI 24.10，Argon 2.4.3 |
| [25.12 / Linux 6.12](docs/25.12-6.12.md) | **希望使用新功能、新内核与新版界面** | FW4 / nftables；APK 软件包 | LuCI 25.12，常规版本 Argon 3.0.0 |

**偏好轻量、以日常使用为主，选择 21.02；希望使用新功能，优先选择 25.12；需要保留 FW4 + IPK 插件组合，选择 24.10。** 21.02 的系统和插件生态较旧，25.12 使用 APK，不能直接安装 IPK。

三套系统均采用 MediaTek 厂商 Wi-Fi 驱动。以下下载区列出各系列可用版本及组件信息；预发布版本会在对应发行页标注。

## 下载

### 21.02 / Linux 5.4

<!-- AX6000:21.02-5.4:START -->
- [下载最新版本与查看说明](https://github.com/SundayRX/ImmortalWrt_Firmware_Redmi_AX6000/releases/tag/ImmortalWrt-21.02-Kernel-5.4-00f784b-20261022T064558Z) · 编译时间：2026-10-22 06:45:58 UTC
- [全部版本与历史固件](https://github.com/SundayRX/ImmortalWrt_Firmware_Redmi_AX6000/releases?q=%2221.02-5.4%22)

| 项目 | 此固件版本 |
| --- | --- |
| 系统 | ImmortalWrt 21.02-SNAPSHOT `r0-00f784b` |
| 内核 | Linux `5.4.284` |
| 布局 | 普通 110m（`immortalwrt-110m`） |
| Wi-Fi 驱动 | MediaTek `mt_wifi` `7.6.7.3` |
| LuCI | `git-23.360.32803-5829eab` |
| Argon | `2.3.1` |
<!-- AX6000:21.02-5.4:END -->

[功能与使用说明](docs/21.02-5.4.md) · [修复与改进](docs/21.02-5.4.md#fixes)

### 24.10 / Linux 6.6

<!-- AX6000:24.10-6.6:START -->
- 下载：本系列暂无可下载的发行。
- [全部版本与历史固件](https://github.com/SundayRX/ImmortalWrt_Firmware_Redmi_AX6000/releases?q=%2224.10-6.6%22)

| 项目 | 此固件版本 |
| --- | --- |
| 系统 | 暂无可下载版本 |
| 内核 | 暂无可下载版本 |
| 布局 | 暂无可下载版本 |
| Wi-Fi 驱动 | 暂无可下载版本 |
| LuCI | 暂无可下载版本 |
| Argon | 暂无可下载版本 |
<!-- AX6000:24.10-6.6:END -->

[功能与使用说明](docs/24.10-6.6.md) · [修复与改进](docs/24.10-6.6.md#fixes)

### 25.12 / Linux 6.12

<!-- AX6000:25.12-6.12:START -->
- [下载最新版本与查看说明](https://github.com/SundayRX/ImmortalWrt_Firmware_Redmi_AX6000/releases/tag/ImmortalWrt-25.12-Kernel-6.12-9f60bb6-20261022T021040Z) · 编译时间：2026-10-22 02:10:40 UTC
- [全部版本与历史固件](https://github.com/SundayRX/ImmortalWrt_Firmware_Redmi_AX6000/releases?q=%2225.12-6.12%22)

| 项目 | 此固件版本 |
| --- | --- |
| 系统 | ImmortalWrt 25.12-SNAPSHOT `r0-9f60bb6` |
| 内核 | Linux `6.12.112` |
| 布局 | 普通 110m（`immortalwrt-110m`） |
| Wi-Fi 驱动 | MediaTek `mt_wifi` `7.6.7.3` |
| LuCI | `26.289.10016~36e3f0d` |
| Argon | `3.0.0-r20261016` |
<!-- AX6000:25.12-6.12:END -->

[功能与使用说明](docs/25.12-6.12.md) · [修复与改进](docs/25.12-6.12.md#fixes)

打开发行页，核对系统、布局和插件版本，再下载 **Assets 中的固件 ZIP**。GitHub 自动生成的 `Source code (zip/tar.gz)` 不能刷机。

ZIP 名称包含系统、内核、设备、布局和编译时间，例如 `ImmortalWrt-21.02-5.4-Redmi_AX6000-110m-20261016T052802Z.zip`，末尾 `Z` 表示 UTC 时间。解压后按用途选择文件：

| 文件 | 用途 |
|---|---|
| `firmware/*squashfs-sysupgrade.bin` | 已有系统内更新或回退 |
| `firmware/*squashfs-factory.bin` | 配套 U-Boot 网页安装或恢复 |
| `bootloader/*-fip-fixed-parts.bin` | RB06 普通 110m 引导文件；初次安装或明确需要更新引导时使用 |
| `release-notes.md` / `packages.txt` | 本次固件说明 / 软件包版本清单 |
| `SHA256SUMS` | 核对包内文件完整性 |

刷写前完成[下载校验](docs/flashing.md#verify-download)。sysupgrade 和 factory 按入口选择其一，无需依次刷入；FIP 是独立引导文件，日常升级无需重刷。使用旧发行包时，先按其文件清单确认安装和恢复所需文件齐全。

## 功能与改进

各系列的说明按使用场景列出修复内容和效果，帮助了解无线连接、管理操作和系统升级有哪些改善。具体版本的组件与预装软件见对应发行说明和包内 `packages.txt`。

| 使用环节 | 改进重点 |
|---|---|
| 无线连接 | 关联兼容、密钥更新、无线配置保存及双频状态显示 |
| 管理页面 | 改善概览加载、配置保存、静态租约管理、下拉列表和升级后页面更新 |
| 网络与服务 | 完善加速设置生效、限速与访问控制配合，以及服务异常后的恢复 |
| 升级与恢复 | 完善备份与写入失败处理，保护跨系列配置切换，提供安装和恢复镜像 |

查看完整清单：[21.02](docs/21.02-5.4.md#fixes) · [24.10](docs/24.10-6.6.md#fixes) · [25.12](docs/25.12-6.12.md#fixes)。

## 默认设置

| 项目 | 默认值 |
|---|---|
| 管理地址 | `192.168.31.1` |
| 用户名 / 密码 | `root`；未预设密码，首次登录后设置 |
| 主机名 | `Redmi_AX6000` |
| 时区 | `Asia/Singapore`，UTC+8 |
| LAN IPv6 | 默认关闭；WAN IPv6 可独立配置 |

以上用于全新安装或不保留配置升级。保留配置时沿用兼容的已有设置，包括管理地址、密码和手动开启的 LAN IPv6；自定义版本以其发行说明为准。

首次使用按以下顺序设置：

1. 电脑用网线连接 LAN，自动获取 IP，打开 `http://192.168.31.1` 并设置管理员密码。
2. 根据接入方式配置 WAN：宽带拨号填写运营商提供的 PPPoE 账号密码，上级路由器分配地址时选择 DHCP。
3. 设置 Wi-Fi 名称与密码，确认有线和无线均能上网后，再按需启用插件。OpenClash 需要另行下载代理核心并导入自己的配置。

<a id="安装与使用"></a>

## 更新与回退

已有本仓库普通 110m 固件且管理页面可用时，优先从“系统 → 备份/升级”上传 `*squashfs-sysupgrade.bin`。**在 21.02、24.10、25.12 之间升级或回退，都取消保留配置**，安装后重新设置网络并安装匹配插件。不能整包恢复另一系列的备份。

系统无法启动时，使用同布局的 factory 镜像从配套 U-Boot 恢复。多布局引导请选择 **`immortalwrt-110m`**；`default` 是另一种布局。完整步骤、备份范围和旧版升级页面的处理办法见[安装、升级与恢复](docs/flashing.md)。

<a id="查看周边-wi-fi"></a>

## 常见使用问题

| 需求 | 操作与注意事项 |
|---|---|
| 给设备固定 IP | 在“网络 → DHCP/DNS → 静态租约”查看和编辑，离线设备也能管理；ARP 绑定是另一项功能，不能替代 DHCP 地址分配 |
| 查看周边 Wi-Fi | 在“状态 → 信道分析”选择频段，需要新结果时重新扫描。查看结果不自动更改工作信道；扫描会短暂占用无线资源 |
| 传输文件 | 使用“系统 → 文件传输”，或在 SFTP 客户端中填写路由器地址、SSH 端口（默认 22）和登录凭据；网页可执行操作取决于账号权限 |
| 升级后恢复插件 | 自行安装的插件程序通常需要重装；先确认 IPK/APK、防火墙和内核依赖，另行恢复插件数据 |
| 升级后仍显示旧页面 | 按 `Ctrl+F5`，必要时清除管理地址的站点缓存并重新登录，无需因此恢复路由器出厂设置 |
| 限速或统计与预期不同 | 检查硬件加速和代理是否影响该功能，再按所选系统的使用说明调整 |
| 对照固件新旧 | “状态 → 概览”显示版本及编译时间。下载页使用 UTC，路由器按设置的时区显示；时区不同不代表编译时间不同 |

信道图只展示当次扫描得到的信息。21.02 的图表展示范围为 HT20/40，不能用它判断邻居网络完整的 80/160 MHz 带宽。

<a id="反馈"></a>

## 来源与反馈

系统及组件来源与许可见[来源与许可](docs/sources-and-licenses.md)。

遇到问题可提交 [Issue](https://github.com/SundayRX/ImmortalWrt_Firmware_Redmi_AX6000/issues)，附完整 Release Tag 或固件版本、升级方式、是否保留配置，以及复现步骤。截图和日志请先去除密码、订阅地址、令牌等私密信息。

<!-- AX6000:DOCUMENTS:{"build":{"commit":"00f784b3b34f954e195ea3dbb3e0f9ec3711577d","run_attempt":"1","run_id":"39735037673"},"schema":1,"templates_sha256":"233bf4ad05698f4e817e001045da3bf7476c11a7db7c390b06d5cfec2d096912"} -->
