# Blog

基于 [Hugo](https://gohugo.io/) + [PaperMod](https://github.com/adityatelange/hugo-PaperMod) 的静态博客，部署在 GitHub Pages。

线上地址：<https://oyzecheng.github.io/>

## 本地预览

```bash
hugo server -D
```

打开 <http://localhost:1313/>。`-D` 表示同时渲染草稿。

## 写新文章

```bash
hugo new content posts/my-post.md
```

编辑生成的 `content/posts/my-post.md`，写完后把 front matter 里的 `draft: true` 改成 `false`。

## 发布

把改动 push 到 `main` 分支即可。`.github/workflows/hugo.yml` 会自动用 GitHub Actions 构建并部署到 GitHub Pages。

## 目录结构

| 路径 | 说明 |
| --- | --- |
| `content/` | 文章和页面（Markdown） |
| `static/` | 静态资源（图片等），按原样拷贝到站点根目录 |
| `themes/PaperMod/` | 主题（git submodule） |
| `hugo.toml` | 站点配置 |
| `.github/workflows/` | 自动部署流程 |

## 克隆（记得带上主题 submodule）

```bash
git clone --recurse-submodules https://github.com/oyzecheng/oyzecheng.github.io.git
```
