# About My Company

This documentation demonstrates various MkDocs features and serves as a template for your projects.

## Purpose

This Knowledge Base showcases:

- Different documentation page types
- Markdown formatting options
- Navigation structure patterns
- Best practices for technical documentation

## Project Structure

```
knowledge-base/
├── mkdocs.yml              # Main configuration
└── docs/
    ├── index.md            # Homepage
    ├── about.md            # This page
    ├── faq.md              # FAQ page
    ├── getting-started/    # Getting started section
    │   ├── installation.md
    │   ├── quickstart.md
    │   └── configuration.md
    ├── user-guide/         # User guide section
    │   ├── markdown-basics.md
    │   ├── advanced-formatting.md
    │   └── code-examples.md
    ├── api/                # API documentation
    │   ├── overview.md
    │   └── endpoints.md
    └── examples/           # Example pages
        ├── tables-lists.md
        └── images-media.md
```

## Page Types Demonstrated

| Page Type    | Example            | Use Case                      |
| ------------ | ------------------ | ----------------------------- |
| Landing Page | `index.md`         | Project overview, quick links |
| Tutorial     | `quickstart.md`    | Step-by-step guides           |
| Reference    | `configuration.md` | Configuration options         |
| API Docs     | `endpoints.md`     | API reference documentation   |
| FAQ          | `faq.md`           | Common questions              |
| Examples     | `code-examples.md` | Code samples, recipes         |

## Features Used

### Navigation

- Multi-level navigation
- Section grouping
- Clear hierarchy

### Markdown

- Headers and sections
- Tables (basic and complex)
- Lists (ordered, unordered, task)
- Code blocks with syntax highlighting
- Links (internal and external)
- Blockquotes
- Definition lists

### Extensions

- Table of Contents with permalinks
- Fenced code blocks
- Tables

## How to Use This Template

1. **Clone or copy** this project structure
2. **Customize** `mkdocs.yml` with your site name and settings
3. **Replace content** in the Markdown files
4. **Add your pages** and update navigation
5. **Preview** with `mkdocs serve`
6. **Deploy** with `mkdocs gh-deploy` or your preferred method

## Quick Commands

```bash
# Start development server
mkdocs serve

# Build static site
mkdocs build

# Deploy to GitHub Pages
mkdocs gh-deploy

# Build with strict mode (shows warnings as errors)
mkdocs build --strict
```

## Recommended Themes

### ReadTheDocs (Default in this project)

```yaml
theme:
  name: readthedocs
```

Simple, clean, widely recognized documentation style.

### Material for MkDocs

```yaml
theme:
  name: material
```

Modern, feature-rich theme with many customization options.

Install with: `pip install mkdocs-material`

## Resources

- [MkDocs Documentation](https://www.mkdocs.org)
- [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
- [Markdown Guide](https://www.markdownguide.org)

## License

This template is provided as-is for educational purposes. Feel free to use and modify for your projects.

## Version

Current version: **1.0.0**

Last updated: February 2024
