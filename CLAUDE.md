# Weyland Joyner's Blog (Quarto)

## Site overview

- Quarto website, output to `docs/`, hosted on GitHub Pages (custom domain may be configured)
- Config: `_quarto.yml` (theme: cosmo)
- Preview: `quarto preview`
- Render: `quarto render`
- Navbar tabs (in order): Writing, Bookshelf, Links, Language Learning, Resume/CV

## Creating blog posts

Posts live in `posts/<slug>/index.qmd`. To add a new post:

1. `mkdir` the directory `posts/<kebab-case-slug>/`
2. Create `posts/<kebab-case-slug>/index.qmd`
3. Use this frontmatter format:

```yaml
---
title: "Post Title"
author: "Weyland Joyner"
date: "YYYY-MM-DD"
categories: [category1, category2]
---
```

4. The user will often paste content from Apple Notes (sometimes with a screenshot). When they do:
   - **Fix links**: Apple Notes uses `(text)[url]` — convert to `[text](url)`
   - **Em dashes**: Use `---` (three hyphens) for em dashes in Quarto
   - **Bare URLs**: Wrap in angle brackets: `<https://example.com>`
   - **Emphasis**: Use `*italic*` for emphasis where the note's intent is clear
   - **Blockquotes**: Use `>` for quoted text
   - **Footnotes**: Use `[^1]` inline and `[^1]: Footnote text` at the bottom (note the colon)
   - **Backdating**: The user may ask to backdate a post; just set the `date` field accordingly
   - **Don't invent content**: Preserve the user's writing as-is; only fix formatting/links

## Common tasks

- **Adding posts**: Most frequent task. User pastes Apple Notes content, sometimes with a screenshot for reference. Fix the link syntax and formatting, create the post file.
- **Renaming posts**: Just change the `title` field in frontmatter.
- **Committing/pushing**: User will ask to commit and push. Use descriptive commit messages. The `docs/` directory contains rendered HTML that changes with every `quarto render`/`quarto preview`, so file counts in commits will be larger than expected.
- **Nav changes**: Edit `_quarto.yml` navbar section.

## Existing categories

software, agents, ai, books, history, data, consulting, distributed-systems, writing, meta

## Listing config

The homepage listing (`index.qmd`) uses `fields: [date, title, author, categories, description]` — images are excluded from the listing on purpose. The `title` field was removed from `index.qmd` frontmatter so no heading shows above the post list.

## Prototype site

There is a prototype plain HTML/CSS version of this blog at `~/projects/weylandjoyner.com` using the Flexoki color palette (calv.info-inspired). It has its own build system (`node build.js` with `marked`). The user may occasionally ask to add posts to both sites.
