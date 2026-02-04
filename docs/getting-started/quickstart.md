# Quick Start Guide

Get your documentation site running in under 5 minutes.

## Step 1: Create a New Project

```bash
mkdocs new my-project
cd my-project
```

This creates the following structure:

```
my-project/
├── mkdocs.yml
└── docs/
    └── index.md
```

## Step 2: Start the Development Server

```bash
mkdocs serve
```

Open your browser to [http://127.0.0.1:8000](http://127.0.0.1:8000)

> **Tip:** The server auto-reloads when you save changes!

## Step 3: Edit Your Content

Open `docs/index.md` and make changes:

```markdown
# Welcome to My Project

This is my awesome documentation!

## Features

- Easy to write
- Beautiful output
- Fast builds
```

## Step 4: Add More Pages

Create new `.md` files in the `docs/` folder:

```bash
touch docs/about.md
touch docs/tutorial.md
```

## Step 5: Configure Navigation

Edit `mkdocs.yml` to define your navigation:

```yaml
site_name: My Project
nav:
  - Home: index.md
  - About: about.md
  - Tutorial: tutorial.md
```

## Step 6: Build for Production

```bash
mkdocs build
```

This creates a `site/` folder with static HTML files ready for deployment.

## Step 7: Deploy to GitHub Pages

```bash
mkdocs gh-deploy
```

Your site is now live at `https://username.github.io/my-project/`

## Summary

| Step | Command | Description |
|------|---------|-------------|
| 1 | `mkdocs new my-project` | Create project |
| 2 | `mkdocs serve` | Start dev server |
| 3 | Edit `.md` files | Add content |
| 4 | `mkdocs build` | Build static site |
| 5 | `mkdocs gh-deploy` | Deploy to GitHub |

## What's Next?

- Learn about [Configuration](configuration.md) options
- Explore [Markdown Basics](../user-guide/markdown-basics.md)
- Check out [Code Examples](../user-guide/code-examples.md)
