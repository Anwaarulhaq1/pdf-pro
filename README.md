# PDF Pro Viewer

PDF Pro Viewer is a browser-based document library for PDF, TMP, and common Adobe file formats. It stores files locally in your browser with IndexedDB, opens PDF-family files in the native browser PDF viewer, and keeps other Adobe files organized with clear metadata even when the browser cannot preview them directly.

## Features

- Load individual files or full folders.
- Supports PDF/TMP plus many Adobe-family extensions including Acrobat forms/data (`.fdf`, `.xdp`, `.xfdf`), Illustrator (`.ai`, `.ait`, `.eps`, `.ps`), Photoshop (`.psd`, `.psb`, `.abr`, `.acv`, `.atn`, `.pat`, `.grd`, `.asl`, `.csh`, `.tpl`), InDesign/InCopy (`.indd`, `.indt`, `.indb`, `.inx`, `.idml`, `.icml`), After Effects (`.aep`, `.aepx`, `.aet`), Premiere Pro/Motion Graphics (`.prproj`, `.prfpset`, `.mogrt`), Audition (`.sesx`), XD (`.xd`), Animate/Flash (`.fla`, `.xfl`, `.swf`), Lightroom/Camera Raw (`.dng`, `.lrcat`, `.lrtemplate`, `.xmp`), Digital Editions (`.acsm`), and ExtendScript (`.jsx`, `.jsxbin`).
- Search, sort, filter by folder, resize/collapse the sidebar, and navigate with keyboard shortcuts.
- Persist files across browser sessions using local IndexedDB storage.
- Preview PDF-family files directly in the browser.
- Store and list native Adobe formats with file type badges and clear unsupported-preview messaging.
- Optional Nanonets OCR snipping for PDF/TMP files if you provide your own API key and model ID.

## Format support

Browsers can reliably preview PDF files and many `.tmp` files that contain PDF data. Native Adobe project/source formats such as Photoshop, Illustrator, InDesign, Premiere Pro, After Effects, XD, Flash, and PostScript-derived files are imported and listed, but they generally require Adobe desktop apps or specialized converters for editing or full preview.

## OCR

OCR is optional. The current app includes Nanonets OCR for selected PDF/TMP snips when the user adds their own API key and model ID in settings. A future open-source path could add local OCR with projects such as [Tesseract.js](https://github.com/naptha/tesseract.js), but that is intentionally not bundled yet to keep this static app lightweight.

## Run locally

No build step is required.

```bash
python3 -m http.server 8000 --directory .
```

Then open `http://localhost:8000/index.html`.

## Privacy

Files are stored in your browser's local IndexedDB for this site. They are not uploaded anywhere unless you use the optional OCR feature, which sends the selected snip image to Nanonets.

## Roadmap

- Add local open-source OCR with Tesseract.js as an opt-in module.
- Add text search inside PDFs.
- Add bookmarks, annotations, rotate, split, merge, and export tools.
- Add import/export of library metadata.
- Add PWA/offline install support.
- Split the app into maintainable JavaScript/CSS modules with tests and CI.

## Contributing

Contributions are welcome. Please open an issue first for larger changes so the scope and UX can be discussed.

## License

MIT
