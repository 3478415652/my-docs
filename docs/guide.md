# 使用指南

## 一、准备环境

本项目使用 Git、Python 3.12 和文本编辑器。

在 Windows PowerShell 中，可以使用以下命令检查环境：

```powershell
git --version
py -3.12 --version
py -3.12 -m pip --version
```

## 二、下载项目

```powershell
git clone https://github.com/3478415652/my-docs.git
cd my-docs
```

后续命令均在项目根目录中执行。

## 三、创建虚拟环境

```powershell
py -3.12 -m venv .venv
```

虚拟环境用于安装本项目所需的 Python 依赖。

下面直接调用虚拟环境中的 Python，无需先执行激活脚本。

## 四、安装依赖

```powershell
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

## 五、检查构建结果

```powershell
.\.venv\Scripts\python.exe -m mkdocs build --strict
```

此命令会将网站生成到 site 目录。
如果出现警告或错误，应先阅读终端输出，检查配置、页面路径和链接。

## 六、本地预览

```powershell
.\.venv\Scripts\python.exe -m mkdocs serve
```

启动后，在浏览器中打开终端显示的地址，通常为：

```text
http://127.0.0.1:8000/
```

检查首页、关于、使用指南和 API 参考是否能正常访问。

预览结束后，在终端按 Ctrl+C 停止服务。

## 七、更新网站

修改 docs 中的文件并保存，然后执行：

```powershell
git add docs
git diff --staged
git commit -m "更新技术文档"
git push origin main
```

推送后进入 GitHub 仓库的 Actions 页面，查看自动构建与部署结果。

## 八、常见问题

| 现象 | 检查方法 |
| --- | --- |
| 页面无法跳转 | 检查 Markdown 链接与文件名是否一致 |
| 导航缺少页面 | 检查 mkdocs.yml 中的 nav 配置 |
| 构建失败 | 查看 Actions 中失败步骤的具体日志 |
| 网站内容没有更新 | 检查最新部署状态，并刷新浏览器 |
| 网站出现 404 | 检查部署是否完成，以及网址是否包含 /my-docs/ |

## 九、在线访问

[打开公开网站](https://3478415652.github.io/my-docs/)

[返回首页](index.md) · [查看 API 参考](api.md)
