# Mermaid Sequence Diagram Renderer

> A zero-dependency, client-side tool for authoring and exporting [Mermaid](https://mermaid.js.org/) diagrams — live in your browser.

## Live Demo

**[View the POC → https://russelsese.github.io/mermaid-sequence-viewer/](https://russelsese.github.io/mermaid-sequence-viewer/)**

> Open the link above on a mobile device or use your browser's DevTools to emulate a mobile screen (390px width recommended) for the best experience.

---

## Overview

**Mermaid Sequence Diagram Renderer** is a single-page web application that lets you write Mermaid diagram definitions and instantly see the rendered output. There is no backend, no build step, and no installation required — open `index.html` and start diagramming.

---

## Features

| Feature | Details |
|---|---|
| **Live Preview** | Diagram re-renders automatically as you type (300 ms debounce) |
| **Autosave** | Input is persisted to `localStorage` — your work survives page refreshes |
| **Light / Dark Mode** | Respects your OS preference; toggle manually at any time |
| **Export — TXT** | Save the raw Mermaid definition as a `.txt` file |
| **Export — SVG** | Download the rendered diagram as a scalable vector graphic |
| **Export — PNG** | Download or copy the rendered diagram as a rasterised PNG |

---

## Getting Started

No installation or build step is needed.

1. Clone or download this repository.
2. Open `index.html` in any modern browser.
3. Type or paste a Mermaid diagram definition into the editor on the left.
4. The rendered diagram appears instantly on the right.

```
git clone https://github.com/russelsese/mermaid-sequence-viewer.git
cd mermaid-sequence-viewer
open index.html        # macOS
start index.html       # Windows
xdg-open index.html   # Linux
```

---

## Usage

### Writing Diagrams

The editor accepts any valid [Mermaid diagram syntax](https://mermaid.js.org/intro/). The default example is a simple sequence diagram:

```
sequenceDiagram
    participant User
    participant App
    participant API

    User->>App: Click Login
    App->>API: Authenticate
    API-->>App: Token
    App-->>User: Logged in
```

### Exporting

Use the action buttons below the editor:

- **Download TXT** — saves the raw diagram definition text.
- **Download SVG** — saves the rendered diagram as an SVG file.
- **Download PNG** — rasterises the SVG and downloads it as a PNG.
- **Copy PNG** — copies the PNG directly to your clipboard (requires a browser that supports the [Clipboard API](https://developer.mozilla.org/en-US/docs/Web/API/Clipboard_API)).

Files are named with an ISO timestamp, e.g. `mermaid-seq-diag-2026-02-21T10-30-00-000Z.png`.

### Theme Toggle

Click the **Dark / Light** button in the header to switch themes. The preference is saved to `localStorage` and restored on the next visit.

---

## Technical Details

| Property | Value |
|---|---|
| **Runtime dependencies** | [Mermaid.js v10](https://cdn.jsdelivr.net/npm/mermaid@10/) (CDN) |
| **Build dependencies** | None |
| **Backend** | None — fully client-side |
| **Storage** | `localStorage` only |
| **Browser support** | Any modern browser with ES2020+ support |

---

## Project Structure

```
mermaid-sequence-viewer/
└── index.html      # Complete application — markup, styles, and logic
```

---

## Author

Made by [russelsese](https://github.com/russelsese).

---

## License

This project is open source. See the repository for license details.
