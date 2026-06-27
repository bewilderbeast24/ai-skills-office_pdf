# Step: 01-mode-selection

## Description
This stage involves identifying the user's specific PDF processing requirement and selecting the appropriate operational mode.

## Purpose
- Determine the user's intent.
- Map the request to a specialized workflow.
- Ensure the correct tools and libraries are identified.

## Pre-stage Checkpoint
### Version Control
- Ensure the workspace is clean: `git status`.
- Do not make any changes yet.

## Workflow
### Process
1. Analyze the user's request for keywords related to PDF operations (e.g., "merge", "extract", "fill form", "create").
2. If the request is ambiguous, use `ask_user` to present the following options:
    - **Basic Operations**: Merging, splitting, rotating, or metadata.
    - **Extraction**: Extracting text, tables, images, or coordinates.
    - **Creation**: Generating new PDFs programmatically.
    - **Form Filling**: Filling out fillable or non-fillable forms.
    - **Advanced/JS**: High-performance or JavaScript-based tasks.
3. Capture the selected mode.

### Output Format
- Selected mode stored in agent's context.

## Post-stage Checkpoint
### Progress Tracking
- Update `.agents/skills-diary/pdf-processing/[<instance-name>]/checklist.md` by marking the 'Mode Selection' stage as completed.

### Version Control
- N/A (no files modified).

### Human in the Loop (HITL)
- Confirm the selected mode with the user before proceeding to context setup.

### Auto pilot
- If the user's request is unambiguous (e.g., "Merge these two PDFs"), automatically select the corresponding mode and proceed.
