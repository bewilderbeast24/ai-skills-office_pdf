# Step: 04-outcome

## Description
This stage involves validating the final output and confirming task completion.

## Purpose
- Ensure the output meets the user's requirements.
- Validate visual integrity (especially for form filling or creation).
- Cleanup and handover.

## Pre-stage Checkpoint
### Version Control
- N/A.

## Workflow
### Process
1. For PDFs: Convert the first few pages (or all relevant pages) to images using `pdftoppm` or `pypdfium2` to verify layout and content.
2. For data extraction: Check the first few lines of the output file (TXT, JSON, etc.) to ensure data was captured correctly.
3. Present the final result to the user.
4. If the user is satisfied, delete any temporary files (intermediate PNGs, JSONs).

### Output Format
- Final validated PDF or data file.

## Post-stage Checkpoint
### Version Control
- Commit changes if requested by the user.

### Human in the Loop (HITL)
- Ask for user feedback on the result.

### Auto pilot
- Finalize if the output file exists and validation checks pass.
