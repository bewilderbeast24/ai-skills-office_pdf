# CLI Commands for PDF Processing

## Poppler-Utils

### pdftotext
```bash
pdftotext -layout input.pdf output.txt
pdftotext -bbox-layout input.pdf output.xml
```

### pdftoppm (Render)
```bash
pdftoppm -png -r 300 input.pdf prefix
```

### pdfimages (Extract)
```bash
pdfimages -all input.pdf prefix
```

## qpdf

### Merge
```bash
qpdf --empty --pages file1.pdf file2.pdf -- merged.pdf
```

### Split
```bash
qpdf input.pdf --pages . 1-5 -- pages1-5.pdf
```

### Decrypt
```bash
qpdf --password=pwd --decrypt encrypted.pdf decrypted.pdf
```
