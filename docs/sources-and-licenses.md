# 来源与许可

[返回首页](../README.md) · [21.02 / 5.4](21.02-5.4.md) · [24.10 / 6.6](24.10-6.6.md)

固件基于 OpenWrt / ImmortalWrt 和多个上游项目，各组件原有的版权声明与许可继续适用。

## 识别已安装的版本

在“状态 → 概览”查看固件版本及编译时间。新发行的 `r0-xxxxxxx` 与 Release Tag 使用同一组七位固件编号；反馈问题时，同时提供 **完整 Release Tag 或 ZIP 文件名**，以便确定该次发行的软件配置。

例如 `OpenWrt-21.02-Kernel-5.4-1ced19c-20261014T101712Z` 表示系统系列 21.02、内核系列 5.4、固件编号 `1ced19c`，编译时间为 `2026-10-14 10:17:12 UTC`。Release 列表标题简写为 `21.02-5.4-1ced19c-20261014T101712Z`。

路由器概览中的编译时间按设置的时区显示。同一时刻在新加坡时区为 `18:17:12 UTC+8`，与下载页的 UTC 时间并不冲突。重新发布不会改变原编译时间；历史固件未记录该时间时，以其发行说明为准。

预装软件、默认设置和本次更新内容请查看所下载 Release 的说明与包内 `packages.txt`。

## 主要来源

| 部分 | 项目与说明 |
|---|---|
| 系统基础 | [OpenWrt](https://openwrt.org/) / [ImmortalWrt](https://github.com/immortalwrt/immortalwrt) 及其上游组件 |
| 21.02 / 5.4 | [hanwckf/immortalwrt-mt798x](https://github.com/hanwckf/immortalwrt-mt798x)，具体源码版本见对应发行说明 |
| 24.10 / 6.6 | 基于 [padavanonly/immortalwrt-mt798x-6.6](https://github.com/padavanonly/immortalwrt-mt798x-6.6)，增加普通 110m 与管理功能适配，见[功能差异](24.10-6.6.md#与-padavanonly-原版的区别) |
| LuCI 与软件包 | [ImmortalWrt LuCI](https://github.com/immortalwrt/luci)、[ImmortalWrt packages](https://github.com/immortalwrt/packages)、[OpenWrt routing](https://github.com/openwrt/routing)、[OpenWrt telephony](https://github.com/openwrt/telephony) 等 |
| Argon 主题 | [jerrykuku/luci-theme-argon](https://github.com/jerrykuku/luci-theme-argon) 及 ImmortalWrt 中的配套版本 |
| OpenClash | [vernesong/OpenClash](https://github.com/vernesong/OpenClash)，代理核心另行获取并适用其自身许可 |
| 配套引导 | [hanwckf/bl-mt798x](https://github.com/hanwckf/bl-mt798x)，基于 MTK ATF / U-Boot；参阅 [hanwckf 的使用说明](https://cmi.hanwckf.top/p/mt798x-uboot-usage/) |

固件保留 hanwckf 无线组件的版权声明，以及 padavanonly 和其他上游项目的来源与许可。设备适配和管理功能的完善不改变原有组件的版权归属。

## 许可与源码获取

ImmortalWrt 主源码的 `COPYING` 标注 [GPL-2.0-only](https://spdx.org/licenses/GPL-2.0-only.html)，其他组件按各自许可证发行。MTK 厂商组件包含源码、预编译程序和芯片固件，并非所有组件都有公开的完整源码；使用和再次分发时请遵守相应条款。

本仓库提供固件下载与使用说明，**目前尚未提供各次固件完整对应源码的下载入口**。GitHub 自动生成的 Source code 压缩包仅包含公开仓库文档，不是固件源码。

上游链接用于说明来源，不能代替具体固件的完整对应源码，包括适用许可证要求提供的相关编译和安装脚本。源码获取方式公布前，可在 [Issues](https://github.com/SundayRX/OpenWrt_Firmware_Redmi_AX6000/issues) 中提供完整 Release Tag 和 ZIP 文件名查询；该反馈入口不代表对应源码已交付。
