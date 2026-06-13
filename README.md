# Sekiro's Personal Blog

**主页链接**: [https://sekiro-x.github.io](https://sekiro-x.github.io)

## 📝 简介

这是我的个人博客网站，使用 GitHub Pages 和 Jekyll 构建。

## ✨ 功能特性

- 🎨 简洁美观的界面设计
- 📱 响应式布局，支持移动端
- 📝 博客文章管理
- 🔗 社交媒体链接
- 💜 渐变色主题设计

## 🚀 本地开发

### 环境要求

- Ruby (>= 2.5.0)
- Bundler
- Jekyll

### 安装步骤

1. 克隆仓库
```bash
git clone https://github.com/Sekiro-x/Sekiro-x.github.io.git
cd Sekiro-x.github.io
```

2. 安装依赖
```bash
bundle install
```

3. 启动本地服务器
```bash
bundle exec jekyll serve
```

4. 在浏览器中访问 `http://localhost:4000`

## 📁 项目结构

```
.
├── _config.yml          # Jekyll 配置文件
├── _layouts/            # 页面布局模板
│   └── post.html        # 博客文章布局
├── _posts/              # 博客文章目录
│   └── 2026-06-13-test.md
├── assets/              # 静态资源
│   └── images/          # 图片资源
├── css/                 # 样式文件
│   └── style.css
├── index.html           # 主页
└── README.md            # 项目说明
```

## 🎨 自定义

### 修改头像

将你的头像图片放置在 `assets/images/avatar.jpg`，或者修改 `index.html` 中的头像链接。

### 添加社交链接

在 `index.html` 的 `.social-links` 部分添加新的社交链接。

### 发布新文章

在 `_posts/` 目录下创建新的 Markdown 文件，文件名格式为 `YYYY-MM-DD-title.md`。

## 📄 License

MIT License

---

Made with ❤️ by Sekiro
