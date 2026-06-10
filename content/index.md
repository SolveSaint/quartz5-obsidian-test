---
created: 2026-06-09
updated: 2026-06-09
description: Start here to learn how this Quartz 5 site works, how to edit it with Obsidian, and how to publish updates through GitHub Pages.
title: Welcome
publish: true
draft: false
comments: false
enableToc: true
quartz-properties: false
quartz-properties-collapse: false
lang: en
aliases:
  - Home
  - Start Here
  - Getting Started
cssclasses:
  - homepage
socialDescription: A Quartz 5 website built from an Obsidian-compatible Markdown vault and published with GitHub Pages.
published: 2026-06-09
tags:
  - Quartz
  - Obsidian
  - GitHubPages
  - GettingStarted
---

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

## Starter frontmatter rules

Quartz uses YAML frontmatter at the top of Markdown files to control metadata, publishing behavior, comments, table of contents behavior, aliases, CSS classes, and social previews.

Use this standard pattern for regular notes:

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
published: 2026-06-09
tags:
  - Quartz
  - Obsidian
---
```

Important rules:

- Keep `created` first and `updated` second so Obsidian date plugins can manage them predictably.
- Put Quartz behavior fields such as `publish`, `draft`, `comments`, `enableToc`, and `quartz-properties` above `tags`.
- Include only booleans or fields with real set values.
- Do not include `null` placeholder fields.
- Do not include empty optional fields such as `aliases: []` or `cssclasses: []`.
- Do not include `permalink` in standard generated frontmatter.
- Add `permalink` only when a page needs a real custom URL.
- Never use `permalink: /` on `content/index.md`; the homepage already publishes at the site root.
- Do not repeat the page title as a Markdown `# Heading` when Quartz already renders the page title from frontmatter.
- Use `quartz-properties: false` on public landing pages when the properties panel would clutter the design.
- Use `comments: false` unless comments are intentionally configured for the site.

Optional fields should appear only when they have real values:

```yaml
aliases:
  - Alternate Name
cssclasses:
  - landing-page
socialDescription: A custom social preview description.
socialImage: /Attachments/social-card.png
permalink: /about
```

Known fields used by this starter site:

| Field | Purpose |
|---|---|
| `created` | Creation date for the note. |
| `updated` | Last updated date. This stays second for Obsidian date plugins. |
| `description` | Page description for metadata, previews, and search. |
| `title` | Page title rendered by Quartz. |
| `publish` | Marks a page as publishable when explicit publishing is enabled. |
| `draft` | Pages with `draft: true` are removed by the drafts filter. |
| `comments` | Enables or disables comments when a comments provider is configured. |
| `enableToc` | Enables or disables the table of contents for the page. |
| `quartz-properties` | Controls whether the note properties panel is shown. |
| `quartz-properties-collapse` | Controls whether the note properties panel starts collapsed. |
| `lang` | Language code for the page. |
| `published` | Publication date. |
| `tags` | Page tags. |
| `aliases` | Optional alternate names for link resolution. Omit unless set. |
| `cssclasses` | Optional page-specific CSS classes. Omit unless set. |
| `socialDescription` | Optional social-preview-specific description. Omit unless set. |
| `socialImage` | Optional social preview image. Omit unless set. |
| `permalink` | Optional custom URL path. Omit unless a real custom path is needed. |

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
