# 来源与许可

[返回首页](../README.md) · [21.02 / 5.4](21.02-5.4.md) · [24.10 / 6.6](24.10-6.6.md) · [25.12 / 6.12](25.12-6.12.md)

固件基于 OpenWrt / ImmortalWrt 和多个上游项目，各组件原有的版权声明与许可继续适用。

## 查看版本和组件

在“状态 → 概览”查看已安装的固件版本及编译时间。发行页列出该版本的系统、内核、布局、Wi-Fi 驱动、LuCI 和 Argon；包内 `packages.txt` 列出实际预装软件包及版本。

反馈问题时，请提供完整固件版本和 Release Tag 或 ZIP 文件名。部分历史 Tag 使用 `OpenWrt-` 前缀，选择时仍以设备、布局及该次发行说明为准。

下载页的编译时间使用 UTC，路由器按设置的时区显示，例如 `UTC+8`；两者可能显示不同钟点，但对应同一时刻。

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
| 配套引导 | [hanwckf/bl-mt798x](https://github.com/hanwckf/bl-mt798x)，基于 MTK ATF / U-Boot。发行包的 `bootloader/` 提供 RB06 普通 110m FIP；24.10 / 25.12 配套来自 [20241115 发行版](https://github.com/hanwckf/bl-mt798x/releases/tag/20241115)。使用方法见[安装指南](flashing.md) |

固件保留 hanwckf 无线组件的版权声明，以及 padavanonly、chasey-dev 和其他上游项目的来源与许可。设备适配和管理功能的完善不改变原有组件的版权归属。

各系列的修复内容与使用效果见 [21.02](21.02-5.4.md#fixes)、[24.10](24.10-6.6.md#fixes) 和 [25.12](25.12-6.12.md#fixes) 的系统说明。

## 许可

ImmortalWrt 主源码的 `COPYING` 标注 [GPL-2.0-only](https://spdx.org/licenses/GPL-2.0-only.html)，其他组件按各自许可证发行。MTK 驱动、预编译程序和芯片固件也有各自的许可要求；使用和再次分发时，请保留版权声明并遵守对应条款。
