# idea-to-architecture-agent

`idea-to-architecture-agent` is a standalone Codex skill for turning raw ideas,
product concepts, feature requests, and business/system goals into reviewable
architecture proposals.

It is question-first and proposal-first. It preserves user intent, exposes
assumptions and unknowns, and marks architecture content as proposed until
approved.

## Scope

This skill produces Markdown proposal docs and Mermaid diagram sources.

Use it for:

- Raw product ideas without implementation.
- Feature concepts that need architecture options.
- Business or system goals that need module boundaries, workflows, risks, and
  approval points.
- Handoff notes for a future implementation agent.

For existing systems, mixed existing/proposed context, boundary review, or
current architecture work, use `senior-architect-agent`.

## Repository Layout

```text
.
|-- SKILL.md
|-- agents/openai.yaml
|-- docs/
|-- templates/
`-- examples/tennis-court-booking/
```

## Source Format

Markdown is the documentation source of truth. Mermaid files are editable diagram
source. SVG is not required for this skill version.
