# Workflow

Use this workflow to convert a raw idea into proposal artifacts without implying
an existing implementation.

## 1. Intake

Capture the raw idea in the user's language.

Separate:

- User-provided facts
- Stated goals
- Stated constraints
- Missing context

Record the initial idea scope so validation can detect proposal expansion.

Run a complexity scan and record grill depth:

- Low: single workflow, no payment, no authentication, no external integration,
  and no regulated data.
- Medium: 2-4 modules, simple integration, or basic roles.
- High: payment, authentication, multi-role access, regulated data,
  multi-service boundaries, or compliance.

Intake gate: pass only when the idea is restated, initial scope is recorded,
and user-provided facts are separated from unknowns.

## 2. Extract Intent

Identify:

- Primary outcome
- Users or actors
- Business goal
- System goal
- Constraints and non-goals
- Success signals

Intent gate: pass only when goals, actors, constraints, and success signals are
identified before questioning.

## 3. Ask Questions

Ask only architecture-impacting questions. Prefer fewer, sharper questions.

Use assumptions when the answer can be safely revised later. Pause for approval
when the answer changes boundaries, data ownership, compliance, cost, payment
flow, or security posture.

Use grill depth to set question volume:

- Low: ask 2-3 questions maximum.
- Medium: ask 4-6 questions.
- High: ask until all boundary-changing unknowns are resolved or explicitly
  deferred with approval.

If the user does not answer, proceed only with assumptions marked `Assumed`
and `Requires approval`; do not present the proposal as approved.

Question gate: pass only when architecture-impacting questions are asked, or
`None required` is written.

## 4. State Assumptions

Document assumptions before proposing architecture.

Each assumption should include:

- Assumption
- Why it is being made
- Impact if wrong
- Whether approval is required

Assumption gate: pass only when every assumption has impact if wrong and
approval status.

## 5. Propose Architecture

Label every item as proposed.

Cover:

- Proposed modules
- Proposed boundaries
- Proposed integrations
- Proposed decision options
- Proposed tradeoffs

Proposal gate: pass only when modules, workflows, data models, integrations,
and boundaries are marked `Proposed` before mapping or drafting detail.

## 6. Map Workflows

Draft proposed workflows from trigger to outcome.

Include:

- Actor
- Trigger
- Steps
- System responsibilities
- Failure paths
- Open questions

## 7. Draft Data Model

Draft proposed entities and relationships.

Call out:

- Ownership
- Sensitive fields
- Audit needs
- Retention questions
- Reporting needs

## 8. Identify Risks

List risks as proposal risks, not existing defects.

Include:

- Risk
- Why it matters
- Mitigation
- Early validation step
- Owner or decision-maker when known

## 9. Validate

Run the five-question validation gate from `SKILL.md` before Report.

Compare final proposal scope to the initial idea scope recorded at Intake. If
the proposal expanded, list what was added and mark each addition as
user-requested, justified by the idea, or requiring approval.

## 10. Report

End with:

- What was produced
- What is assumed
- What needs approval
- What remains unknown
- Safe next actions
