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

### Font Family
- **Built-in font dropdown** in the toolbar with sans-serif, serif, and monospace options
- Select text and choose a font to apply it, or pick a font before typing
- Available families include DM Sans, Arial, Verdana, Calibri, Source Serif 4, Georgia, Times New Roman, Cambria, JetBrains Mono, Courier New, and more

### Custom Font Upload
Upload your organisation's proprietary fonts directly into the editor:

1. Click the **⬆ upload** icon next to the font dropdown in the toolbar
2. Select a font file — supported formats: `.woff`, `.woff2`, `.ttf`, `.otf`
3. The font is loaded instantly via `@font-face` and appears in the **Custom Fonts** section of the dropdown
4. Select text and choose your custom font, or start typing with it selected
5. A **font info bar** appears below the toolbar confirming the loaded font, with a **Remove** button to unregister it

**Export with embedded fonts:** When you export to HTML, any uploaded custom fonts are automatically embedded as base64 `@font-face` rules. The exported file is completely self-contained — recipients see the correct font without needing the font file installed.

> **Tip:** `.woff2` files are recommended for the smallest export size.

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

---

## Import

Click **Import** in the top bar to open the Import Document dialog. Two file types are supported:

### Import DOCX (Word Documents)
Convert Microsoft Word `.docx` files to HTML directly in the browser using [mammoth.js](https://github.com/mwilliamson/mammoth.js):

1. Click the **`.docx file`** button and select your Word document
2. The file is converted entirely client-side — nothing leaves your machine
3. Converted HTML appears in the preview textarea for review and optional editing
4. Click **Import** to load the result into the editor

**What's preserved from DOCX:**
- Headings (H1–H4) and paragraphs
- Bold, italic, underline, strikethrough
- Ordered and unordered lists (including nested)
- Tables
- Links and images (embedded images are converted to base64)
- Blockquotes
- Custom Word styles are mapped to semantic HTML (Title → H1, Heading 1–4, Quote → blockquote, etc.)

**Conversion feedback:**
- A loading spinner is shown during conversion
- Success message with the filename when complete
- If there are minor conversion warnings (e.g., unsupported Word features), they are displayed in a collapsible panel
- Clear error messages for unsupported formats

> **Note:** The legacy `.doc` format (pre-2007 binary format) is **not supported**. If you have a `.doc` file, open it in Word and save it as `.docx` (File → Save As → .docx) before importing.

### Import HTML
- Click the **`.html file`** button and select an HTML file, **or** paste raw HTML directly into the textarea
- If the file is a full HTML document, the body content is extracted automatically
- Review and edit the HTML in the preview textarea before importing

---

## Export

Click the **Export** button (or press `Ctrl+S`) to download the article as a standalone `.html` file.

The exported file includes:
- Full `<!DOCTYPE html>` document structure
- Embedded CSS with professional documentation styling
- Google Fonts (Source Serif 4, DM Sans, JetBrains Mono)
- Any custom uploaded fonts embedded as base64 `@font-face` rules
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

## Dependencies

KBA Studio loads the following external libraries from CDN:
- [Google Fonts](https://fonts.googleapis.com) — Bricolage Grotesque, DM Sans, Source Serif 4, JetBrains Mono
- [Font Awesome 6.5](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css) — Toolbar and UI icons
- [mammoth.js 1.8](https://cdnjs.cloudflare.com/ajax/libs/mammoth/1.8.0/mammoth.browser.min.js) — Client-side DOCX to HTML conversion

All processing happens in the browser. No data is sent to any server.

---

## Notes

- All work is **in-memory only**. There is no auto-save to disk. Export your article regularly.
- The editor uses `contentEditable` and `document.execCommand` for formatting, which is widely supported in current browsers.
- Exported HTML files are completely self-contained and do not depend on any external JavaScript.
- Custom font files are held in memory only for the current session. Re-upload them if you refresh the page.
- DOCX conversion quality depends on the complexity of the original document. Heavily styled or layout-heavy Word files may lose some visual formatting — review the converted HTML before importing.
