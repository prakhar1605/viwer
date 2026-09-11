# viwer

A single-file viewer for Markdown and PDF. Open a file, read it. Nothing is uploaded, nothing is stored.

**[viwer-sigma.vercel.app](https://viwer-sigma.vercel.app/)**

There is no build step, no bundler and no server — `index.html` is the whole application.
Open it from disk and it works exactly the same as the hosted version.

## Why

Most Markdown previewers want you to install an editor, sign in, or paste your document
into someone else's server. This one is a page you open. Your file is read by the browser's
`FileReader` and rendered locally; it never leaves the machine.

## Features

- Drag and drop, or open with <kbd>⌘O</kbd> / <kbd>Ctrl+O</kbd>
- Markdown and PDF in the same window — the file type is detected for you
- GitHub-flavoured Markdown — tables, task lists, strikethrough, fenced code
- Syntax highlighting with a copy button on every code block
- PDFs render page by page, fitted to the window and redrawn when you resize
- Outline sidebar generated from headings, highlighting the section you are reading
- Works on a phone: the outline becomes a slide-over, tables and code scroll on their own
- Light or dark, remembered between visits
- Print or save to PDF with the interface stripped out
- Rendered HTML sanitised with DOMPurify

## Run it

```bash
git clone https://github.com/prakhar1605/viwer.git
cd viwer
open index.html          # macOS
# xdg-open index.html    # Linux
# start index.html       # Windows
```

To host your own copy, point any static host at the repository root. No configuration needed.

## Keyboard

| Key | Action |
|---|---|
| <kbd>⌘O</kbd> / <kbd>Ctrl+O</kbd> | Open a file |
| <kbd>⌘P</kbd> / <kbd>Ctrl+P</kbd> | Print or save as PDF |

## Built on

[marked](https://github.com/markedjs/marked) for parsing,
[DOMPurify](https://github.com/cure53/DOMPurify) for sanitising,
[highlight.js](https://github.com/highlightjs/highlight.js) for code,
[pdf.js](https://github.com/mozilla/pdf.js) for PDFs (loaded only when you open one).
They come from jsDelivr, so the first open needs a connection. For a fully offline
copy, download them into `vendor/` and repoint the `<script>` tags.

## Contributing

Issues and pull requests are welcome. The whole app is one file, so:

1. Edit `index.html`
2. Open it in a browser and check light mode, dark mode, and a narrow window
3. Open a PR describing what changed and why

Keep it dependency-light and keep it to a single file — that constraint is the point.

## License

MIT — see [LICENSE](LICENSE).
