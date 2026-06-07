---
name: "hexo-helper"
description: "Hexo 博客日常维护工具。提供新建文章、启动服务器、部署站点、生成静态文件、清理缓存和查看状态等功能。当用户需要进行 Hexo 博客日常维护操作时调用此技能。"
---

# Hexo 博客维护助手

## 功能介绍

本技能提供以下 Hexo 日常维护功能：

### 1. 新建文章
- 命令: `hexo new post "文章标题"`
- 说明: 在 `source/_posts/` 目录下创建新的 Markdown 文章文件

### 2. 启动本地服务器
- 命令: `hexo server`
- 说明: 启动本地预览服务器，默认端口 4000
- 访问地址: http://localhost:4000/

### 3. 生成静态文件
- 命令: `hexo generate` 或 `hexo g`
- 说明: 将 Markdown 文章生成为静态 HTML 文件，输出到 `public/` 目录

### 4. 清理缓存
- 命令: `hexo clean`
- 说明: 清理生成的静态文件和缓存

### 5. 部署到 GitHub Pages
- 命令: `hexo deploy` 或 `hexo d`
- 说明: 将站点部署到配置的远程仓库

### 6. 查看站点状态
- 命令: `hexo list post`
- 说明: 列出所有文章信息

## 快捷操作

### 一键部署（推荐）
```bash
hexo clean && hexo deploy -g
```
此命令会依次执行：清理缓存 → 生成静态文件 → 部署

### 常用组合命令
- 预览前清理: `hexo clean && hexo server`
- 生成并预览: `hexo g && hexo s`

## 使用示例

```bash
# 创建新文章
hexo new post "我的第一篇博客"

# 启动预览服务器
hexo server

# 生成静态文件
hexo generate

# 部署到 GitHub
hexo deploy

# 清理缓存
hexo clean

# 查看文章列表
hexo list post
```

## 配置文件

主要配置文件: `_config.yml`
- `url`: 站点 URL
- `deploy`: 部署配置
- `theme`: 主题配置

## 注意事项

1. 部署前请确保已正确配置 `_config.yml` 中的 deploy 部分
2. 首次部署需要先安装 `hexo-deployer-git` 插件
3. 服务器运行时按 `Ctrl+C` 停止