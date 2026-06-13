---
layout: default
title: UV 指南
---

# 使用 UV 控制 Python 版本

以下是一份使用 UV 控制 Python 版本的详细文档，涵盖安装、项目环境管理、依赖包配置及环境导出等内容，适合团队协作和跨设备开发。

## 一、安装 UV

UV 是一个基于 Rust 的现代 Python 项目管理工具，支持快速安装和管理 Python 版本、虚拟环境及依赖包。

### 1. Linux 和 macOS 安装

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

### 2. Windows 安装

```powershell
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"
```

### 3. 配置命令补全（可选，提升体验）

Linux/macOS：添加以下命令到 `~/.bashrc` 或 `~/.zshrc`：

```bash
eval "$(uv generate-shell-completion)"
```

Windows：在用户配置文件（如 `$PROFILE`）添加：

```powershell
Invoke-Expression (&uv generate-shell-completion)
```

## 二、使用 UV 安装和管理 Python 版本

UV 支持安装、切换和管理多个 Python 版本，无需依赖系统全局环境。

### 1. 查看可用的 Python 版本

```bash
uv python list
```

### 2. 安装指定版本的 Python

```bash
uv python install 3.12
```

### 3. 切换当前项目的 Python 版本（在虚拟环境中）

```bash
uv python pin 3.12
```

## 三、在项目中使用 UV 管理 Python 虚拟环境

UV 通过虚拟环境隔离项目依赖，避免版本冲突。

### 1. 初始化项目

```bash
uv init my-project
cd my-project
```

生成的项目结构：

```
my-project/
├── pyproject.toml
├── README.md
└── hello.py
```

### 2. 配置项目 Python 版本

编辑 `pyproject.toml`：

```toml
[project]
requires-python = ">=3.12"
```

### 3. 创建并激活虚拟环境

```bash
uv venv
source .venv/bin/activate        # Linux/macOS
.venv\Scripts\activate           # Windows
```

## 四、安装第三方依赖包

UV 兼容 `pip` 的语法，但更高效。

### 1. 安装生产依赖

```bash
uv pip install requests flask
```

### 2. 安装开发依赖（如测试工具）

```bash
uv pip install pytest --dev
```

### 3. 从 requirements.txt 安装

```bash
uv pip install -r requirements.txt
```

## 五、导出和共享项目环境

确保其他开发者能复现环境。

### 1. 生成依赖锁文件

```bash
uv pip freeze > requirements.lock
```

### 2. 共享环境配置

将以下文件提交到版本控制（如 Git）：

- `pyproject.toml`（或 `requirements.txt`）
- `requirements.lock`

`.venv/` 目录通常不需要提交，但可添加 `.gitignore` 忽略。

### 3. 在其他设备上恢复环境

克隆项目后，执行：

```bash
uv venv
uv pip install -r requirements.lock
```

## 六、常见问题与技巧

全局安装包（不推荐，但可用于工具类包）：

```bash
uv pip install --system some-package
```

删除虚拟环境：

```bash
rm -rf .venv
```

查看当前项目 Python 版本：

```bash
uv python list --only-installed
```

## 七、总结

通过 UV，开发者可以：

- 统一管理项目 Python 版本和依赖
- 快速创建隔离环境，避免全局污染
- 一键同步环境配置，方便团队协作
- 利用高效安装速度（比 pip 快 10-100 倍）

## 参考资料

- UV 官方文档：[https://docs.astral.sh/uv/](https://docs.astral.sh/uv/)
- 示例项目模板：[https://github.com/astral-sh/uv](https://github.com/astral-sh/uv)
