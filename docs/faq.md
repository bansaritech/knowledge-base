# Frequently Asked Questions

Common questions and answers about using MkDocs.

---

## General Questions

### What is MkDocs?

MkDocs is a fast, simple static site generator that's geared towards building project documentation. Documentation source files are written in Markdown, and configured with a single YAML configuration file.

### Why use MkDocs over other documentation tools?

**Advantages of MkDocs:**

- Simple setup and configuration
- Fast build times
- Live preview server
- Easy deployment to GitHub Pages
- Large ecosystem of themes and plugins
- Pure Python (easy to extend)

### What are the alternatives?

| Tool | Language | Best For |
|------|----------|----------|
| MkDocs | Python | Project documentation |
| Sphinx | Python | Python projects, extensive docs |
| Jekyll | Ruby | Blogs, general sites |
| Docusaurus | JavaScript | React-based projects |
| GitBook | JavaScript | Commercial documentation |
| Hugo | Go | Speed-critical sites |

---

## Installation & Setup

### How do I install MkDocs?

```bash
pip install mkdocs
```

For the Material theme:

```bash
pip install mkdocs-material
```

### What Python version is required?

MkDocs requires Python 3.8 or higher.

### Can I use MkDocs without Python knowledge?

Yes! Basic usage only requires:

- Editing Markdown files
- Basic YAML configuration
- Running a few terminal commands

---

## Configuration

### Where do I configure MkDocs?

All configuration is in `mkdocs.yml` at the root of your project.

### How do I add navigation?

```yaml
nav:
  - Home: index.md
  - About: about.md
  - User Guide:
    - Getting Started: guide/start.md
    - Advanced: guide/advanced.md
```

### How do I change the theme?

```yaml
theme:
  name: material  # or 'readthedocs', etc.
```

### Can I use custom CSS?

Yes, add to `mkdocs.yml`:

```yaml
extra_css:
  - stylesheets/custom.css
```

Then create `docs/stylesheets/custom.css`.

---

## Writing Content

### What Markdown flavor does MkDocs use?

MkDocs uses Python-Markdown with extensions. It's compatible with CommonMark with some additions.

### How do I link between pages?

```markdown
[Link to page](other-page.md)
[Link to section](other-page.md#section-heading)
```

### How do I add images?

```markdown
![Alt text](images/screenshot.png)
```

### Can I use HTML in Markdown?

Yes, HTML is supported:

```html
<div class="custom">
  Custom HTML content
</div>
```

### How do I add code with syntax highlighting?

Use fenced code blocks with language identifier:

    ```python
    def hello():
        print("Hello, World!")
    ```

---

## Building & Deploying

### How do I build the site?

```bash
mkdocs build
```

This creates a `site/` directory with static HTML files.

### How do I preview locally?

```bash
mkdocs serve
```

Then open http://127.0.0.1:8000 in your browser.

### How do I deploy to GitHub Pages?

```bash
mkdocs gh-deploy
```

This builds and pushes to the `gh-pages` branch automatically.

### Can I deploy elsewhere?

Yes! After `mkdocs build`, the `site/` folder can be deployed to:

- Netlify
- Vercel
- AWS S3
- Any static hosting

---

## Troubleshooting

### Build fails with "page not found"

Check that:

1. Files exist in the `docs/` directory
2. File paths in `nav` match actual files
3. File extensions are `.md`

### Live reload not working

Try:

1. Clear browser cache
2. Restart `mkdocs serve`
3. Check for syntax errors in `mkdocs.yml`

### Theme not applying

Ensure:

1. Theme is installed: `pip install mkdocs-material`
2. Theme name is correct in `mkdocs.yml`
3. Run `mkdocs build --clean`

### Broken links after deployment

Check:

1. `site_url` is set correctly
2. Use relative links: `[link](../page.md)`
3. Case sensitivity on server

---

## Advanced Topics

### How do I add search?

Search is built-in. Configure in `mkdocs.yml`:

```yaml
plugins:
  - search:
      lang: en
```

### Can I use multiple languages?

Yes, with the `i18n` plugin:

```bash
pip install mkdocs-i18n
```

### How do I add versioning?

Use the `mike` plugin for version management:

```bash
pip install mike
mike deploy 1.0
mike deploy 2.0 latest
```

### Can I include external Markdown files?

With the `include` plugin:

```bash
pip install mkdocs-include-markdown-plugin
```

---

## Getting Help

### Where can I find more documentation?

- [Official MkDocs Docs](https://www.mkdocs.org)
- [Material Theme Docs](https://squidfunk.github.io/mkdocs-material/)

### Where do I report bugs?

- [MkDocs GitHub Issues](https://github.com/mkdocs/mkdocs/issues)

### Is there a community?

- Stack Overflow: Tag `mkdocs`
- GitHub Discussions
- Discord servers for documentation
