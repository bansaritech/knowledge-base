# Images and Media

How to include images, diagrams, and media in your MkDocs documentation.

## Basic Images

### Inline Image

```markdown
![Alt text](path/to/image.png)
```

### Image with Title

```markdown
![Alt text](path/to/image.png "Image title on hover")
```

### Image from URL

```markdown
![MkDocs Logo](https://www.mkdocs.org/img/favicon.ico)
```

## Image Organization

### Recommended Structure

```
docs/
├── images/
│   ├── screenshots/
│   │   ├── dashboard.png
│   │   └── settings.png
│   ├── diagrams/
│   │   ├── architecture.png
│   │   └── flow.png
│   └── logos/
│       ├── logo-dark.png
│       └── logo-light.png
├── index.md
└── guide.md
```

### Reference Images

From the same directory:

```markdown
![Screenshot](./screenshot.png)
```

From images folder:

```markdown
![Dashboard](../images/screenshots/dashboard.png)
```

## Image Sizing (HTML)

### Fixed Width

```html
<img src="../images/logo.png" alt="Logo" width="200">
```

### Fixed Height

```html
<img src="../images/logo.png" alt="Logo" height="100">
```

### Percentage Width

```html
<img src="../images/banner.png" alt="Banner" style="width: 100%;">
```

### Max Width

```html
<img src="../images/photo.png" alt="Photo" style="max-width: 500px;">
```

## Image Alignment

### Centered Image

```html
<p align="center">
  <img src="../images/centered.png" alt="Centered">
</p>
```

### Float Left

```html
<img src="../images/icon.png" alt="Icon" align="left" style="margin-right: 10px;">
Text flows around the image on the right side.
```

### Float Right

```html
<img src="../images/icon.png" alt="Icon" align="right" style="margin-left: 10px;">
Text flows around the image on the left side.
```

## Image Galleries

### Side by Side (Table)

| Screenshot 1 | Screenshot 2 |
|--------------|--------------|
| ![Screen 1](https://via.placeholder.com/200x150) | ![Screen 2](https://via.placeholder.com/200x150) |
| Dashboard view | Settings panel |

### Grid Layout (HTML)

```html
<div style="display: flex; flex-wrap: wrap; gap: 10px;">
  <img src="img1.png" width="200">
  <img src="img2.png" width="200">
  <img src="img3.png" width="200">
</div>
```

## Figures with Captions

### Using HTML

```html
<figure>
  <img src="../images/architecture.png" alt="System Architecture">
  <figcaption>Figure 1: System Architecture Overview</figcaption>
</figure>
```

<figure>
  <img src="https://via.placeholder.com/400x200" alt="Example">
  <figcaption>Figure 1: Example placeholder image</figcaption>
</figure>

## Diagrams

### ASCII Diagrams

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│   Client    │────▶│   Server    │────▶│  Database   │
└─────────────┘     └─────────────┘     └─────────────┘
       │                   │
       │                   │
       ▼                   ▼
┌─────────────┐     ┌─────────────┐
│    Cache    │     │    Queue    │
└─────────────┘     └─────────────┘
```

### Mermaid Diagrams (with plugin)

If you have the mermaid plugin installed:

    ```mermaid
    graph TD
        A[Start] --> B{Is it working?}
        B -->|Yes| C[Great!]
        B -->|No| D[Debug]
        D --> B
    ```

### Flowchart

```
Start
  │
  ▼
┌───────────┐
│  Input    │
└─────┬─────┘
      │
      ▼
┌───────────┐     No
│ Validate  │─────────┐
└─────┬─────┘         │
      │ Yes           │
      ▼               ▼
┌───────────┐   ┌───────────┐
│  Process  │   │   Error   │
└─────┬─────┘   └───────────┘
      │
      ▼
┌───────────┐
│  Output   │
└───────────┘
      │
      ▼
    End
```

## Videos

### YouTube Embed

```html
<iframe
  width="560"
  height="315"
  src="https://www.youtube.com/embed/VIDEO_ID"
  frameborder="0"
  allowfullscreen>
</iframe>
```

### Local Video

```html
<video width="640" height="360" controls>
  <source src="../videos/demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```

## GIFs

Animated GIFs work like regular images:

```markdown
![Demo Animation](../images/demo.gif)
```

## SVG Images

SVG files are well-supported and scale perfectly:

```markdown
![Vector Logo](../images/logo.svg)
```

Or inline:

```html
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" fill="#007bff"/>
</svg>
```

## Screenshots Best Practices

1. **Consistent size** - Use same dimensions for similar screenshots
2. **Highlight important areas** - Add boxes or arrows
3. **Compress images** - Use tools like ImageOptim or TinyPNG
4. **Use PNG for UI** - Better quality for text and sharp edges
5. **Use JPG for photos** - Smaller file size for photographic images
6. **Add borders** - Helps screenshots stand out from the page

## Image Optimization

### Recommended Formats

| Format | Best For | Typical Use |
|--------|----------|-------------|
| PNG | Screenshots, diagrams, logos | UI images with text |
| JPG | Photos, complex images | Hero images, backgrounds |
| SVG | Icons, logos, diagrams | Scalable graphics |
| GIF | Simple animations | Short demos |
| WebP | General purpose | Modern alternative to PNG/JPG |

### File Size Guidelines

- Thumbnails: < 50 KB
- Regular images: < 200 KB
- Large images: < 500 KB
- Hero images: < 1 MB
