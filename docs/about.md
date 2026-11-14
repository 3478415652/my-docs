# 关于本项目

## 项目介绍

本项目是一个使用 MkDocs Material 构建的个人技术文档网站。

网站的原始内容使用 Markdown 编写，保存在 GitHub 仓库中。
当网站相关文件更新并提交到 main 分支后，GitHub Actions 会按照工作流配置构建网站，并将生成的网页发布到 GitHub Pages。

## 项目目标

- 建立包含四个页面的文档网站。
- 为各页面配置清晰的导航。
- 在文档中使用表格、代码块和页面链接。
- 完成自动构建与自动部署。
- 通过再次修改文档，验证网站能够自动更新。

## 技术组成

| 工具 | 在项目中的作用 |
| --- | --- |
| Markdown | 编写页面正文 |
| Python | 提供 MkDocs 的运行环境 |
| MkDocs | 将 Markdown 转换为静态网站 |
| Material for MkDocs | 提供网站主题、导航和搜索界面 |
| Git | 记录文件修改并推送到远程仓库 |
| GitHub Actions | 自动执行构建与部署任务 |
| GitHub Pages | 托管生成的网站 |

## 文件结构说明

| 路径 | 内容 |
| --- | --- |
| docs/ | 网站的 Markdown 源文件 |
| mkdocs.yml | 网站名称、主题和导航配置 |
| requirements.txt | Python 依赖列表 |
| .github/workflows/deploy.yml | 自动部署工作流 |
| report/ | 实验报告与操作截图 |
| site/ | 本地构建时自动生成的网站文件 |

## 发布流程

1. 编写或修改 docs 目录中的文档。
2. 在本地检查页面效果与构建结果。
3. 将修改提交并推送到 main 分支。
4. GitHub Actions 构建并上传网站文件。
5. 部署任务将网站发布到 GitHub Pages。
6. 通过公开网址检查页面内容。

## 我的理解

在这个项目中，Markdown 文件负责保存内容，MkDocs 负责生成网页，
GitHub Actions 负责自动执行发布流程，GitHub Pages 负责提供网站访问服务。

将内容编写与发布流程分开后，日常更新主要集中在 Markdown 文件，
无需每次手工上传生成的网页。

[返回首页](index.md) · [查看使用指南](guide.md)
