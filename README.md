# viwer

A tiny, single-file Markdown viewer. Open `index.html` in a browser, drop a `.md` file, read it.

No build step, no server, no upload — the file never leaves your machine.

## Features

- Drag & drop or file picker (`.md`, `.markdown`, `.txt`)
- GitHub-flavoured Markdown: tables, task lists, footnotes, strikethrough
- Syntax highlighting for code blocks + one-click copy button
- Auto-generated outline sidebar from headings
- Light / dark theme (remembers your choice, follows system by default)
- Print / Save as PDF with a clean print stylesheet
- Output sanitised with DOMPurify

## Usage

```bash
git clone https://github.com/prakhar1605/viwer.git
cd viwer
open index.html        # macOS
# xdg-open index.html  # Linux
```

## Shortcuts

| Key | Action |
|---|---|
| `Cmd/Ctrl + O` | Open a file |
| `Cmd/Ctrl + P` | Print / save as PDF |

## Notes

Rendering libraries (`marked`, `DOMPurify`, `highlight.js`) load from jsDelivr, so the first
open needs internet. Want it fully offline? Download those three files into a `vendor/`
folder and point the `<script>` tags there.

## License

MIT
