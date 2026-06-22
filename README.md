# Owen's Blog

A static blog built with [Hugo](https://gohugo.io/) and the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme, deployed on GitHub Pages.

Live site: <https://oyzecheng.github.io/>

## Local Preview

```bash
hugo server -D
```

Open <http://localhost:1313/>. `-D` also renders drafts.

## Write a New Post

```bash
hugo new content posts/my-post.md
```

Edit the generated `content/posts/my-post.md`, then change `draft: true` to `false` in the front matter.

## Publish

Push to the `main` branch. `.github/workflows/hugo.yml` builds and deploys to GitHub Pages automatically via GitHub Actions.

## Project Structure

| Path | Description |
| --- | --- |
| `content/` | Posts and pages (Markdown) |
| `static/` | Static assets (images, etc.), copied as-is to the site root |
| `themes/PaperMod/` | Theme (git submodule) |
| `hugo.toml` | Site configuration |
| `.github/workflows/` | Deployment workflow |

## Clone (with theme submodule)

```bash
git clone --recurse-submodules https://github.com/oyzecheng/oyzecheng.github.io.git
```
