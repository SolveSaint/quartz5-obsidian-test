---
created: 2026-06-09
updated: 2026-06-09
description: Start here to learn how this Quartz 5 site works, how to edit it with Obsidian, and how to publish updates through GitHub Pages.
title: Welcome
publish: true
draft: false
comments: false
enableToc: true
quartz-properties: true
quartz-properties-collapse: false
lang: en
aliases:
  - Home
  - Start Here
  - Getting Started
cssclasses:
  - homepage
socialDescription: A Quartz 5 website built from an Obsidian-compatible Markdown vault and published with GitHub Pages.
socialImage: null
published: 2026-06-09
tags:
  - Quartz
  - Obsidian
  - GitHubPages
  - GettingStarted
---

# Welcome

This is a Quartz 5 website built from an Obsidian-compatible Markdown vault.

The public website is generated from the Markdown files in this repository’s `/content` folder. You can edit the site manually, write in Obsidian, or use AI assistance to create and organize notes.

## Authoring with Obsidian

Open the `/content` folder as an Obsidian vault.

You can use normal Obsidian features, including:

- `[[wikilinks]]`
- tags
- folders
- callouts
- embedded images and files
- frontmatter
- Markdown notes

## Authoring with AI

You can also use AI to help maintain the site.

Useful requests include:

- Create a new Markdown note in `/content`
- Rewrite or expand an existing note
- Add frontmatter
- Create a topic index or Map of Content
- Add wikilinks between related notes
- Organize notes into folders
- Update the homepage
- Commit changes to GitHub

The Markdown files in `/content` are the source of truth.

## Frontmatter available in this site

Quartz uses YAML frontmatter at the top of Markdown files to control page metadata, publishing behavior, comments, table of contents behavior, aliases, CSS classes, and social previews.

This site uses the full visible starter pattern for regular notes:

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

Known fields used by this starter site:

| Field | Purpose |
|---|---|
| `created` | Creation date for the note. |
| `updated` | Last updated date. This stays second for Obsidian date plugins. |
| `description` | Page description for metadata, previews, and search. |
| `title` | Page title. |
| `publish` | Marks a page as publishable when explicit publishing is enabled. |
| `draft` | Pages with `draft: true` are removed by the drafts filter. |
| `comments` | Enables or disables comments when a comments provider is configured. |
| `enableToc` | Enables or disables the table of contents for the page. |
| `quartz-properties` | Controls whether the note properties panel is shown. |
| `quartz-properties-collapse` | Controls whether the note properties panel starts collapsed. |
| `lang` | Language code for the page. |
| `permalink` | Custom URL path for non-homepage pages. |
| `aliases` | Alternate names for link resolution. |
| `cssclasses` | Page-specific CSS classes. |
| `socialDescription` | Optional social-preview-specific description. |
| `socialImage` | Optional social preview image. |
| `published` | Publication date. |
| `tags` | Page tags. |

Homepage rule: `content/index.md` already becomes the site root, so the homepage should omit `permalink` entirely. Do not use `permalink: /` on the homepage.

For the full reference, see [[Quartz Guide/Frontmatter Reference]].

## Publishing

When changes are pushed to GitHub, GitHub Actions builds the Quartz site and GitHub Pages publishes the updated website.

Workflow:

1. Edit notes in Obsidian or with AI.
2. Commit and push changes to GitHub.
3. GitHub Actions builds the site.
4. GitHub Pages updates the live website.

## Important folders

- `/content` — Obsidian vault and Quartz content source
- `/content/index.md` — this homepage
- `/content/Notes` — recommended folder for regular notes
- `/content/Attachments` — recommended folder for images, PDFs, and other files
- `/quartz` — Quartz engine, plugins, components, and styles
- `/.github/workflows/deploy.yml` — GitHub Pages deployment workflow

## First note

Start with:

[[Notes/First Note]]
