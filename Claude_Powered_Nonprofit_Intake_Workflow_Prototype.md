# Claude-Powered Nonprofit Intake & Resource Routing Workflow

**Public-Interest AI Workflow Prototype | Built for Claude Corps Evidence Packet**

| Field | Details |
| --- | --- |
| Project | Claude-Powered Nonprofit Intake & Resource Routing Workflow |
| Type | Self-directed public-interest AI workflow prototype |
| Status | Complete prototype using synthetic intake notes; no real client data |
| Use case | Helping non-technical nonprofit staff summarize intake, identify needs, route resources, and create handoff notes |

## 1. Executive Summary

This prototype demonstrates how a small nonprofit or community-resource organization could use Claude to reduce intake administration while preserving human judgment. The workflow converts messy intake notes into a structured case summary, identifies likely need categories, flags missing information, drafts follow-up questions, and creates a staff handoff note. It is intentionally lightweight: a non-technical staff member can run it with a prompt chain, checklist, and runbook rather than production software.

- Designed for workforce-development, community-resource, student-support, or social-service intake teams.
- Uses synthetic intake notes only; no real client data or personally identifiable information is included.
- Keeps the human reviewer accountable for accuracy, eligibility decisions, tone, privacy, and final routing.
- Includes a failure case and review checkpoints to show where AI output must be corrected or rejected.

## 2. Problem and User

Small public-interest organizations often receive unstructured client notes from calls, walk-ins, emails, or referral forms. Staff need to understand the actual need, decide the next step, and document handoff details quickly. This prototype addresses the administrative friction without automating final decisions.

| User | Pain Point | Workflow Support |
| --- | --- | --- |
| Intake coordinator | Notes are messy and incomplete | Structured summary + missing-info flags |
| Case manager | Needs quick routing and follow-up questions | Need categories + suggested next actions |
| Program manager | Needs consistency across staff | Repeatable prompt chain + review checklist |
| Executive / grant lead | Needs responsible AI adoption evidence | Runbook + privacy limitations + failure logging |

## 3. Workflow Overview

1. Intake note enters the workflow. Staff paste a de-identified note into Claude using the intake prompt.
2. Claude produces a structured summary: situation, stated needs, constraints, urgency, and possible resources.
3. Claude flags missing information and writes human-friendly follow-up questions.
4. Staff review the output against the checklist and correct errors, unsupported claims, or overly confident language.
5. Staff use the handoff note internally, never as an automated eligibility decision or replacement for caseworker judgment.

## 4. Prompt Chain

### Prompt 1 - Intake Structuring

> You are helping a nonprofit intake coordinator. Convert the de-identified intake note into a structured summary. Do not invent facts. Separate confirmed facts from assumptions. Flag missing information. Use plain language.

### Prompt 2 - Need Identification and Routing

> Classify the client needs into resource categories such as housing stability, employment, food access, transportation, healthcare navigation, benefits navigation, education/training, childcare, language access, or legal referral. Provide a confidence level and explain what evidence supports each category.

### Prompt 3 - Follow-Up Questions

> Write 5-8 respectful follow-up questions a staff member should ask. Prioritize information needed for safe routing. Avoid intrusive questions unless necessary for service eligibility or safety.

### Prompt 4 - Staff Handoff Note

> Draft an internal staff handoff note. Include: short case summary, likely needs, immediate next step, missing information, caution flags, and human-review reminders. Keep tone factual and non-judgmental.

### Prompt 5 - Quality and Safety Review

> Audit the draft. Identify hallucinations, unsupported claims, sensitive data risks, tone problems, legal/medical/benefits risks, and places where staff judgment is required. Recommend corrections before use.

## 5. Sample Before/After Outputs

### Sample A - Workforce Support

**Messy intake note:** Client recently lost part-time work after childcare schedule changed. Behind on phone bill, worried about missing job interview calls, wants short training program but cannot attend evenings. Has reliable bus access only on weekdays.

**Structured output:** Resource categories: employment support, childcare referral, transportation constraint, benefits/navigation. Follow-up: preferred training schedule, current childcare options, zip code/service area, eligibility for workforce program, urgency of phone service. Handoff: prioritize workforce navigator plus childcare resource list; do not promise eligibility.

### Sample B - Student Housing and Food Access

**Messy intake note:** College student says financial aid refund is delayed, couch-surfing with friend, skipping meals, and unsure whether school has emergency help. Works weekends and speaks Spanish at home.

**Structured output:** Resource categories: emergency aid, food access, housing stability, bilingual support. Follow-up: campus affiliation, safe place tonight, food pantry access, financial aid contact, consent to connect with student services. Handoff: urgent but non-emergency; staff should verify campus resources and avoid legal/benefits claims.

### Sample C - Healthcare Navigation

**Messy intake note:** Parent missed clinic appointment because of transportation and language barriers. Needs help rescheduling and understanding paperwork. No medical advice requested.

**Structured output:** Resource categories: healthcare navigation, language access, transportation, appointment support. Follow-up: preferred language, clinic contact, appointment urgency, transportation options, consent. Handoff: staff can support scheduling and interpretation resources; Claude must not provide medical advice.

## 6. Human Review Checklist

- **Accuracy:** Did Claude stay within the note, or did it infer facts not provided?
- **Eligibility:** Did Claude avoid promising program eligibility or benefits outcomes?
- **Tone:** Is the output respectful, plain-language, and non-judgmental?
- **Privacy:** Has real personally identifiable information been removed before use?
- **Risk:** Are urgent safety, medical, legal, or housing issues routed to qualified staff or emergency protocols?
- **Handoff:** Could another staff member understand the next step without re-reading the full intake note?
- **Failure logging:** Did staff record any AI mistake so the workflow can improve?

## 7. Failure Case and Correction

**Failure case:** Claude may over-route a client to legal aid or benefits programs based on vague language such as “paperwork problem” or “lost job.” This is risky because it can imply eligibility or create false confidence.

**Correction rule:** Claude may suggest “possible resource category to verify,” but staff must confirm the actual issue, service area, eligibility, and urgency before giving the client a referral.

**Example correction:** Replace “Client should apply for emergency rental assistance” with “Ask whether the client has a lease, current notice, income documentation, and service-area eligibility; then check whether emergency rental assistance is available.”

## 8. Runbook and Handoff Notes

1. Use only de-identified or synthetic notes. Remove names, dates of birth, addresses, phone numbers, medical IDs, and case numbers before using Claude.
2. Paste the intake note into Prompt 1 and review the structured summary for accuracy.
3. Run Prompts 2-4 only after correcting the summary; otherwise later outputs compound early mistakes.
4. Run Prompt 5 before using or sharing the handoff note.
5. A human staff member must approve all client-facing communication, eligibility guidance, and referrals.
6. Update the prompt chain when staff identify repeated errors, confusing outputs, or missing categories.
7. Keep a simple error log: date, input type, issue, correction, and whether the runbook/prompt was updated.

## 9. Claude Corps Relevance

- **Discover and scope:** Translates a messy social-service intake problem into a repeatable workflow.
- **Build with Claude:** Uses a prompt chain, resource taxonomy, sample outputs, and review checkpoints.
- **Enable the organization:** Written for non-technical staff and includes training-friendly examples.
- **Hand off well:** Includes a runbook, checklist, failure case, and maintenance notes.
- **Exercise judgment:** Explicitly limits AI use around privacy, eligibility, medical/legal risk, and unsupported claims.

## Appendix A - Resource Routing Taxonomy

| Category | Examples | Minimum Info Needed | Human Review Risk |
| --- | --- | --- | --- |
| Employment / Workforce | Job search, resume support, training programs | Work authorization if relevant, schedule, skills, location | Avoid promising placement |
| Housing Stability | Shelter, rental help, eviction prevention | Current safe housing, notice/deadline, service area | Legal/benefits eligibility must be verified |
| Food Access | Food pantry, meal programs, SNAP navigation | Household size, location, urgency | Benefits claims require verification |
| Healthcare Navigation | Appointments, insurance navigation, interpretation | Urgency, provider, language preference | No medical advice |
| Transportation | Bus passes, ride programs, appointment transport | Location, schedule, eligibility | Do not guarantee availability |
| Education / Training | GED, certifications, college support | Program goal, schedule, prerequisites | Verify admissions/aid requirements |
| Childcare / Family Support | Childcare referrals, school schedule issues | Ages, schedule, location, urgency | Safety protocols apply |
| Language Access | Interpretation, translated materials | Preferred language, context, confidentiality | Use qualified interpreter where needed |
| Legal Referral | Benefits denial, eviction notice, immigration issue | Document type, deadline, location | Never provide legal advice |

## Appendix B - Resume-Ready Project Bullets

- Designed a Claude-powered nonprofit intake workflow converting synthetic unstructured client notes into structured summaries, resource-routing categories, follow-up questions, and staff handoff notes.
- Created a runbook for non-technical staff covering prompt steps, review checkpoints, privacy cautions, failure cases, and when human judgment must override AI output.
- Built before/after examples and a resource-routing taxonomy to demonstrate responsible AI adoption for workforce, housing, food access, healthcare navigation, and benefits-support scenarios.
