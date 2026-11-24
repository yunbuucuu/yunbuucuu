# Monochrome Sketch GitHub Profile 维护指南

本项目为 GitHub 用户 `@yunbuucuu` 定制的 **黑白手绘涂鸦风（Monochrome Ink & Chalk）** 个人主页，支持根据访客的 GitHub 深色 / 浅色模式自动切换配色。

## 核心配色体系

- **浅色模式（Concrete & Ink）**：水泥灰 `#8C8C8C` / 浅灰纸 `#ECECEC` + 纯黑墨线 `#111111` + 粉笔白 `#FFFFFF`
- **深色模式（Charcoal & Chalk）**：深炭黑 `#141414` / `#262626` + 纯白粉笔描边 `#FFFFFF` + 浅灰字 `#D4D4D4`

## 后续扩展内容

- **添加博客或 X（Twitter）徽章**：打开 `README.md`，取消顶部“社交与联系方式徽章”中的注释并替换链接即可。
- **上线精选项目**：在 `README.md` 的“精选项目”区块下方，已内置 2×2 双列卡片模板，替换 `REPO_1` / `REPO_2` 与简介即可。
- **贪吃蛇自动更新**：`.github/workflows/snake.yml` 每次推送到 `main` 及每日 UTC 00:00 自动生成黑白灰阶深/浅双版贪吃蛇并推送至 `output` 分支。
- **本地预览**：浏览器打开 `preview.html` 即可一键切换深色 / 浅色效果（已通过 `.gitignore` 排除，不会推送到远端）。
