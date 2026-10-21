# 项目说明

## 项目结构

```text
github-pages-lab/
├── .github/workflows/deploy.yml
├── docs/
│   ├── index.md
│   ├── about.md
│   ├── guide.md
│   └── api.md
├── mkdocs.yml
└── requirements.txt
```

`docs/` 保存 Markdown 页面，`mkdocs.yml` 定义站点名称、主题和导航；`requirements.txt` 固定 MkDocs Material 版本；工作流负责验证、打包和发布。

## 自动化边界

构建作业只读取仓库并上传静态站点制品；部署作业仅获得 Pages 发布和 OIDC 身份令牌权限。工作流使用 GitHub 提供的 Pages 制品接口，不需要向仓库推送部署分支。
