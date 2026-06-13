# 快速开始指南

## 🎉 恭喜！你的个人主页已经创建完成

### ✅ 已完成的功能

1. **顶部导航栏**
   - 主页按钮
   - 备忘录按钮
   - 评论按钮

2. **左侧个人信息栏**
   - 头像（默认使用占位图，你可以替换为自己的头像）
   - ID: Sekiro
   - GitHub 链接

3. **右侧博客区域**
   - 已创建一篇测试文章 "Test Blog Post"
   - 支持显示多篇文章
   - 每篇文章显示标题、日期和摘要

4. **其他页面**
   - 备忘录页面 (memo.html)
   - 评论页面 (comments.html)

### 📝 如何自定义

#### 1. 更换头像
将你的头像图片放到 `assets/images/` 目录下，命名为 `avatar.jpg`，或者修改 `index.html` 中的头像路径。

#### 2. 修改 GitHub 链接
在 `index.html` 中找到这一行：
```html
<a href="https://github.com/Sekiro-x" target="_blank" class="social-link">
```
将链接改为你的 GitHub 地址。

#### 3. 添加更多社交链接
在 `index.html` 的 `.social-links` 部分添加新的链接，例如：
```html
<a href="你的链接" class="social-link">
    <i class="图标类名"></i>
    <span>平台名称</span>
</a>
```

#### 4. 发布新博客文章
在 `_posts/` 目录下创建新的 Markdown 文件，文件名格式为：`YYYY-MM-DD-标题.md`

例如：`2026-06-14-my-first-post.md`

文件内容格式：
```markdown
---
layout: post
title: "文章标题"
date: 2026-06-14 10:00:00 +0800
categories: [分类]
tags: [标签]
---

这里是文章内容...
```

### 🚀 本地预览

如果你想在本机预览网站效果：

1. 安装 Ruby 和 Bundler
2. 运行以下命令：
```bash
bundle install
bundle exec jekyll serve
```
3. 在浏览器中访问 `http://localhost:4000`

### 🌐 部署到 GitHub Pages

1. 将所有文件推送到你的 GitHub 仓库
2. 进入仓库设置 (Settings)
3. 找到 "Pages" 选项
4. 选择主分支作为源
5. 等待几分钟，你的网站就会在 `https://sekiro-x.github.io` 上线

### 🎨 主题特色

- 💜 紫色渐变主题
- 📱 响应式设计，支持移动端
- ✨ 平滑的动画效果
- 🎯 简洁现代的界面

---

如有任何问题，欢迎随时询问！
