# Anti-Patterns

Avoid these patterns when using this skill.

## Existing-System Drift

Do not inspect or describe an existing codebase. If the user points to current
files, services, repositories, current architecture, boundary review, or mixed
existing/proposed context, use `senior-architect-agent`.

## Treating Proposals as Implementation

Do not write as though a proposed module, workflow, data model, or integration
exists. Prefer "Proposed" and "would" until the user approves the direction.

## Diagram-First Work

Do not make diagrams the main output. Mermaid is optional editable source for
review, not the product of the skill.

## Document Bloat

Do not produce exhaustive enterprise architecture documentation for a raw idea.
Keep the proposal reviewable.

## Premature Service Splitting

Do not split modules into services unless scale, ownership, deployment,
compliance, or integration boundaries justify it.

## Hidden Assumptions

Do not bury assumptions inside prose. Put them in an assumptions section or table.

## Ignoring Approval Points

Do not let major product, compliance, payment, tenancy, or security decisions
pass as default choices.
