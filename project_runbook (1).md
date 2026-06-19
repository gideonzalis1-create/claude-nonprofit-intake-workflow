# Project Runbook

## Purpose

This runbook explains how a non-technical nonprofit staff member could use the Claude-Powered Nonprofit Intake & Resource-Routing Workflow prototype.

The goal is not to automate decisions. The goal is to reduce intake administration by turning messy notes into a structured draft that a human can review, correct, and hand off.

## Inputs

Use only de-identified or synthetic intake notes unless the organization has approved policies for using AI tools with sensitive data.

A usable intake note may include:

- What the person asked for.
- Basic context around employment, housing, food, transportation, healthcare navigation, childcare, language access, or benefits navigation.
- Urgency or deadlines.
- Missing information that staff still need to ask about.

Do not include unnecessary personally identifiable information.

## Workflow Steps

### Step 1: Structure the note

Run Prompt 1 from `prompt_chain.md` to turn the messy note into a structured summary. The output should separate confirmed facts, assumptions, and missing information.

### Step 2: Identify possible resource categories

Run Prompt 2 to identify likely resource-routing categories. Claude should present these as categories to review, not final referrals.

### Step 3: Draft follow-up questions

Run Prompt 3 to create respectful follow-up questions that staff can ask before routing the person further.

### Step 4: Draft staff handoff note

Run Prompt 4 to create a concise internal handoff note. The note should include the case summary, likely needs, immediate next step, missing information, and caution flags.

### Step 5: Review for quality and safety

Run Prompt 5 to audit the output. Staff should then complete `human_review_checklist.md` before taking action.

## Review Checkpoints

Before using the AI-assisted output, staff should ask:

- Did Claude invent any facts?
- Did Claude imply eligibility without proof?
- Did Claude make a legal, medical, or benefits recommendation?
- Did Claude miss urgent safety, housing, medical, or legal issues?
- Is the tone respectful and non-judgmental?
- Could another staff member understand the next step?

## Privacy Cautions

- Do not paste real names, addresses, phone numbers, Social Security numbers, medical record details, or other unnecessary sensitive data into an AI tool.
- Follow the organization's data policies and tool terms before using AI with any real intake content.
- When in doubt, use synthetic or de-identified notes.

## When Human Judgment Must Override AI

Human staff must make the final decision when the case involves:

- Benefits eligibility.
- Legal issues, including eviction, immigration, or benefits denials.
- Medical advice or urgent health situations.
- Safety concerns, domestic violence, abuse, or crisis intervention.
- Housing deadlines or court notices.
- Any situation where Claude's output is uncertain, overconfident, or not supported by the note.

## Maintenance Notes

To keep the workflow useful:

- Add new failure cases when staff find problems.
- Update the routing taxonomy when programs or categories change.
- Remove prompts that produce unclear or unsafe outputs.
- Keep the workflow short enough for a new staff member to learn quickly.
- Review the tool's privacy and data-use policies before using real data.
