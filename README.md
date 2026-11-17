# pdf-editor

A single-page PDF text editor that runs entirely in the browser. Open a PDF, click a line of text to retype it, add new text, or cover part of a page, then download the result. Files are not uploaded anywhere.

## Use

Open `index.html` in a browser, or enable GitHub Pages for this repository (Settings → Pages → Deploy from branch → `main`, root) and open the Pages link.

## How it works

- [pdf.js](https://mozilla.github.io/pdf.js/) renders each page and reads the position of its text.
- [pdf-lib](https://pdf-lib.js.org/) writes the edits into a copy of the file.
- Both libraries load from cdnjs, so the page needs an internet connection the first time.

## Limits

- Edited lines are redrawn in Helvetica, Times or Courier, not the document's own font.
- The original text is covered, not removed, so this is not a redaction tool.
- Scanned PDFs have no editable text.
- Password-protected PDFs are saved as page images with the edits drawn on.
- Text outside the Latin alphabet is saved as a picture.
