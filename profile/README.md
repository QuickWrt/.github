# QuickWrt - OpenWRT 快速构建系统

![OpenWRT Version](https://img.shields.io/badge/OpenWRT-v24.10-blue.svg)
![License](https://img.shields.io/badge/License-GPLv3-green.svg)
![Platform](https://img.shields.io/badge/Platform-Linux%20x86_64%20%7C%20Rockchip-orange)

一个高度优化的 OpenWRT 自动化构建系统，支持快速编译和定制化固件生成。

## 🌟 特性

- **快速构建**: 支持预编译工具链加速，大幅缩短编译时间
- **多架构支持**: 支持 x86_64 和 Rockchip 架构
- **智能缓存**: 工具链缓存机制，避免重复编译
- **自动化流程**: 一键式构建，简化复杂配置过程
- **定制化配置**: 集成 ImmortalWRT 组件，增强设备兼容性
- **安全可靠**: 严格的错误处理和验证机制

## 📋 参数说明
| 参数          | 必选 | 说明           | 可选值               |
| ------------- | ---- | -------------- | -------------------- |
| `version`     | ✅   | OpenWRT 版本   | v24 (当前支持)       |
| `architecture`| ✅   | 目标架构       | x86_64, rockchip     |
| `build_mode`  | ❌   | 编译模式       | accelerated, normal, toolchain-only |

## 📁 项目结构

```
QuickWrt/
├── build.sh                 # 主构建脚本
├── scripts/                 # 构建子脚本
│   ├── 00-prepare_base.sh
│   ├── 01-prepare_package.sh
│   ├── 02-x86_64_target_only.sh
│   └── 02-rockchip_target_only.sh
├── OpenBox/                 # 定制化配置和软件包
│   ├── Config/
│   │   ├── X86_64.config
│   │   └── Rockchip.config
│   └── key.tar.gz
└── README.md
```

## 🔧 架构支持详情

### x86_64 架构
- **目标设备**: 标准 x86_64 硬件、虚拟机、软路由
- **特性**: 通用 x86 优化，支持大多数 x86 网卡和硬件

### Rockchip 架构
- **目标设备**: Rockchip 系列开发板（RK3568、RK3588 等）
- **特性**: 集成 ImmortalWRT 组件，增强设备兼容性

## ⚙️ 高级配置

### 自定义软件包

构建系统会自动集成 OpenBox 仓库中的定制化软件包。要添加自定义软件包：

1. 将软件包放入 `OpenBox/package/` 目录
2. 在对应的配置文件中启用相关选项
3. 重新执行构建脚本

#### Top Repositories

<a href="https://github.com/QuickWrt/QuickWrt">
  <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=QuickWrt&repo=QuickWrt&theme=buefy" />
</a>
<a href="https://github.com/QuickWrt/openwrt_packages">
  <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=QuickWrt&repo=openwrt_packages&theme=buefy" />
</a>
<a href="https://github.com/QuickWrt/QuickWrt-Scripts">
  <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=QuickWrt&repo=QuickWrt-Scripts&theme=buefy" />
</a>
<a href="https://github.com/QuickWrt/ZeroWrt">
  <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=QuickWrt&repo=ZeroWrt&theme=buefy" />
</a>
<br />
