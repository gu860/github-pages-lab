# 接口与发布信息

本示例发布的是静态 Markdown 文档，不提供后端业务 API。部署入口和可复现命令如下：

| 项目 | 配置 |
| --- | --- |
| 主分支 | `main` |
| 自动构建文件 | `.github/workflows/deploy.yml` |
| 站点配置文件 | `mkdocs.yml` |
| 内容目录 | `docs/` |
| 构建产物目录 | `site/` |
| 线上地址 | `https://gu860.github.io/github-pages-lab/` |

## 本地命令

```powershell
python -m pip install -r requirements.txt
mkdocs build --strict
mkdocs serve
```

推送到 `main` 或从 GitHub Actions 手动启动工作流即可触发在线发布。站点地址由 GitHub Pages 提供；构建与发布的执行记录保存在仓库的 Actions 页面中。
