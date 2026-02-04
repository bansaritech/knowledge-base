# Configuration Guide

All MkDocs configuration lives in a single file: `mkdocs.yml`

## Basic Configuration

```yaml
# Site information
site_name: My Documentation
site_url: https://example.com
site_description: Project documentation
site_author: Your Name

# Repository information
repo_name: username/repo
repo_url: https://github.com/username/repo

# Theme settings
theme:
  name: readthedocs
```

## Navigation Configuration

### Simple Navigation

```yaml
nav:
  - Home: index.md
  - About: about.md
  - Contact: contact.md
```

### Nested Navigation

```yaml
nav:
  - Home: index.md
  - User Guide:
    - Getting Started: guide/getting-started.md
    - Installation: guide/installation.md
    - Configuration: guide/configuration.md
  - API:
    - Overview: api/overview.md
    - Reference: api/reference.md
  - About: about.md
```

### Section Index Pages

```yaml
nav:
  - User Guide:
    - guide/index.md  # Section landing page
    - Installation: guide/installation.md
    - Usage: guide/usage.md
```

## Theme Configuration

### ReadTheDocs Theme

```yaml
theme:
  name: readthedocs
  # Custom settings
  prev_next_buttons_location: bottom
  style_external_links: true
  collapse_navigation: true
  sticky_navigation: true
```

### Material Theme

```yaml
theme:
  name: material
  palette:
    primary: indigo
    accent: indigo
  features:
    - navigation.tabs
    - navigation.sections
    - toc.integrate
    - search.suggest
```

## Markdown Extensions

```yaml
markdown_extensions:
  # Table of contents with permalinks
  - toc:
      permalink: true
      toc_depth: 3

  # Tables support
  - tables

  # Fenced code blocks with syntax highlighting
  - fenced_code

  # Footnotes
  - footnotes

  # Definition lists
  - def_list

  # Abbreviations
  - abbr
```

## Plugins

```yaml
plugins:
  - search:
      lang: en
  - minify:
      minify_html: true
```

## Extra Settings

```yaml
extra:
  # Social links
  social:
    - icon: fontawesome/brands/github
      link: https://github.com/username
    - icon: fontawesome/brands/twitter
      link: https://twitter.com/username

  # Version
  version: 1.0.0

  # Analytics
  analytics:
    provider: google
    property: G-XXXXXXXXXX
```

## Environment Variables

You can use environment variables in your config:

```yaml
site_url: !ENV [SITE_URL, 'https://example.com']
```

## Complete Example

```yaml
site_name: My Project
site_url: https://myproject.com
site_description: Complete project documentation
site_author: John Doe

repo_name: johndoe/myproject
repo_url: https://github.com/johndoe/myproject
edit_uri: edit/main/docs/

theme:
  name: readthedocs
  locale: en

nav:
  - Home: index.md
  - Getting Started:
    - Installation: getting-started/installation.md
    - Quick Start: getting-started/quickstart.md
  - User Guide:
    - Basics: user-guide/basics.md
    - Advanced: user-guide/advanced.md
  - API Reference: api/reference.md
  - FAQ: faq.md

markdown_extensions:
  - toc:
      permalink: true
  - tables
  - fenced_code

plugins:
  - search

extra:
  version: 1.0.0
```

## Configuration Validation

Check your configuration for errors:

```bash
mkdocs build --strict
```

This will fail if there are any configuration issues.
