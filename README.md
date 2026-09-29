# 个人技术笔记

使用 [Hugo](https://gohugo.io/) 和 [GitHub Style](https://github.com/MeiK2333/github-style) 构建的个人技术博客。

## 本地开发

```bash
hugo server --buildDrafts
```

默认在 `http://localhost:1313` 预览。

## 新建文章

```bash
hugo new post/my-new-post.md
```

将新文章的 `draft` 改为 `false` 后，它会出现在生产构建中。

## 生产构建

```bash
hugo --gc --minify
```

静态产物输出到 `public/`，Vercel 的构建命令使用同一命令，输出目录为 `public`。

## 目录说明

- `content/`：Markdown 页面与文章
- `static/`：自定义静态文件
- `themes/github-style/`：GitHub Style 主题子模块
- `hugo.toml`：站点配置
