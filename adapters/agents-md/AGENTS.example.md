# Idea To Architecture Agent

Use `idea-to-architecture-agent` when an AI agent must turn a raw idea, product
concept, feature request, or business goal into a reviewable architecture
proposal.

## Use When

- The user provides a raw idea without an existing implementation.
- The work needs assumptions, open questions, risks, decision options, module
  proposals, workflow proposals, or data model drafts.
- The output must remain proposed until approved.

## Do Not Use When

- Existing project files or current architecture must be inspected.
- The work mixes existing-system evidence with proposed future changes.
- The user needs current-state architecture maps or file responsibility maps.

Use `senior-architect-agent` for those cases.

## Rules

- Preserve user intent.
- Ask architecture-impacting questions.
- Continue with explicit assumptions when safe.
- Mark modules, workflows, data models, integrations, and boundaries as
  proposed until approved.
- Do not present proposed architecture as confirmed implementation.
- Keep Markdown as documentation source of truth.
- Keep Mermaid as editable diagram source.

## Handoff

End proposal work with:

- user-provided facts
- assumptions
- proposed architecture
- unknowns
- risks
- decisions requiring approval
- safe next actions
