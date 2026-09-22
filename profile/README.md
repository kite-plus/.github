<p align="center">
  <img src="https://raw.githubusercontent.com/kite-plus/.github/main/assets/readme/logo.svg" width="64" alt="Kite Plus logo">
</p>

<h1 align="center">Kite Plus</h1>

<p align="center">Open-source tools for creating, publishing, and discovering content.</p>

<p align="center">
  <strong>English</strong> · <a href="https://github.com/kite-plus/.github/blob/main/profile/README.zh-CN.md">简体中文</a>
</p>

Everything we build starts from one idea: your writing belongs in plain files you own, and where you publish it should stay your choice. We start with **Kite**, a Markdown publishing platform. **Explore**, a place to discover what people publish, is planned.

## Kite

**Write in Markdown. Manage content in your browser. Publish on your terms.**

<a href="https://github.com/kite-plus/kite"><img src="https://raw.githubusercontent.com/kite-plus/kite/main/docs/assets/screenshot.png" width="100%" alt="A site built with Kite, in light and dark mode"></a>

Kite gives you the writing experience of a CMS and the portability of a static site generator. It is a single Go binary with the admin studio built in.

- **A studio in your browser.** A visual editor that reads and writes Markdown, with the source one click away, image uploads, tags, categories, and drafts.
- **Files that stay yours.** Content is plain Markdown on disk. Saving rewrites only what changed and keeps your key order and comments, so editing a title is a one-line `git diff`.
- **Publish your way.** Export static pages for any host, run the site on your own server, or commit and push through Git.
- **Nothing else to install.** The studio, the default theme, and the SQLite driver are compiled into the binary.

**[Install and start →](https://github.com/kite-plus/kite#install-and-start)** · [Repository](https://github.com/kite-plus/kite) · [Reference guide](https://github.com/kite-plus/kite/blob/main/docs/reference.md) · [Apache&nbsp;2.0](https://github.com/kite-plus/kite/blob/main/LICENSE)

> Kite is in early development. For now, install it from source; the steps include the full studio.

## How it works

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/kite-plus/.github/main/assets/readme/workflow-dark.svg">
  <img src="https://raw.githubusercontent.com/kite-plus/.github/main/assets/readme/workflow.svg" width="100%" alt="One Markdown file goes through kite to three outputs: kite build writes static HTML to public/, kite run serves the site and the studio on localhost:1717, and kite publish commits and pushes with Git">
</picture>

Your Markdown files are the source of truth. The index Kite keeps under `.kite/` is only a cache: delete it, rebuild, and the same data comes back.

- `kite run` serves your site, drafts included, with the studio at `/admin/`. Every save goes back into the same file.
- `kite build` renders static pages into `public/` for GitHub Pages or any static host.
- `kite publish --all --push` commits your content changes and pushes them to your Git remote.

## Roadmap

- **Done:** static builds, live serving, the browser studio, and Git publishing (Kite M0–M4).
- **Next for Kite:** a public theme contract, `kite.lock` with the `kitew` wrapper, a dynamic mode backed by SQLite, and WebAssembly plugins.
- **Explore:** a platform for aggregating and discovering published content. Planned, not launched yet.

The full milestone list lives in the [Kite reference guide](https://github.com/kite-plus/kite/blob/main/docs/reference.md#roadmap).

## Get involved

- **Report a bug or share an idea:** [open an issue](https://github.com/kite-plus/kite/issues) with your version, environment, and steps to reproduce.
- **Contribute code or docs:** read the [contributing notes](https://github.com/kite-plus/kite/blob/main/docs/reference.md#contributing) and run `make check` before you open a pull request. If a change conflicts with the design documents, update the documents first.
- **Read the design:** the [architecture, theme, and plugin documents](https://github.com/kite-plus/kite/tree/main/docs/design) explain why Kite works the way it does. They are written in Chinese.
