# idea-to-architecture-agent

`idea-to-architecture-agent` is an AI architecture proposal skill for turning
raw ideas, product concepts, feature requests, and business goals into
reviewable architecture maps.

It is question-first and proposal-first. It preserves user intent, exposes
assumptions and unknowns, and marks architecture content as proposed until
approved.

## Use When

Use this skill for:

- Raw product ideas without implementation.
- Feature concepts that need architecture options.
- Business or system goals that need module boundaries, workflows, risks, and
  approval points.
- Handoff notes for a future implementation agent.

## Do Not Use When

- Existing project files, codebase structure, or current architecture must be
  inspected.
- The work mixes existing-system evidence with proposed future changes.
- The user needs current-state architecture maps or file responsibility maps.
- The task belongs to broader architecture review, boundary review, or system
  handoff.

For those cases, use
[`senior-architect-agent`](https://github.com/aetox-skills/senior-architect-agent).

## Relationship To Other Skills

This is the focused sibling skill for raw ideas.

Use [`senior-architect-agent`](https://github.com/aetox-skills/senior-architect-agent)
for existing systems, mixed existing/proposed work, architecture boundaries,
risk review, handoff notes, or broader architecture mapping.

## Scope

This skill produces Markdown proposal docs and Mermaid diagram sources.

## Repository Layout

```text
.
|-- SKILL.md
|-- INSTALL.md
|-- agents/openai.yaml
|-- adapters/
|-- docs/
|-- templates/
`-- examples/tennis-court-booking/
```

## Source Format

Markdown is the documentation source of truth. Mermaid files are editable diagram
source. SVG is not required for this skill version.

## Example Outputs

- Tennis court booking proposal:
  [`examples/tennis-court-booking/output/`](examples/tennis-court-booking/output/)

## Install

See [INSTALL.md](INSTALL.md) for Codex, Claude Code, Antigravity, AGENTS.md,
and manual installation notes.

Install this Codex skill from:

```txt
aetox-skills/idea-to-architecture-agent
```

## License

MIT
