# Step: 03-specialized-workflow

## Description
This stage executes the specific PDF operation according to the selected mode and gathered context.

## Purpose
- Perform the requested PDF manipulation or extraction.
- Apply the correct technical implementation (Python, JS, or CLI).
- Handle multi-step processes like form filling.

## Pre-stage Checkpoint
### Version Control
- If creating or modifying files, ensure you are in a state where changes can be tracked.

## Workflow
### Process
1. **Basic Operations**: Use `pypdf` or `qpdf` snippets to merge, split, or rotate PDFs.
2. **Extraction**: Use `pdfplumber` for text/tables or `pdfimages` for embedded assets.
3. **Creation**: Use `ReportLab` (Canvas or Platypus) to build the PDF.
4. **Form Filling**: 
    - Check for fillable fields using `scripts/check_fillable_fields.py`.
    - If fillable: Use `scripts/extract_form_field_info.py` and `scripts/fill_fillable_fields.py`.
    - If non-fillable: Use `scripts/extract_form_structure.py` and `scripts/fill_pdf_form_with_annotations.py`.
    - Refer to [form-filling-workflow.md](../references/form-filling-workflow.md) for detailed steps.
5. **Advanced/JS**: Execute `pypdfium2` scripts or Node.js `pdf-lib` logic.

### Output Format
- Resulting PDF file or extracted data (TXT, JSON, XLSX, CSV).

## Post-stage Checkpoint
### Progress Tracking
- Update `.agents/skills-diary/pdf-processing/[<instance-name>]/checklist.md` by marking the 'Specialized Workflow' stage as completed.

### Version Control
- Verify the generated files: `ls -l <output_file>`.

### Human in the Loop (HITL)
- Provide a summary of the action taken and the location of the output.

### Auto pilot
- Verify the existence and size of the output file. If successful, proceed to outcome.
