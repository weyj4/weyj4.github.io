# weyj4.github.io

Personal blog built with [Quarto](https://quarto.org).

## Local Development

To preview the site locally:

```bash
quarto preview
```

To build the site:

```bash
quarto render
```

## Deployment

This site is configured to deploy to GitHub Pages from the `docs/` directory.

1. Push this repository to GitHub as `weyj4/weyj4.github.io`
2. In repository settings, go to Pages
3. Set source to "Deploy from a branch"
4. Select the `main` branch and `/docs` folder
5. Save

The site will be available at https://weyj4.github.io

## Writing New Posts

Create a new directory under `posts/` with an `index.qmd` file:

```bash
mkdir posts/my-new-post
touch posts/my-new-post/index.qmd
```

Add frontmatter to the post:

```yaml
---
title: "My Post Title"
description: "Brief description"
author: "weyj4"
date: "2026-01-21"
categories: [tag1, tag2]
---
```

Then write your content in Markdown below the frontmatter.
