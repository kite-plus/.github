# Kite Plus · 组织主页

这个仓库维护 [Kite Plus](https://github.com/kite-plus) 的 GitHub 组织主页。

- [英文主页](profile/README.md)：组织概览页默认展示的内容。
- [中文主页](profile/README.zh-CN.md)：供中文读者访问的版本。
- [品牌 Logo](assets/readme/logo.svg)：Kite 现有标志的纯填充版本，透明背景，裁掉了四周留白。
- [产品地图](assets/readme/lifecycle.svg)：创作、发布、发现三个阶段与各项目的对应关系；[中文版](assets/readme/lifecycle.zh-CN.svg)供中文主页使用。

组织主页只做概览。各项目的特性、工作方式和路线图写在项目自己的 README 里，主页链接过去即可，例如 [Kite](https://github.com/kite-plus/kite)。

## 文件结构

```text
.github/
├── README.md
├── profile/
│   ├── README.md
│   └── README.zh-CN.md
└── assets/readme/
    ├── logo.svg
    ├── lifecycle.svg
    └── lifecycle.zh-CN.svg
```

## 上线

将这些文件发布到 GitHub 上公开的 `kite-plus/.github` 仓库默认分支，GitHub 会读取 `profile/README.md` 作为组织主页。不需要构建、部署网站或配置 GitHub Actions。

主页图片和语言切换使用指向本仓库 `main` 分支的完整 URL，确保在组织概览页也能访问；若实际默认分支不是 `main`，需要一起调整链接。图片只有在文件上传后才会在线显示。

## 维护

1. 同步更新中英文主页中的项目介绍、状态和链接。
2. 项目能力以各项目当前文档为准；规划中的功能不能写成已交付功能。项目状态变化时（例如 Kite 结束早期开发、Explore 启动），同时更新两份主页和两张产品地图。
3. 添加项目时提供真实仓库入口与简短用途，避免手动维护容易过期的星标数和版本号。
4. 图片只写 `width`，不要同时写 `width` 和 `height`：外链图片同时带宽高时，GitHub 会给它加上灰色占位底色和圆角，透明 Logo 看起来就像带了阴影。
5. `lifecycle.svg` 与 `lifecycle.zh-CN.svg` 布局相同、只有文字不同，修改时一起改。深浅色由 SVG 内部的 `prefers-color-scheme` 样式切换，不需要单独的深色文件。
6. 修改 Logo 或产品地图后，检查桌面和手机宽度，以及深浅页面背景下的可读性。
7. 许可证以各项目自身的 `LICENSE` 为准，不在组织主页统一推定。

此仓库只承载展示内容，不设置组织级的 Issue 模板、PR 模板或贡献规则，避免影响其他项目的协作流程。
