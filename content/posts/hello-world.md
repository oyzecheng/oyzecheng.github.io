---
title: "Getting Started"
date: 2026-06-21T18:00:00+08:00
draft: false
tags: ["announcement"]
summary: "The first post on this site — what you'll find here."
---

This is the first post on this site. More content and resources will be shared here over time.

## Related Links

<!-- Add product backlinks like the line below — replace the text and URL with your own product: -->

- [Example Product](https://example.com)

## How to Publish a New Post

Create a new post:

```bash
hugo new content posts/my-new-post.md
```

Then change `draft: true` to `false` in the front matter, and commit & push:

```bash
git add .
git commit -m "New post"
git push
```

GitHub Actions will build and deploy automatically. Refresh the site after a minute or two.
