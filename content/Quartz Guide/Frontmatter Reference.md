---
created: 2026-06-09
updated: 2026-06-09
description: Reference for the Quartz 5 frontmatter fields used by this starter site.
title: Frontmatter Reference
publish: true
draft: false
comments: true
enableToc: true
quartz-properties: true
quartz-properties-collapse: false
lang: en
aliases:
  - Quartz Frontmatter
  - Frontmatter Guide
cssclasses: []
socialDescription: null
socialImage: null
published: 2026-06-09
tags:
  - Quartz
  - Frontmatter
  - Reference
---

# Frontmatter Reference

This site uses YAML frontmatter at the top of each Markdown file.

Standard generated notes keep `created` first and `updated` second so Obsidian plugins can manage the updated date without moving the field.

## Standard order for regular notes

```yaml
---
created: 2026-06-09
updated: 2026-06-09
description: Short page description.
title: Page Title
publish: true
draft: false
comments: false
enableToc: true
quartz-properties: true
quartz-properties-collapse: false
lang: en
aliases: []
cssclasses: []
socialDescription: null
socialImage: null
published: 2026-06-09
tags:
  - Quartz
  - Obsidian
---
```

## Homepage exception

`content/index.md` already becomes the site root.

Do not add `permalink` to the homepage frontmatter.

Do not use:

```yaml
permalink: /
```

That can create a root redirect artifact instead of the real homepage.

## Field meanings

| Field | What it does |
|---|---|
| `created` | Creation date for the note. |
| `updated` | Last updated date. Leave this near the top for Obsidian date plugins. |
| `description` | Page description for metadata, previews, and search. |
| `title` | Page title. |
| `publish` | Used by explicit publish filtering if enabled. |
| `draft` | Pages with `draft: true` are removed by the drafts filter. |
| `comments` | Enables or disables page comments when a comments plugin is configured. |
| `enableToc` | Enables or disables the table of contents for the page. |
| `quartz-properties` | Controls whether the note properties panel is shown. |
| `quartz-properties-collapse` | Controls whether the note properties panel starts collapsed. |
| `lang` | Language code for the page. |
| `permalink` | Custom URL path for non-homepage pages. Use `null` when unused. |
| `aliases` | Alternate names for link resolution. |
| `cssclasses` | Page-specific CSS classes. |
| `socialDescription` | Optional social-preview-specific description. |
| `socialImage` | Optional social preview image. |
| `published` | Publication date. |
| `tags` | Page tags. |
