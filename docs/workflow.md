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

## 2. Extract Intent

Identify:

- Primary outcome
- Users or actors
- Business goal
- System goal
- Constraints and non-goals
- Success signals

## 3. Ask Questions

Ask only architecture-impacting questions. Prefer fewer, sharper questions.

Use assumptions when the answer can be safely revised later. Pause for approval
when the answer changes boundaries, data ownership, compliance, cost, payment
flow, or security posture.

## 4. State Assumptions

Document assumptions before proposing architecture.

Each assumption should include:

- Assumption
- Why it is being made
- Impact if wrong
- Whether approval is required

## 5. Propose Architecture

Label every item as proposed.

Cover:

- Proposed modules
- Proposed boundaries
- Proposed integrations
- Proposed decision options
- Proposed tradeoffs

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

Run the validation gate from `SKILL.md`.

## 10. Report

End with:

- What was produced
- What is assumed
- What needs approval
- What remains unknown
- Safe next actions
