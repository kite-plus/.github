<p align="center">
  <img src="https://raw.githubusercontent.com/kite-plus/.github/main/assets/readme/logo.svg" width="64" alt="Kite Plus 标志">
</p>

<h1 align="center">Kite Plus</h1>

<p align="center">围绕内容创作、发布与发现，构建开源工具。</p>

<p align="center">
  <a href="https://github.com/kite-plus/.github/blob/main/profile/README.md">English</a> · <strong>简体中文</strong>
</p>

我们做的每一个项目都出自同一个想法：你写下的内容应该保存在自己掌握的文件里，发布到哪里也应该一直由你决定。我们从 **Kite** 开始，它是一个以 Markdown 为基础的内容发布平台；面向内容聚合与发现的 **Explore** 还在规划中。

## Kite

**用 Markdown 写作，在浏览器里管理内容，把站点发布到你想去的地方。**

<a href="https://github.com/kite-plus/kite"><img src="https://raw.githubusercontent.com/kite-plus/kite/main/docs/assets/screenshot.png" width="100%" alt="用 Kite 搭建的站点，浅色与深色外观"></a>

Kite 兼顾 CMS 的写作体验与静态站点生成器的可迁移性。它是一个用 Go 编写的单文件程序，管理后台直接内置其中。

- **浏览器里的后台**：可视化编辑器直接读写 Markdown，一键切换源码，支持图片上传、标签、分类和草稿。
- **文件始终属于你**：内容就是磁盘上的 Markdown 文件。保存时只改写真正变化的部分，key 的顺序和注释原样保留，改个标题，`git diff` 只有一行。
- **发布方式由你选**：导出静态页面放到任意托管平台，在自己的服务器上运行站点，或者通过 Git 提交并推送。
- **无需额外安装**：后台、默认主题和 SQLite 驱动都已编译进这一个程序。

**[安装并启动 →](https://github.com/kite-plus/kite/blob/main/README.zh-CN.md#安装并启动)** · [代码仓库](https://github.com/kite-plus/kite) · [使用与开发参考](https://github.com/kite-plus/kite/blob/main/docs/reference.zh-CN.md) · [Apache 2.0 许可证](https://github.com/kite-plus/kite/blob/main/LICENSE)

> Kite 仍处于早期开发阶段，目前需要从源码安装，安装步骤已包含完整的后台。

## 工作方式

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/kite-plus/.github/main/assets/readme/workflow-dark.svg">
  <img src="https://raw.githubusercontent.com/kite-plus/.github/main/assets/readme/workflow.svg" width="100%" alt="一篇 Markdown 文章经过 kite 产生三种输出：kite build 把静态 HTML 写入 public/，kite run 在 localhost:1717 提供站点和后台，kite publish 通过 Git 提交并推送">
</picture>

Markdown 文件是唯一的真相源。Kite 在 `.kite/` 下维护的索引只是缓存：删掉、重建，得到的数据完全一样。

- `kite run` 启动站点（包含草稿），并在 `/admin/` 提供后台；每次保存都写回同一个文件。
- `kite build` 把站点渲染成静态页面并输出到 `public/`，可以部署到 GitHub Pages 或任意静态托管平台。
- `kite publish --all --push` 提交内容改动，并推送到你的 Git 远程仓库。

## 路线图

- **已完成**：静态构建、实时预览服务、浏览器后台、Git 发布（Kite M0–M4）。
- **Kite 接下来**：公开主题契约、`kite.lock` 与 `kitew` wrapper、基于 SQLite 的动态模式、WebAssembly 插件。
- **Explore**：内容聚合与发现平台，仍在规划中，尚未上线。

完整的里程碑列表见 [Kite 使用与开发参考](https://github.com/kite-plus/kite/blob/main/docs/reference.zh-CN.md#路线图)。

## 参与其中

- **反馈问题或提出想法**：[提交 Issue](https://github.com/kite-plus/kite/issues)，写明版本、环境和复现步骤。
- **贡献代码或文档**：先阅读[参与贡献](https://github.com/kite-plus/kite/blob/main/docs/reference.zh-CN.md#参与贡献)，提交 PR 前运行 `make check`。与设计文档冲突的改动，先改文档，再改代码。
- **了解设计**：[架构、主题与插件设计文档](https://github.com/kite-plus/kite/tree/main/docs/design)解释了 Kite 为什么这样设计。
