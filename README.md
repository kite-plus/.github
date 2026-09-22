# Kite Plus · 组织主页

这个仓库维护 [Kite Plus](https://github.com/kite-plus) 的 GitHub 组织主页。

- [英文主页](profile/README.md)：组织概览页默认展示的内容。
- [中文主页](profile/README.zh-CN.md)：供中文读者访问的版本。
- [品牌 Logo](assets/readme/logo.svg)：Kite 现有标志的纯填充版本，透明背景，裁掉了四周留白。
- [工作流示意图](assets/readme/workflow.svg)：浅色版本；[深色版本](assets/readme/workflow-dark.svg)会在 GitHub 深色主题下自动替换。

## 文件结构

```text
.github/
├── README.md
├── profile/
│   ├── README.md
│   └── README.zh-CN.md
└── assets/readme/
    ├── logo.svg
    ├── workflow.svg
    └── workflow-dark.svg
```

## 上线

将这些文件发布到 GitHub 上公开的 `kite-plus/.github` 仓库默认分支，GitHub 会读取 `profile/README.md` 作为组织主页。不需要构建、部署网站或配置 GitHub Actions。

主页图片和语言切换使用指向本仓库 `main` 分支的完整 URL，确保在组织概览页也能访问；若实际默认分支不是 `main`，需要一起调整链接。图片只有在文件上传后才会在线显示。

Kite 截图直接引用 `kite-plus/kite` 仓库的 `docs/assets/screenshot.png`，更新截图只需要改 kite 仓库。

## 维护

1. 同步更新中英文主页中的项目介绍、状态和链接。
2. 项目能力以各项目当前文档为准；规划中的功能不能写成已交付功能。路线图以 Kite 的 `docs/reference.md` 为准，里程碑完成后同步更新两份主页。
3. 添加项目时提供真实仓库入口与简短用途，避免手动维护容易过期的星标数和版本号。
4. 图片只写 `width`，不要同时写 `width` 和 `height`：外链图片同时带宽高时，GitHub 会给它加上灰色占位底色和圆角，透明 Logo 看起来就像带了阴影。
5. `workflow.svg` 与 `workflow-dark.svg` 是同一张图的两套配色，修改时一起改。图里只放命令、路径这类中英文通用的内容，说明文字写在 Markdown 里，两种语言共用一套图。
6. 修改 Logo 或示意图后，检查桌面和手机宽度，以及深浅页面背景下的可读性。
7. 许可证以各项目自身的 `LICENSE` 为准，不在组织主页统一推定。

此仓库只承载展示内容，不设置组织级的 Issue 模板、PR 模板或贡献规则，避免影响其他项目的协作流程。
