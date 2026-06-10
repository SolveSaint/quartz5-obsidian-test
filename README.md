# Quartz 5 Obsidian Test

Live site: https://solvesaint.github.io/quartz5-obsidian-test/

This repository contains a Quartz 5 website built from an Obsidian-compatible Markdown vault.

The public website is generated from the Markdown files inside `/content`.

## How to edit the site

Open the `/content` folder as an Obsidian vault.

You can write normal Obsidian Markdown, including:

- `[[wikilinks]]`
- tags
- folders
- callouts
- embedded images and files
- frontmatter
- Mermaid diagrams

## How publishing works

When changes are pushed to GitHub, GitHub Actions builds the Quartz site and publishes it with GitHub Pages.

Workflow:

1. Edit notes in Obsidian or with AI.
2. Commit and push changes to GitHub.
3. GitHub Actions builds the Quartz site.
4. GitHub Pages updates the live website.

## Important folders

- `/content` — Obsidian vault and Quartz content source
- `/content/index.md` — homepage
- `/content/Notes` — recommended folder for regular notes
- `/content/Attachments` — recommended folder for images, PDFs, and other files
- `/quartz` — Quartz engine, plugins, components, and styles
- `/.github/workflows/deploy.yml` — GitHub Pages deployment workflow
