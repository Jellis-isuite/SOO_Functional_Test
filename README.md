# SOO Review & Functional Test Builder

A free, single-page web tool for commissioning and controls engineers. Paste or open a
**sequence of operations** (`.docx` or `.pdf`) and it will:

1. Split it into individual requirements and match each to an equipment-specific test library.
2. Pull setpoints, delays and limits from the SOO into the test steps.
3. Review the SOO for missing functions, undefined values and untestable wording.
4. Export a functional test script as an **Excel (.xlsx)** workbook.

**Privacy:** everything runs in your browser. Documents are never uploaded anywhere, and the tool works offline once the page has loaded.

## Use it

Open the published page: `https://<your-username>.github.io/<repo-name>/`
(or download `index.html` and double-click it – it is a single self-contained file).

### PDF notes
- PDFs need selectable text. Scanned (image-only) PDFs must be OCR'd first.
- By default the tool keeps only the sequence-of-operations text and skips images, schematics, title blocks and sheet indexes. Untick *"PDFs: keep only the sequence-of-operations text"* to extract everything.
- Multi-column drawing sheets are read column by column. Always skim the extracted text before clicking **Analyze & generate**.

## Publish your own copy (GitHub Pages)
1. Create a new public repository and upload the files in this folder.
2. **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main`, folder `/ (root)`.
3. After a minute the site is live at the URL above.

## Maintainer features
Open the page with `?admin` at the end of the URL (e.g. `.../index.html?admin`) to show the **Admin log-in** button.
Admin mode lets you correct test-library mappings and publish an updated `index.html` that carries those corrections;
commit that file to update the public site. The admin button is hidden from normal visitors.

## Important
The built-in test templates are **drafts** written from public commissioning practice. They must be reviewed by the
responsible engineer before use on a project. No warranty is given (see `LICENSE`).

## License
MIT for this tool (see `LICENSE`). Embedded PDF.js is Apache-2.0 (see `NOTICE.md`).
