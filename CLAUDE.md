# Weyland Joyner's Blog (Quarto)

## Site overview

- Quarto website, output to `docs/`, hosted on GitHub Pages
- Config: `_quarto.yml` (theme: cosmo)
- Preview: `quarto preview`
- Render: `quarto render`

## Creating blog posts

Posts live in `posts/<slug>/index.qmd`. To add a new post:

1. Create `posts/<kebab-case-slug>/index.qmd`
2. Use this frontmatter format:

```yaml
---
title: "Post Title"
author: "Weyland Joyner"
date: "YYYY-MM-DD"
categories: [category1, category2]
---
```

3. The user will often paste content from Apple Notes. When they do:
   - **Fix links**: Apple Notes uses `(text)[url]` — convert to `[text](url)`
   - **Em dashes**: Use `---` (three hyphens) for em dashes
   - **Bare URLs**: Wrap in angle brackets: `<https://example.com>`
   - **Emphasis**: Use `*italic*` for emphasis where the note's intent is clear
   - **Blockquotes**: Use `>` for quoted text
   - **Backdating**: The user may ask to backdate a post; just set the `date` field accordingly
   - **Don't invent content**: Preserve the user's writing as-is; only fix formatting/links

## Existing categories

software, agents, ai, books, history, data, consulting, distributed-systems, writing, meta

## Listing config

The homepage listing (`index.qmd`) uses `fields: [date, title, author, categories, description]` — images are excluded from the listing on purpose.
