# GitHub Pages 自动部署实验

本项目用 MkDocs 把 Markdown 文档生成静态网站，再由 GitHub Actions 自动部署到 GitHub Pages。推送文档或构建配置后，无须手动上传生成文件，工作流会完成构建、制品归档和在线发布。

## 实验目标

- 创建包含多个页面的 MkDocs 文档项目。
- 编写 Actions 工作流，在代码推送时自动构建网站。
- 使用 GitHub Pages 托管构建结果，并检查线上页面。

## 发布流程

`main` 分支提交 → Actions 安装依赖 → MkDocs 检查并生成 `site/` → Pages 制品上传 → GitHub Pages 部署

## 快速开始

```powershell
python -m pip install -r requirements.txt
mkdocs serve
```

本地预览默认地址为 `http://127.0.0.1:8000/`。推送到 `main` 后，可在仓库的 **Actions** 页面查看自动部署结果。
