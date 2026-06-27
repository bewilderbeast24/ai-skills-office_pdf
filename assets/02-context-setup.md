# Step: 02-context-setup

## Description
This stage involves loading the relevant code snippets, templates, and library configurations based on the selected mode.

## Purpose
- Gather the necessary technical assets for execution.
- Verify library availability in the environment.
- Prepare the environment for the specialized workflow.

## Pre-stage Checkpoint
### Version Control
- N/A.

## Workflow
### Process
1. Based on the selected mode, identify the required reference files:
    - Basic/Extraction/Creation -> [python-snippets.md](../references/python-snippets.md)
    - Advanced/JS -> [js-snippets.md](../references/js-snippets.md)
    - CLI Tools -> [cli-commands.md](../references/cli-commands.md)
2. Read the selected reference files to load the required code patterns into context.
3. Check for the existence of required Python packages (`pypdf`, `pdfplumber`, `reportlab`, `pypdfium2`) or CLI tools (`qpdf`, `pdftotext`).

### Output Format
- Code snippets and library status loaded into context.

## Post-stage Checkpoint
### Version Control
- N/A.

### Human in the Loop (HITL)
- Inform the user of the libraries and snippets being used.

### Auto pilot
- Proceed automatically if all required libraries are present.
