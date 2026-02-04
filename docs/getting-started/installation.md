# Installation Guide

This page demonstrates a typical **installation guide** format with modern styling.

---

## Prerequisites

!!! warning "Before You Begin"

    Ensure you have the following installed on your system:

    - [x] Python 3.8 or higher
    - [x] pip (Python package manager)
    - [ ] Git (optional, for version control)

Check your Python version:

```bash
python --version
```

---

## Installation Methods

=== "pip (Recommended)"

    The simplest way to install MkDocs:

    ```bash
    pip install mkdocs
    ```

    For the Material theme:

    ```bash
    pip install mkdocs-material
    ```

=== "pipx (Isolated)"

    Install in an isolated environment:

    ```bash
    pipx install mkdocs
    pipx inject mkdocs mkdocs-material
    ```

=== "From Source"

    Clone and install from source:

    ```bash
    git clone https://github.com/mkdocs/mkdocs.git
    cd mkdocs
    pip install .
    ```

---

## Verify Installation

```bash
mkdocs --version
```

Expected output:

```
mkdocs, version 1.5.x from /path/to/site-packages/mkdocs
```

!!! success "Installation Complete"

    If you see the version number, MkDocs is installed correctly!

---

## Installing Themes

### Material Theme :material-palette:

The most popular MkDocs theme with modern features.

```bash
pip install mkdocs-material
```

Configure in `mkdocs.yml`:

```yaml title="mkdocs.yml"
theme:
  name: material
  palette:
    primary: indigo
    accent: indigo
  features:
    - navigation.tabs
    - navigation.sections
    - content.code.copy
```

### ReadTheDocs Theme

The classic documentation theme:

```yaml title="mkdocs.yml"
theme:
  name: readthedocs
```

---

## Optional Extensions

Enhance your documentation with these extensions:

| Extension | Purpose | Install Command |
|:----------|:--------|:----------------|
| `pymdown-extensions` | Advanced Markdown | `pip install pymdown-extensions` |
| `mkdocs-minify-plugin` | Minify HTML | `pip install mkdocs-minify-plugin` |
| `mkdocs-git-revision-date-plugin` | Show last updated | `pip install mkdocs-git-revision-date-plugin` |

---

## Troubleshooting

??? question "Command not found: mkdocs"

    Add Python scripts to your PATH:

    === "Linux/macOS"

        ```bash
        export PATH="$HOME/.local/bin:$PATH"
        ```

    === "Windows"

        Add `%USERPROFILE%\AppData\Local\Programs\Python\Python3x\Scripts` to PATH

??? question "Permission denied during install"

    Use the `--user` flag:

    ```bash
    pip install --user mkdocs
    ```

??? question "Python version error"

    Upgrade Python to 3.8 or higher:

    === "Ubuntu/Debian"

        ```bash
        sudo apt update
        sudo apt install python3.10
        ```

    === "macOS"

        ```bash
        brew install python@3.10
        ```

    === "Windows"

        Download from [python.org](https://www.python.org/downloads/)

---

## Getting Help

!!! info "Need assistance?"

    - :material-book: Check the [FAQ](../faq.md)
    - :material-github: Search [GitHub Issues](https://github.com/mkdocs/mkdocs/issues)
    - :material-stack-overflow: Ask on [Stack Overflow](https://stackoverflow.com/questions/tagged/mkdocs)

---

## Next Steps

<div class="grid" markdown>

<div class="card" markdown>

### :rocket: Quick Start

Create your first documentation project.

[Quick Start Guide :material-arrow-right:](quickstart.md)

</div>

<div class="card" markdown>

### :gear: Configuration

Learn about all configuration options.

[Configuration Guide :material-arrow-right:](configuration.md)

</div>

</div>
