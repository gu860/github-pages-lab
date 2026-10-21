# GitHub Pages 自动部署实验

本仓库演示如何使用 MkDocs Material 编写静态文档，并通过 GitHub Actions 自动构建、发布到 GitHub Pages。

[![自动构建与部署](https://github.com/gu860/github-pages-lab/actions/workflows/deploy.yml/badge.svg?branch=main)](https://github.com/gu860/github-pages-lab/actions/workflows/deploy.yml)

- 文档站点：[https://gu860.github.io/github-pages-lab/](https://gu860.github.io/github-pages-lab/)
- 构建命令：`mkdocs build --strict`
- 本地预览：`mkdocs serve`
- 发布方式：向 `main` 分支推送文档、配置或依赖变更，由 Actions 上传站点制品并部署。

站点内容位于 `docs/`，站点配置位于 `mkdocs.yml`，CI/CD 工作流位于 `.github/workflows/deploy.yml`。
