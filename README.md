# Kite Plus · 组织主页

这个仓库维护 [Kite Plus](https://github.com/kite-plus) 的 GitHub 组织主页。

- [中文主页](profile/README.md)：组织概览页默认展示的内容。
- [英文主页](profile/README.en.md)：供英文读者访问的版本。
- [品牌横幅](assets/readme/hero.svg)：使用 Kite 现有标志和蓝色，可直接编辑的静态 SVG。

## 文件结构

```text
.github/
├── README.md
├── profile/
│   ├── README.md
│   └── README.en.md
└── assets/readme/
    └── hero.svg
```

## 上线

将这些文件发布到 GitHub 上公开的 `kite-plus/.github` 仓库默认分支，GitHub 会读取 `profile/README.md` 作为组织主页。不需要构建、部署网站或配置 GitHub Actions。

主页图片和语言切换使用指向本仓库 `main` 分支的完整 URL，确保在组织概览页也能访问；若实际默认分支不是 `main`，需要一起调整链接。图片只有在文件上传后才会在线显示。

## 维护

1. 同步更新中英文主页中的项目介绍、状态和链接。
2. 项目能力以各项目当前文档为准；规划中的功能不能写成已交付功能。
3. 添加项目时提供真实仓库入口与简短用途，避免手动维护容易过期的星标数和版本号。
4. 修改横幅后检查桌面和手机宽度，以及深浅页面背景下的可读性。
5. 许可证以各项目自身的 `LICENSE` 为准，不在组织主页统一推定。

此仓库只承载展示内容，不设置组织级的 Issue 模板、PR 模板或贡献规则，避免影响其他项目的协作流程。
