# Nord GitHub Profile 部署与维护指南

本项目为 GitHub 用户 `@yunbuucuu` 定制的 **Nord 冰川蓝灰** 主题个人主页，支持根据访客的 GitHub 深色 / 浅色模式自动切换配色。

## 1. 创建同名 Profile 仓库

1. 登录 GitHub，点击右上角 **+** → **New repository**。
2. **Repository name** 必须填写与你的用户名完全一致的名称：`yunbuucuu`（此时 GitHub 会提示这是一个特殊的主页仓库）。
3. 仓库权限设为 **Public**，不要勾选自带的 README / `.gitignore`（以便直接推送本地文件），点击 **Create repository**。

## 2. 推送本地文件到 GitHub

在当前目录（`e:\DuplicateFile\code_project\github-MyHome`）执行：

```powershell
git init -b main
git add .
git commit -m "feat: add Nord themed GitHub profile README"
git remote add origin https://github.com/yunbuucuu/yunbuucuu.git
git push -u origin main
```

> 说明：`.gitignore` 已自动排除本地预览文件 `preview.html`，不会推送到远端仓库。

## 3. 启用贪吃蛇贡献动画

推送完成后，`.github/workflows/snake.yml` 会自动触发首次运行（也可以在仓库的 **Actions → Generate Nord Contribution Snake → Run workflow** 手动运行一次）。

运行成功后会自动创建 `output` 分支并生成 Nord 深/浅双版贪吃蛇 SVG，之后主页中的贪吃蛇板块即可正常显示，并每天自动更新。

## 4. 后续如何扩展内容

- **添加博客或 X（Twitter）徽章**：打开 `README.md`，取消顶部“社交与联系方式徽章”区块中的注释并填入你的链接即可。
- **补充技术栈**：`README.md` 的技术栈区块下方已预留 NumPy、CUDA、Linux、Git、Docker、LaTeX 等常用 Nord 风格徽章链接模板，可直接复制使用。
- **上线精选项目**：在 `README.md` 的“精选项目”区块下方，已内置 2×2 双列项目卡片模板，替换 `REPO_1` / `REPO_2` 与简介即可。
- **本地预览深/浅效果**：直接用浏览器打开本地的 `preview.html`，点击右上角按钮即可在 Nord 深色（Polar Night）和浅色（Snow Storm）之间一键切换查看。
