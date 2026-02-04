# Advanced Formatting

Beyond basic Markdown, MkDocs supports advanced formatting features.

## Tables

### Basic Table

```markdown
| Header 1 | Header 2 | Header 3 |
|----------|----------|----------|
| Cell 1   | Cell 2   | Cell 3   |
| Cell 4   | Cell 5   | Cell 6   |
```

| Header 1 | Header 2 | Header 3 |
|----------|----------|----------|
| Cell 1   | Cell 2   | Cell 3   |
| Cell 4   | Cell 5   | Cell 6   |

### Column Alignment

```markdown
| Left | Center | Right |
|:-----|:------:|------:|
| L    | C      | R     |
| 1    | 2      | 3     |
```

| Left | Center | Right |
|:-----|:------:|------:|
| L    | C      | R     |
| 1    | 2      | 3     |

### Complex Table

| Feature | Free | Pro | Enterprise |
|:--------|:----:|:---:|:----------:|
| Basic Support | Yes | Yes | Yes |
| Advanced Features | No | Yes | Yes |
| Priority Support | No | No | Yes |
| Price | $0 | $10/mo | $50/mo |

## Definition Lists

```markdown
Term 1
:   Definition for term 1

Term 2
:   Definition for term 2
:   Another definition for term 2
```

Term 1
:   Definition for term 1

Term 2
:   Definition for term 2
:   Another definition for term 2

## Footnotes

```markdown
Here is a sentence with a footnote[^1].

[^1]: This is the footnote content.
```

Here is a sentence with a footnote[^1].

[^1]: This is the footnote content.

## Abbreviations

```markdown
The HTML specification is maintained by the W3C.

*[HTML]: Hyper Text Markup Language
*[W3C]: World Wide Web Consortium
```

The HTML specification is maintained by the W3C.

*[HTML]: Hyper Text Markup Language
*[W3C]: World Wide Web Consortium

## Keyboard Keys

Show keyboard shortcuts:

```markdown
Press <kbd>Ctrl</kbd> + <kbd>C</kbd> to copy.
Press <kbd>Cmd</kbd> + <kbd>V</kbd> to paste.
```

Press <kbd>Ctrl</kbd> + <kbd>C</kbd> to copy.
Press <kbd>Cmd</kbd> + <kbd>V</kbd> to paste.

## Subscript and Superscript

```markdown
H<sub>2</sub>O is water.
E = mc<sup>2</sup>
```

H<sub>2</sub>O is water.
E = mc<sup>2</sup>

## Highlighting

```markdown
==This text is highlighted==
```

Or using HTML:

<mark>This text is highlighted</mark>

## Collapsible Sections

```html
<details>
<summary>Click to expand</summary>

This content is hidden by default.

- Item 1
- Item 2
- Item 3

</details>
```

<details>
<summary>Click to expand</summary>

This content is hidden by default.

- Item 1
- Item 2
- Item 3

</details>

## Admonitions (with extensions)

If using Material theme or pymdownx extensions:

```markdown
!!! note
    This is a note admonition.

!!! warning
    This is a warning.

!!! tip
    This is a helpful tip.

!!! danger
    This is dangerous!
```

## Custom Containers

Using HTML divs for custom styling:

```html
<div class="warning">
  <strong>Warning:</strong> Be careful with this operation.
</div>
```

## Emoji (with extension)

```markdown
:smile: :rocket: :thumbsup:
```

## Math Equations (with extension)

Inline: `$E = mc^2$`

Block:

```markdown
$$
\frac{n!}{k!(n-k)!} = \binom{n}{k}
$$
```

## Best Practices

1. **Use semantic markup** - Choose elements that convey meaning
2. **Keep tables simple** - Complex data might need a different format
3. **Test rendering** - Preview your docs frequently
4. **Be consistent** - Use the same patterns throughout

## Required Extensions

Add these to `mkdocs.yml` for full support:

```yaml
markdown_extensions:
  - tables
  - footnotes
  - def_list
  - abbr
  - attr_list
  - pymdownx.mark
  - pymdownx.details
  - pymdownx.emoji
  - pymdownx.arithmatex
```
