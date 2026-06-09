# First-practice
第一次练习网页制作

项目说明
=======

概述
----
这是一个极简的静态站点示例仓库。已把 `index.html` 替换为一个简单的待办（TODO）页面，支持：

- 输入并添加事项（回车或点击“添加”）
- 每项带复选框，支持多选
- 删除所选事项（点击“删除选中”）
- 全选/取消全选

快速验证
-------
1. 在文件管理器中打开 `index.html`，或用浏览器直接拖入并打开该文件。
2. 在页面上输入事项，点击“添加”或按回车，验证事项出现在列表中。
3. 勾选若干事项，点击“删除选中”以确认删除功能正常。

回滚说明
------
如需恢复原始 `index.html`，可用版本控制回退或手动替换为之前的备份内容（若没有版本控制，请告知我，我可以尝试恢复原始内容，如果你提供备份）。

变更清单
------
- 新增：`AGENTS.md`（为 AI 代理提供仓库简要说明）
- 修改：`index.html`（替换为 TODO 页面）
- 新增：`README.md`（当前文件）

下一步建议
--------
- （可选）创建 `.github/copilot-instructions.md` 以提供更细化的代理交互策略。
- （可选）为 TODO 页面增加数据持久化（localStorage）或导出/导入功能。

需要我继续创建 `.github/copilot-instructions.md` 吗？

部署到 GitHub Pages
-----------------
你可以使用 GitHub Pages 自动部署本仓库（已添加 GitHub Actions 工作流）。流程概览和本地命令：

1. 在 GitHub 上创建一个新的仓库（例如 `your-username/your-repo`）。
2. 在本地将当前目录初始化为 git 仓库并推送到远端：

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
# 通过 SSH
git remote add origin git@github.com:YOUR_USERNAME/YOUR_REPO.git
# 或通过 HTTPS
# git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

3. 推送后，GitHub Actions 会在 `main` 分支有新提交时自动执行部署工作流。首次运行可能需要几分钟。

4. 部署成功后，页面地址通常为 `https://YOUR_USERNAME.github.io/YOUR_REPO/`。你也可以在仓库的 `Settings → Pages` 查看生效的网址。

注意：工作流会把仓库根目录内容作为站点内容发布，如果你希望只发布 `dist/` 或其他子目录，请告知，我会调整工作流。

如果当前 GitHub Pages 还没有启用，工作流会在仓库秘密 `PAGES_PAT` 存在时尝试自动启用 Pages。没有设置该秘钥时，工作流将跳过自动启用步骤，需先在仓库设置中手动启用 Pages：`Settings → Pages`，将源设置为 `main` 分支和根目录，然后保存。

要让自动启用工作流正常运行，请创建一个 GitHub 个人访问令牌（PAT），至少包含 `repo` 范围或 `administration:write` 和 `pages:write` 权限，并将其保存为仓库秘密 `PAGES_PAT`。

当前该仓库已重定向为 GitHub Pages 站点仓库 `First-practice.github.io`，所以网站应发布到：

https://zhaoyucheng111.github.io/
