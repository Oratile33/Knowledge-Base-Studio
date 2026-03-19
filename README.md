# KBA Studio — Knowledge Base Article Editor

A fully-featured WYSIWYG HTML editor built specifically for authoring knowledge base articles. Export clean, standalone HTML files ready for upload to your KBA management system.

---

## Getting Started

1. Open `index.html` in any modern browser (Chrome, Firefox, Edge, Safari).
2. Start typing in the editor area, or pick a **template** to get a head start.
3. When finished, hit **Export** to download your article as a self-contained `.html` file.

---

## Interface Overview

| Area | Description |
|---|---|
| **Top Bar** | Document title, Import, Templates, Shortcuts reference, and Export button |
| **Toolbar** | All formatting and insertion tools (scrollable on mobile) |
| **Editor** | The main WYSIWYG writing area |
| **Sidebar** | Document Outline (auto-generated from headings) and Metadata panel |
| **Status Bar** | Word count, character count, reading time estimate, article status badge |

---

## Features

### Text Formatting
- **Bold** / **Italic** / **Underline** / **Strikethrough** via toolbar or standard shortcuts
- **Subscript** and **Superscript**
- **Text color** and **highlight color** pickers
- **Clear Formatting** button (eraser icon) to reset selected text

### Block Formats
- Paragraph, Heading 1–4, Blockquote, Code Block — selectable from the dropdown
- **Code blocks** support `Tab` for indentation and `Shift+Enter` to exit the block

### Lists & Alignment
- Bullet (unordered) and numbered (ordered) lists
- Indent / Outdent for nested list levels
- Left, Center, Right, and Justify alignment

### Inserting Content
- **Links** — Opens a dialog for URL and display text
- **Images** — Opens a dialog for image URL and alt text
- **Tables** — Choose rows, columns, and whether to include a header row
- **Horizontal Rule** — Inserts a visual divider
- **Callout Blocks** — Four types: Info, Warning, Success, Danger (click the message icon dropdown)

### Table Editing
When your cursor is inside a table, a **context bar** appears with:
- Add Row Above / Below
- Add Column Left / Right
- Delete Row / Delete Column / Delete Table

### Templates
Click **Templates** in the top bar to choose from six pre-built structures:

| Template | Use Case |
|---|---|
| How-To Guide | Step-by-step task instructions |
| FAQ Article | Question and answer format |
| Troubleshooting | Diagnose and resolve issues |
| Release Notes | Document version changes |
| Policy / Process | Internal policies or SOPs |
| General Article | Flexible all-purpose format |

> Selecting a template will replace current editor content (with a confirmation prompt if content exists).

### Find & Replace
- Open with the magnifying glass icon or `Ctrl+H`
- Matches are highlighted in the editor as you type
- Navigate between matches with the arrow buttons
- Replace one at a time or all at once

### Source Code View
- Toggle the `</>` button to switch between WYSIWYG and raw HTML view
- Edit HTML directly, then toggle back to see the rendered result

### Document Metadata (Sidebar → Metadata tab)
Fill in optional metadata that gets embedded in the exported HTML as comments:
- **Author** — Article author name
- **Category** — Topic category (e.g., Networking, Security)
- **Tags** — Comma-separated keywords
- **Version** — Article version number
- **Status** — Draft, In Review, or Published (also shown in the status bar)
- **Notes** — Internal notes (not visible in the published article body)

### Import HTML
- Click **Import** in the top bar
- Paste raw HTML into the text area, **or** click "Load .html file" to open an existing file
- Click **Import** to load it into the editor

---

## Export

Click the **Export** button (or press `Ctrl+S`) to download the article as a standalone `.html` file.

The exported file includes:
- Full `<!DOCTYPE html>` document structure
- Embedded CSS with professional documentation styling
- Google Fonts (Source Serif 4, DM Sans, JetBrains Mono)
- Responsive layout (mobile-friendly)
- Print-friendly styles
- Article metadata in an HTML comment block at the top of `<head>`

The filename is auto-generated from your document title.

### Copy HTML to Clipboard
Press `Ctrl+Shift+C` to copy the raw inner HTML of the editor to your clipboard — useful for pasting directly into a CMS.

---

## Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Ctrl+B` | Bold |
| `Ctrl+I` | Italic |
| `Ctrl+U` | Underline |
| `Ctrl+K` | Insert Link |
| `Ctrl+H` | Find & Replace |
| `Ctrl+S` | Export HTML |
| `Ctrl+Shift+C` | Copy HTML to Clipboard |
| `Ctrl+1` – `Ctrl+4` | Heading 1–4 |
| `Ctrl+0` | Paragraph |
| `Tab` | Indent (inside code blocks) |
| `Shift+Enter` | Exit code block |

> On macOS, use `Cmd` instead of `Ctrl`.

---

## Dark Mode

The editor automatically detects your system's color scheme preference. No manual toggle is needed — switch your OS or browser to dark mode and the editor follows.

---

## Browser Compatibility

Tested on modern versions of:
- Google Chrome
- Mozilla Firefox
- Microsoft Edge
- Safari

---

## Notes

- All work is **in-memory only**. There is no auto-save to disk. Export your article regularly.
- The editor uses `contentEditable` and `document.execCommand` for formatting, which is widely supported in current browsers.
- Exported HTML files are completely self-contained and do not depend on any external JavaScript.
