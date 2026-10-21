# 实验指南

## 一、创建文档项目

在 GitHub 创建仓库并克隆到本地，然后建立 `docs/`、`.github/workflows/` 目录及 `mkdocs.yml`。依次编写首页、项目说明、使用指南和接口说明。

## 二、本地构建与检查

安装 `requirements.txt` 中的依赖后运行：

```powershell
mkdocs build --strict
mkdocs serve
```

`mkdocs build --strict` 检查配置和文档引用，并在项目根目录生成 `site/`；`mkdocs serve` 启动本地预览服务器。

## 三、配置自动部署

工作流监听 `main` 分支中的文档、MkDocs 配置、依赖和工作流文件变更，也支持在 Actions 页面手动触发。构建成功后，Actions 将 `site/` 上传为 Pages 制品，后续部署作业发布该制品。

## 四、验证发布结果

1. 将项目文件提交并推送到 `main`。
2. 打开仓库的 Actions 页面，检查构建和部署作业均显示成功。
3. 打开 [线上文档站点](https://gu860.github.io/github-pages-lab/)，确认导航和各文档页可访问。
4. 更新首页标题并再次推送，确认线上页面随新工作流运行更新。

## 结果判定

当严格模式构建通过、GitHub Pages 部署任务成功，且线上站点能显示导航页时，本实验的自动构建和发布流程即验证完成。
