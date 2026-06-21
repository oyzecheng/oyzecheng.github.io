---
title: "开篇：关于这个站点"
date: 2026-06-21T18:00:00+08:00
draft: false
tags: ["公告"]
summary: "站点的第一篇文章，介绍这里会分享什么内容。"
---

这是本站的第一篇文章。这里会陆续分享一些内容与资源。

## 相关链接

<!-- 在文章里放外链就像下面这样，把文字和地址换成你自己的产品： -->

- [示例产品](https://example.com)

## 怎么发新文章

新建一篇文章：

```bash
hugo new content posts/my-new-post.md
```

写完后把文章顶部 front matter 里的 `draft: true` 改成 `false`，然后提交推送：

```bash
git add .
git commit -m "新文章"
git push
```

推送后 GitHub Actions 会自动构建并发布，等一两分钟刷新站点就能看到。
