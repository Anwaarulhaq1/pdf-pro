# Contributing

Thanks for helping improve PDF Pro Viewer.

## Development

This is currently a static app with no build step.

```bash
python3 -m http.server 8000 --directory .
```

Open `http://localhost:8000/index.html`.

## Pull requests

- Keep changes focused and small.
- Describe the user-facing behavior you changed.
- Test importing at least one PDF before submitting UI or file-loading changes.
- Do not commit API keys, credentials, sample private documents, or generated browser storage.

## Feature ideas

Good first areas:

- Accessibility improvements.
- Local OCR experiments with open-source libraries.
- PDF text search.
- Better folder/library management.
- Automated browser smoke tests.
