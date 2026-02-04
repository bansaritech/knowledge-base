# Markdown Basics

MkDocs uses standard Markdown syntax. Here's a comprehensive guide.

## Text Formatting

### Basic Formatting

```markdown
**Bold text**
*Italic text*
***Bold and italic***
~~Strikethrough~~
`Inline code`
```

**Renders as:**

**Bold text**
*Italic text*
***Bold and italic***
~~Strikethrough~~
`Inline code`

## Headings

```markdown
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

Use headings to create a clear document structure. The Table of Contents is automatically generated from headings.

## Links

### Internal Links

```markdown
[Link to another page](../faq.md)
[Link to a section](#headings)
[Link with title](../about.md "About Page")
```

### External Links

```markdown
[External Link](https://example.com)
[Link opens in new tab](https://example.com){target=_blank}
```

### Reference Links

```markdown
[MkDocs][mkdocs-link] is a great tool.

[mkdocs-link]: https://www.mkdocs.org
```

## Lists

### Unordered Lists

```markdown
- Item 1
- Item 2
  - Nested item 2.1
  - Nested item 2.2
- Item 3
```

- Item 1
- Item 2
  - Nested item 2.1
  - Nested item 2.2
- Item 3

### Ordered Lists

```markdown
1. First item
2. Second item
   1. Nested item 2.1
   2. Nested item 2.2
3. Third item
```

1. First item
2. Second item
   1. Nested item 2.1
   2. Nested item 2.2
3. Third item

### Task Lists

```markdown
- [x] Completed task
- [ ] Incomplete task
- [ ] Another task
```

- [x] Completed task
- [ ] Incomplete task
- [ ] Another task

## Blockquotes

```markdown
> This is a blockquote.
> It can span multiple lines.
>
> > Nested blockquotes are also possible.
```

> This is a blockquote.
> It can span multiple lines.
>
> > Nested blockquotes are also possible.

## Horizontal Rules

```markdown
---
```

---

## Paragraphs

Separate paragraphs with a blank line:

```markdown
This is the first paragraph.

This is the second paragraph.
```

For a line break without a new paragraph, end the line with two spaces or use `<br>`.

## Escaping Characters

Use backslash to escape special characters:

```markdown
\*Not italic\*
\# Not a heading
\[Not a link\]
```

\*Not italic\*
\# Not a heading
\[Not a link\]

## HTML in Markdown

You can use HTML when Markdown isn't enough:

```html
<div style="text-align: center">
  <strong>Centered bold text</strong>
</div>
```

## Summary Table

| Element | Syntax |
|---------|--------|
| Bold | `**text**` |
| Italic | `*text*` |
| Code | `` `code` `` |
| Link | `[text](url)` |
| Image | `![alt](url)` |
| Heading | `# Heading` |
| List | `- item` |
| Quote | `> quote` |

## Next Steps

- Learn [Advanced Formatting](advanced-formatting.md)
- See [Code Examples](code-examples.md)
