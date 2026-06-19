[README (1).md](https://github.com/user-attachments/files/29148012/README.1.md)
# Claude-Powered Nonprofit Intake & Resource-Routing Workflow

A public-interest Claude workflow prototype showing how a small nonprofit could turn messy intake notes into structured summaries, resource-routing categories to review, follow-up questions, and staff handoff notes — while keeping humans responsible for final decisions.

**Status:** Complete prototype using synthetic sample notes only.  
**Built for:** Claude Corps application portfolio.  
**Core idea:** Use AI to reduce administrative burden without replacing frontline staff judgment.

## Problem

Small nonprofits and community-resource organizations often collect intake information through phone calls, walk-ins, forms, texts, and staff notes. That information can be messy, incomplete, and difficult to hand off between staff members.

The risk is not just inefficiency. A missed detail can delay help, route someone to the wrong service category, or create confusion about next steps. At the same time, using AI in intake work creates its own risks: hallucinated facts, privacy exposure, overconfident referrals, and staff relying on a model when a human needs to verify eligibility, urgency, or safety.

This prototype explores a practical middle ground: Claude helps organize intake information, but staff remain accountable for review, routing, and final decisions.

## What this workflow does

Given a synthetic, de-identified intake note, the workflow helps a staff member:

1. Convert unstructured notes into a structured summary.
2. Separate confirmed facts from assumptions or missing information.
3. Identify likely resource-routing categories to review.
4. Draft respectful follow-up questions.
5. Create an internal staff handoff note.
6. Run a quality and safety review before anyone relies on the output.

## What is included in this repo

| File | Purpose |
| --- | --- |
| `Claude_Powered_Nonprofit_Intake_Workflow_Prototype.md` | Markdown version of the full project overview for easy GitHub viewing. |
| `Claude_Powered_Nonprofit_Intake_Workflow_Prototype.pdf` | Polished PDF work sample. |
| `prompt_chain.md` | Step-by-step Claude prompts for intake structuring, routing, follow-up questions, handoff notes, and safety review. |
| `project_runbook.md` | Non-technical instructions for using and maintaining the workflow. |
| `human_review_checklist.md` | Checklist staff should complete before using any AI-assisted output. |
| `failure_case.md` | Example of how the workflow can go wrong and the correction rule. |
| `resource_routing_taxonomy.csv` | Resource categories, examples, minimum information needed, and human-review risks. |
| `sample_intake_notes.md` | Synthetic intake notes for workforce, housing/food access, and healthcare navigation cases. |
| `sample_outputs.md` | Example before/after outputs showing how a messy note becomes a structured handoff. |

## How a non-technical staff member would use it

1. Start with a de-identified intake note.
2. Run Prompt 1 to create a structured summary.
3. Run Prompt 2 to identify possible resource categories to review.
4. Run Prompt 3 to draft follow-up questions.
5. Run Prompt 4 to create a staff handoff note.
6. Run Prompt 5 to audit the output for hallucinations, unsupported claims, privacy issues, tone problems, and legal/medical/benefits risks.
7. Complete the human review checklist before taking action.

The intended user is not a developer. The workflow is written for staff who need clear steps, cautious defaults, and plain-language review instructions.

## Human review and safety limits

This workflow is designed around human accountability. Claude should not decide eligibility, promise benefits, diagnose needs, provide legal or medical advice, or make final referrals.

Staff must verify:

- Program eligibility and service area.
- Urgent safety, medical, housing, or legal issues.
- Personally identifiable information handling.
- Whether the suggested category is only a possibility, not a confirmed referral.
- Whether the final handoff note is accurate, respectful, and useful.

## What this prototype does not do

This is not:

- Production software.
- A deployed app.
- A benefits eligibility engine.
- A replacement for trained staff.
- Legal, medical, housing, immigration, or benefits advice.
- A system using real client data.

It is a documented Claude workflow prototype using synthetic data.

## Why this matters for Claude Corps

Claude Corps Fellows are expected to scope messy organizational problems, build practical Claude workflows, teach non-technical users, document handoffs, and exercise judgment about when AI should or should not be used.

This project was built to demonstrate that loop:

- **Scope:** Intake notes are messy, incomplete, and difficult to hand off.
- **Build:** A Claude prompt chain turns notes into structured summaries, routing categories, follow-up questions, and handoff notes.
- **Enable:** The workflow is written for non-technical staff.
- **Hand off:** The repo includes a runbook, checklist, taxonomy, and sample outputs.
- **Exercise judgment:** The failure case shows how overconfident AI routing can mislead staff, and the correction rule keeps AI suggestions within safe bounds.

## Future improvements

- Test the workflow with staff from a real nonprofit or community-resource organization.
- Add a simple form-to-sheet workflow for structured intake capture.
- Create a short training deck or video walkthrough for non-technical staff.
- Add more failure cases and review rules.
- Build a version tailored to bilingual English/Spanish intake support.
- Create a lightweight evaluation checklist comparing AI-assisted handoffs against human-only notes.

## Repository description

Public-interest Claude workflow prototype for nonprofit intake summarization, resource-routing support, human review, and staff handoff.
