# 来源、版权与源码获取状态

[返回首页](../README.md) · [21.02 / 5.4](21.02-5.4.md) · [24.10 / 6.6](24.10-6.6.md)

SundayRX 负责本项目的设备适配、功能定制、维护和发行。固件由多个上游项目及组件组成，各自的作者、版权声明和许可继续适用。24.10 系列的具体改动见[与 padavanonly 原版的区别](24.10-6.6.md#与-padavanonly-原版的区别)，其中的无线驱动核心和芯片固件继续使用上游配套。

## 主要来源

| 部分 | 来源与责任 |
|---|---|
| OpenWrt 基础 | [OpenWrt](https://openwrt.org/) 及其上游组件 |
| 21.02 / 5.4 系列 | [hanwckf/immortalwrt-mt798x](https://github.com/hanwckf/immortalwrt-mt798x) |
| 24.10 / 6.6 初始来源 | [padavanonly/immortalwrt-mt798x-6.6](https://github.com/padavanonly/immortalwrt-mt798x-6.6)，最初导入版本为 `ec9ef10efc65da1e6d1de4e2c043c0e13d08eed8`；本项目随后维护普通 110m 适配、管理功能与修正 |
| LuCI 与软件包 | [ImmortalWrt LuCI](https://github.com/immortalwrt/luci)、[ImmortalWrt packages](https://github.com/immortalwrt/packages)、[OpenWrt routing](https://github.com/openwrt/routing) 和 [OpenWrt telephony](https://github.com/openwrt/telephony) 等；实际组件及版本见所选构建的 `packages-构建标识.txt`，或该固件 ZIP 内的 `packages.txt` |
| Argon 主题 | [jerrykuku/luci-theme-argon](https://github.com/jerrykuku/luci-theme-argon) 及 ImmortalWrt 中的配套版本；本项目调整部分布局与版本显示 |
| 可选 OpenClash | [vernesong/OpenClash](https://github.com/vernesong/OpenClash)；代理核心另行获取并适用其自身许可 |
| 旧版配套引导 | [hanwckf/bl-mt798x](https://github.com/hanwckf/bl-mt798x)，基于 MTK ATF / U-Boot；[使用说明](https://cmi.hanwckf.top/p/mt798x-uboot-usage/)由原作者维护 |

上网时段控制、文件传输、NTP、UU 和 TurboACC 等界面及程序保留所继承项目的版权声明；本项目对其移植和后端适配不会改变原作者归属。MTK QoS 和基础无线管理同样保留已有来源。

这些链接用于说明来源。上游仓库当前分支与本项目各次构建并非同一版本，也不包含本项目的全部定制；上游地址不能代替该固件完整对应源码的获取入口。

## 许可范围

ImmortalWrt 主源码中的 `COPYING` 标注 [GPL-2.0-only](https://spdx.org/licenses/GPL-2.0-only.html)，同时明确其他许可也可能适用。Linux、U-Boot、LuCI、应用程序、库和其他组件分别依据自身许可发行，具体以相应版本中的许可证及版权声明为准。

MTK 厂商配套包含可阅读源码、预编译对象和芯片固件。源码树中保留某个文件，不等于该二进制组件的完整源代码已经公开，也不表示它与其他组件使用相同许可。厂商二进制的使用和再分发继续受其原有条款约束。

## 完整对应源码的当前状态

本公开仓库用于发布固件及使用文档，**当前没有公开完整的项目源码，也尚未提供各次构建固件的完整对应源码获取入口**。GitHub 自动生成的 Source code 压缩包仅为本发行仓库的文档快照，不代表该系列最新固件或每次历史构建的源码；Release 中的配置摘要、包清单和校验文件也不能代替完整对应源码。

涉及 GPL 的二进制分发需要按适用许可证安排完整对应源码。GPL v2 第 3 条中的对应源码范围包括相关源码及控制编译、安装所用的脚本；仅列出上游链接或保留私有副本不能替代具体发行版本的对应源码交付安排，详见[许可证原文](https://spdx.org/licenses/GPL-2.0-only.html)。

各次构建固件的完整对应源码提供方式仍待落实并公布，目前没有可用的完整下载地址。需要核对某个版本的来源或源码提供状态时，可在 [Issues](https://github.com/SundayRX/OpenWrt_Firmware_Redmi_AX6000/issues) 中注明 Release Tag，并提供构建标识或完整 ZIP 文件名；该联系入口本身不能替代对应源码提供安排。
