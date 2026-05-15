# Form Filling Workflow Reference

## Phase 1: Assessment
1. Run `python scripts/check_fillable_fields.py <file.pdf>`.
2. Determine if the PDF has fillable form fields or if it requires annotations (non-fillable).

## Phase 2A: Fillable Fields
1. **Extract Info**: `python scripts/extract_form_field_info.py <input.pdf> <field_info.json>`.
2. **Visual Check**: `python scripts/convert_pdf_to_images.py <file.pdf> <output_dir>`.
3. **Prepare Values**: Create `field_values.json` matching the extracted `field_id`s.
4. **Fill**: `python scripts/fill_fillable_fields.py <input.pdf> <field_values.json> <output.pdf>`.

## Phase 2B: Non-Fillable Fields (Annotations)
1. **Structure Extraction**: `python scripts/extract_form_structure.py <input.pdf> form_structure.json`.
2. **Approach A (Structure-Based)**: If labels are found, calculate entry coordinates from `form_structure.json`.
3. **Approach B (Visual Estimation)**: If scanned, use `convert_pdf_to_images.py` and crop regions to refine pixel coordinates.
4. **Prepare Fields**: Create `fields.json` with `pdf_width`/`pdf_height` (for A) or `image_width`/`image_height` (for B).
5. **Validate**: `python scripts/check_bounding_boxes.py fields.json`.
6. **Fill**: `python scripts/fill_pdf_form_with_annotations.py <input.pdf> fields.json <output.pdf>`.

## Phase 3: Verification
1. Convert output PDF to images.
2. Verify text placement and readability.
