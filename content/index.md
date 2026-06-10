---
created: 2026-06-09
updated: 2026-06-09
description: Instructions for editing, configuring, and deploying this Quartz 5 test site through the SolveSaint/quartz5-obsidian-test GitHub repository.
title: Welcome to your Quartz 5 site running on SolveSaint/quartz5-obsidian-test
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

This Quartz 5 site is running from the `SolveSaint/quartz5-obsidian-test` GitHub repository.

Live site:

```text
https://solvesaint.github.io/quartz5-obsidian-test/
```

Repository:

```text
https://github.com/SolveSaint/quartz5-obsidian-test
```

## Operating rule

Build the site in phases. Do not mix bootstrap, deployment, content, styling, and layout changes in the same step.

The safe sequence is:

1. Bootstrap Quartz 5 into the wiped repository.
2. Set the baseline configuration.
3. Remove the temporary bootstrap workflow.
4. Add the deploy workflow.
5. Verify GitHub Pages deployment.
6. Add content and customization in small commits.

## Baseline configuration

The required project-page base URL is:

```yaml
baseUrl: SolveSaint.github.io/quartz5-obsidian-test
```

The top-left site title is controlled by `configuration.pageTitle` in `quartz.config.yaml`. It should match the repository/site name:

```yaml
pageTitle: quartz5-obsidian-test
```

Set `baseUrl` and `pageTitle` together during the baseline configuration step.

## Deployment workflow

The deployment workflow should be the only permanent GitHub Actions workflow unless a specific new workflow is intentionally added.

The deploy workflow should:

1. Check out the repository.
2. Use Node 24.
3. Run `npm ci`.
4. Run `npx quartz plugin install`.
5. Run `npx quartz build`.
6. Upload the `public` folder.
7. Deploy to GitHub Pages.

Temporary bootstrap workflows should be removed after they succeed.

## Content rules

Pages live in the `content/` folder. Folders organize notes, but folders are not pages by themselves. Links create structure.

Keep starter content simple until the deploy is verified. Do not add layout experiments, CSS experiments, or plugin changes during the install phase.

## Frontmatter rules

Use only fields with actual values. Do not include null placeholders, empty arrays, or unused optional fields.

Good pattern:

```yaml
---
created: 2026-06-09
updated: 2026-06-09
description: Short page description.
title: Page Title
draft: false
enableToc: true
quartz-properties: false
lang: en
tags:
  - Quartz
  - Obsidian
---
```

Avoid:

```yaml
aliases: []
cssclasses: []
socialDescription: null
socialImage: null
permalink: null
```

Do not put `permalink: /` on the homepage. Quartz already treats `content/index.md` as the site root.

## Editing workflow

Edit Markdown files in `content/`. Commit changes to `main`. GitHub Actions will rebuild and publish the site.

After any change, verify:

1. The GitHub Actions deploy run completes successfully.
2. The live site loads.
3. Internal links work under `/quartz5-obsidian-test/`.
4. The left site title still reads `quartz5-obsidian-test`.

## Debugging rule

When something breaks, inspect before patching:

1. Read the workflow file.
2. Read the workflow logs.
3. Read `quartz.config.yaml`.
4. Read the affected content file.
5. Compare with Quartz 5 documentation.
6. Apply one small fix.
7. Verify the result.

Repository state is authoritative. Do not assume Quartz 4 behavior on this Quartz 5 site.
