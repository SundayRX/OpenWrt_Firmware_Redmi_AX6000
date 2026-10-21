# 来源与许可

[返回首页](../README.md) · [21.02 / 5.4](21.02-5.4.md) · [24.10 / 6.6](24.10-6.6.md) · [25.12 / 6.12](25.12-6.12.md)

固件基于 OpenWrt / ImmortalWrt 和多个上游项目，各组件原有的版权声明与许可继续适用。

## 识别已安装的版本

在“状态 → 概览”查看完整固件版本及编译时间。反馈问题时，请同时提供这些信息和 **完整 Release Tag 或 ZIP 文件名**，以便确定该次发行的软件配置；不要只凭七位短编号判断两个固件是否相同。

例如 `OpenWrt-21.02-Kernel-5.4-1ced19c-20261014T101712Z` 表示系统系列 21.02、内核系列 5.4、固件编号 `1ced19c`，编译时间为 `2026-10-14 10:17:12 UTC`。Release 列表标题简写为 `21.02-5.4-1ced19c-20261014T101712Z`。

路由器概览中的编译时间按设置的时区显示。同一时刻在新加坡时区为 `18:17:12 UTC+8`，与下载页的 UTC 时间并不冲突。重新发布不会改变原编译时间；历史固件未记录该时间时，以其发行说明为准。

预装软件、默认设置和本次更新内容请查看所下载 Release 的说明与包内 `packages.txt`。

## 主要来源

| 部分 | 项目与说明 |
|---|---|
| 系统基础 | [OpenWrt](https://openwrt.org/) / [ImmortalWrt](https://github.com/immortalwrt/immortalwrt) 及其上游组件 |
| 21.02 / 5.4 | 基于 [hanwckf/immortalwrt-mt798x](https://github.com/hanwckf/immortalwrt-mt798x)，无线、管理和升级功能的完善见[修复与改进](21.02-5.4.md#fixes) |
| 24.10 / 6.6 | 基于 [padavanonly/immortalwrt-mt798x-6.6](https://github.com/padavanonly/immortalwrt-mt798x-6.6)，普通 110m、无线及管理功能的完善见[修复与改进](24.10-6.6.md#fixes) |
| 25.12 / 6.12 | 基于 [chasey-dev/immortalwrt-mt798x-rebase](https://github.com/chasey-dev/immortalwrt-mt798x-rebase) 的 25.12 系列，RB06 普通 110m、厂商无线与管理功能的适配见[修复与改进](25.12-6.12.md#fixes) |
| 24.10 的 Wi-Fi 7.6.7.3 配套 | 使用 [hanwckf 的厂商驱动配套](https://github.com/hanwckf/immortalwrt-mt798x)，参考 [chasey-dev 的内核兼容适配](https://github.com/chasey-dev/immortalwrt-mt798x-rebase)；具体发行是否采用此配套以发行说明为准 |
| LuCI 与软件包 | [ImmortalWrt LuCI](https://github.com/immortalwrt/luci)、[ImmortalWrt packages](https://github.com/immortalwrt/packages)、[OpenWrt routing](https://github.com/openwrt/routing)、[OpenWrt telephony](https://github.com/openwrt/telephony) 等 |
| Argon 主题 | [jerrykuku/luci-theme-argon](https://github.com/jerrykuku/luci-theme-argon) 及 ImmortalWrt 中的配套版本 |
| OpenClash | [vernesong/OpenClash](https://github.com/vernesong/OpenClash)，代理核心另行获取并适用其自身许可 |
| 配套引导 | 新发行包的 `bootloader/` 提供 [hanwckf/bl-mt798x](https://github.com/hanwckf/bl-mt798x) 的 RB06 普通 110m FIP，基于 MTK ATF / U-Boot。24.10 / 25.12 的配套来自 [20241115 发行版](https://github.com/hanwckf/bl-mt798x/releases/tag/20241115)的固定 110m 文件；历史包是否附带引导，以其文件清单为准。操作见[安装指南](flashing.md) |

固件保留 hanwckf 无线组件的版权声明，以及 padavanonly、chasey-dev 和其他上游项目的来源与许可。设备适配和管理功能的完善不改变原有组件的版权归属。

各系列的具体改进分别列在 [21.02](21.02-5.4.md#fixes)、[24.10](24.10-6.6.md#fixes) 和 [25.12](25.12-6.12.md#fixes) 的版本说明中。按文中标注的固件版本和公开状态核对适用范围；后续更新不会自动进入已经下载的旧固件。

## 许可与源码获取

ImmortalWrt 主源码的 `COPYING` 标注 [GPL-2.0-only](https://spdx.org/licenses/GPL-2.0-only.html)，其他组件按各自许可证发行。MTK 厂商组件包含源码、预编译程序和芯片固件，并非所有组件都有公开的完整源码；使用和再次分发时请遵守相应条款。

本仓库提供固件下载与使用说明，**目前尚未提供各次固件完整对应源码的下载入口**。GitHub 自动生成的 Source code 压缩包仅包含公开仓库文档，不是固件源码。

上游链接用于说明来源，不能代替具体固件的完整对应源码，包括适用许可证要求提供的相关编译和安装脚本。源码获取方式公布前，可在 [Issues](https://github.com/SundayRX/OpenWrt_Firmware_Redmi_AX6000/issues) 中提供完整 Release Tag 和 ZIP 文件名查询；该反馈入口不代表对应源码已交付。
