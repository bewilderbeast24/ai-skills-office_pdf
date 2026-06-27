---
name: office-pdf
description: Use when you need a comprehensive suite for PDF manipulation, extraction, creation, and form filling. It uses Python and JavaScript tools.
---

# PDF Processing
  
## Skill Overview
This skill provides a standardized workflow for various PDF operations, including basic manipulations (merge, split), advanced data extraction (text, tables, images), programmatic PDF creation, and complex form filling. It serves as a centralized hub for PDF-related tasks, routing to specific workflows and code assets based on the user's needs.

## Workflow Sequence

| Stage | Description | Workflow |
| :--- | :--- | :--- |
| **1. Mode Selection** | Identify the required PDF operation and select the corresponding mode. | [01-mode-selection.md](assets/01-mode-selection.md) |
| **2. Context Setup** | Load necessary snippets, templates, and library configurations. | [02-context-setup.md](assets/02-context-setup.md) |
| **3. Specialized Workflow** | Execute the chosen operation (Basic, Extraction, Creation, Forms, or Advanced). | [03-specialized-workflow.md](assets/03-specialized-workflow.md) |
| **4. Outcome** | Verify the results and finalize the task. | [04-outcome.md](assets/04-outcome.md) |

## Pre-stage Checkpoint
- **Human in the Loop (HITL)**: Default mode. The agent will confirm the selected mode and plan before proceeding asking for user confirmation whenever user is to be kept in loop.
- **Autopilot**: If explicitly requested, the agent will autonomously select the best tool/library for the task and execute the workflow.

## Core Operation Flow

### Stage 1: Mode Selection
Analyze the user's request or use `ask_user` to select a mode:
- **Basic Operations**: Merging, splitting, rotating, or metadata.
- **Extraction**: Extracting text, tables, images, or coordinates.
- **Creation**: Generating new PDFs programmatically.
- **Form Filling**: Filling out fillable or non-fillable forms.
- **Advanced/JS**: High-performance or JavaScript-based tasks.

### Stage 2: Context Setup
Load references based on selection:
- [python-snippets.md](references/python-snippets.md)
- [js-snippets.md](references/js-snippets.md)
- [cli-commands.md](references/cli-commands.md)
- [form-filling-workflow.md](references/form-filling-workflow.md)

### Stage 3: Specialized Workflow
Follow the procedures in [03-specialized-workflow.md](assets/03-specialized-workflow.md).

### Stage 4: Outcome
Finalize per [04-outcome.md](assets/04-outcome.md).

## Handover & Confirmation
- All PDF operations are verified for correctness.
- Temporary files are cleaned up.
- Final PDF/Data is presented to the user.

## Additional Instructions
All temporary scripts generated while execution of skills (scripts which will be deleted after execution) will be written in `.gemini/skills-diary/temp-scripts/<timestamp>/`.
