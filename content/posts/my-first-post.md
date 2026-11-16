---
title: "使用 Hugo + PaperMod 搭建个人博客"
date: 2026-11-16T22:00:00+08:00
draft: false
tags: ["Hugo", "Blog", "GitHub Pages"]
categories: ["技术"]
description: "基于 Hugo 和 PaperMod 主题的个人博客搭建与自动化部署流程记录。"
---

## 为什么选择 Hugo + PaperMod？

1. **极速构建**：Go 语言编写，毫秒级编译。
2. **优雅阅读**：PaperMod 主题干净纯粹，支持深色模式切换、文章目录、搜索、代码一键复制。
3. **零成本维护**：配合 GitHub Actions 与 GitHub Pages，提交 Markdown 即自动发布。

## 写作流程

日常写作只需要在 VS Code 中编写 Markdown 文件，然后执行 Git 提交：

```bash
git add .
git commit -m "发布新文章"
git push
```

GitHub Actions 会自动触发并在几十秒内完成构建与发布。
