# sysung.github.io

A modern, fast, and content-driven single-page developer portfolio built using the **Astro** framework. 

All project cards on the front page are dynamically generated from Markdown files, making it incredibly simple to keep your portfolio up-to-date.

---

## 🚀 Quick Start

Start the local development server:
```bash
npm run dev
```
* Your site will be live at [http://localhost:4321](http://localhost:4321).
* Any changes you make will instantly reload in the browser.

---

## 📝 How to Update Your Portfolio

### 1. Add or Edit Projects
To add a new project card or modify an existing one, navigate to the **`src/content/projects/`** directory.

Create a new Markdown file (e.g. `my-awesome-tool.md`) and include this frontmatter configuration block at the very top:

```yaml
---
title: "My Awesome Tool"
description: "A short, engaging description of what you built."
tags: ["Astro", "TypeScript", "Vanilla CSS"]
link: "https://mycoolapp.com"
github: "https://github.com/sysung/my-repository"
featured: true
order: 3
---

Your markdown details go here. You can write in-depth notes, bullet points,
or explanations about the project.
```

* **`order`**: Used to sort project cards on the page (lower numbers display first).
* **`featured`**: A boolean flag to prioritize display.

---

## 🎨 Customizing Design & Layout

* **Global Styling**: Edit colors, typography, gradients, glassmorphism filters, and responsive sizes in `src/styles/global.css`.
* **Page Layout**: Change the header, footer, or dynamic light/dark theme persistence code inside `src/layouts/Layout.astro`.
* **Front Page Structure**: Customize the hero section text, grid layout, or contact banner inside `src/pages/index.astro`.

---

## 📦 Build & Automated Deployment

### Local Production Build
Test compiling the production build locally:
```bash
npm run build
```
Static files will compile into the `dist/` directory.

### Automatic GitHub Pages Deploy
This repository has an automated **GitHub Action** set up in `.github/workflows/deploy.yml`.

Whenever you push changes to your `main` branch:
1. GitHub automatically runs the build pipeline.
2. The compiled static HTML/CSS is pushed directly to your `gh-pages` branch.
3. Your live portfolio at **`https://sysung.github.io/`** is updated within seconds!
