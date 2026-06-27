# JavaScript Code Snippets for PDF Processing

## pdf-lib (Node.js)

### Load and Modify
```javascript
import { PDFDocument } from 'pdf-lib';
import fs from 'fs';

async function modify() {
    const bytes = fs.readFileSync('input.pdf');
    const pdfDoc = await PDFDocument.load(bytes);
    const page = pdfDoc.addPage([600, 400]);
    page.drawText('Modified');
    const pdfBytes = await pdfDoc.save();
    fs.writeFileSync('output.pdf', pdfBytes);
}
```

## pdf.js (Browser/Node)

### Extract Text
```javascript
import * as pdfjsLib from 'pdfjs-dist';

async function extract(url) {
    const pdf = await pdfjsLib.getDocument(url).promise;
    const page = await pdf.getPage(1);
    const content = await page.getTextContent();
    console.log(content.items.map(i => i.str).join(' '));
}
```
