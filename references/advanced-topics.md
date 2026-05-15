# Advanced PDF Processing Topics

## Performance Optimization
- **Large PDFs**: Use streaming or `qpdf --split-pages`.
- **Image Extraction**: `pdfimages` is faster than rendering.
- **Memory**: Process in chunks.

## Troubleshooting
- **Encrypted PDFs**: Use `reader.decrypt("pwd")` in pypdf or `qpdf --decrypt`.
- **Corrupted PDFs**: Repair with `qpdf --fix-qdf`.
- **Text Extraction**: Fallback to OCR (`pytesseract`).

## Licenses
- **pypdf**: BSD
- **pdfplumber**: MIT
- **pypdfium2**: Apache/BSD
- **ReportLab**: BSD
- **Poppler**: GPL-2
- **qpdf**: Apache
