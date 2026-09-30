# 个人技术笔记

使用 [Hugo](https://gohugo.io/) 和官方 [PaperMod](https://github.com/adityatelange/hugo-PaperMod) 主题构建的个人技术博客。

## 本地开发

首次克隆后先初始化主题子模块：

```bash
git submodule update --init --recursive
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

静态产物输出到 `public/`。Vercel 会先初始化主题子模块，并使用 Hugo `0.167.0` 构建到同一目录。

## 目录说明

- `content/`：Markdown 页面与文章
- `assets/css/extended/`：PaperMod 扩展样式
- `themes/PaperMod/`：PaperMod 主题子模块
- `hugo.toml`：站点配置
