---
created: 2026-06-09
updated: 2026-06-10
description: A starter guide for editing and publishing the SolveSaint/quartz5-obsidian-test Quartz 5 site.
title: Welcome to your Quartz 5 site running on SolveSaint/quartz5-obsidian-test
cssclasses:
  - homepage
draft: false
enableToc: true
quartz-properties: false
lang: en
tags:
  - Quartz
  - GitHubPages
  - Obsidian
  - Instructions
---

<img class="site-banner" src="static/quartz5-obsidian-test-banner.svg" alt="quartz5-obsidian-test banner">

# Welcome to your Quartz 5 site running on SolveSaint/quartz5-obsidian-test

This site is a Quartz 5 GitHub Pages site generated from the `SolveSaint/quartz5-obsidian-test` repository.

Live site: https://solvesaint.github.io/quartz5-obsidian-test/

Repository: https://github.com/SolveSaint/quartz5-obsidian-test

## What this site is

Quartz turns Markdown notes into a linked, searchable static website. Write notes in Markdown, keep them in the `content/` folder, and publish changes through GitHub.

## Editing notes

Edit Markdown files inside `content/`. Each Markdown file becomes a page if it is not removed by filters.

Folders help organize files, but folders are not pages by themselves. Links between notes create the real site structure.

## Publishing changes

Commit changes to the `main` branch. GitHub Actions rebuilds the site and publishes the updated version to GitHub Pages.

After a publish, check the live site and confirm that new pages, internal links, search, and navigation work under `/quartz5-obsidian-test/`.

## Basic frontmatter pattern

Use only fields with actual values. Do not add empty placeholders or null fields.

For ordinary pages, start with title, description, draft status, table-of-contents setting, language, and tags.

Do not put `permalink: /` on the homepage. Quartz already treats `content/index.md` as the site root.

## Adding content

Start with small changes: add one note, link it from another note, commit and publish, then verify the live page.
