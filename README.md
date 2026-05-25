# nocentino.dev

Personal website of Jake Nocentino. Built with [Astro](https://astro.build) and [Tailwind CSS](https://tailwindcss.com), deployed to GitHub Pages via GitHub Actions.

## Stack

- **Framework:** Astro 5
- **Styles:** Tailwind CSS 3
- **Language:** TypeScript
- **Deployment:** GitHub Actions → GitHub Pages

## Development

```bash
npm install
npm run dev      # start dev server at localhost:4321
npm run build    # production build → dist/
npm run preview  # preview production build locally
```

## Structure

```
src/
  components/   Nav, Hero, About, Experience, Projects, BlogPreview, Footer
  content/blog/ Markdown blog posts
  layouts/      Base HTML layout
  pages/        index, blog/index, blog/[slug]
public/         Static assets (images, favicon, CNAME)
.github/
  workflows/    deploy.yml — builds and deploys on push to master
```

## Adding content

- **Bio / Skills:** `src/components/About.astro`
- **Jobs:** `src/components/Experience.astro`
- **Projects:** `src/components/Projects.astro`
- **Blog posts:** add a `.md` file to `src/content/blog/` with frontmatter:

```yaml
---
title: "Post title"
date: 2025-01-01
description: "One-line summary"
categories: ["category"]
---
```

## Deployment

Push to `master`. GitHub Actions builds the Astro site and deploys to GitHub Pages automatically. Make sure GitHub Pages source is set to **GitHub Actions** in repo settings.
