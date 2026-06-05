# Install Idea To Architecture Agent

`idea-to-architecture-agent` is an Aetox skill package. The primary instruction
file is `SKILL.md`.

## Source Of Truth

- `SKILL.md`: core skill instructions for all agents.
- `agents/openai.yaml`: Codex/OpenAI interface metadata only.
- `adapters/agents-md/AGENTS.example.md`: optional project instruction adapter.

## Codex

Install from GitHub:

```txt
aetox-skills/idea-to-architecture-agent
```

Common local skill paths:

```txt
Windows: %USERPROFILE%\.codex\skills\idea-to-architecture-agent
macOS:   ~/.codex/skills/idea-to-architecture-agent
Linux:   ~/.codex/skills/idea-to-architecture-agent
```

Restart Codex after installation so the skill list refreshes.

## Claude Code

Use `SKILL.md` as the project instruction source.

One practical pattern is to add a project `CLAUDE.md` that imports the skill:

```md
# Project Instructions

Use Idea To Architecture Agent when turning raw ideas into reviewable
architecture proposals.

@/absolute/path/to/idea-to-architecture-agent/SKILL.md
```

Use a real absolute path for the machine where Claude Code runs.

## Antigravity Or Other Agent Runtimes

Use the root `SKILL.md` as the skill instruction file when your runtime supports
skills.

If the runtime supports `AGENTS.md`-style project instructions, copy or merge:

```txt
adapters/agents-md/AGENTS.example.md
```

into the target project's `AGENTS.md`.

## Manual Use

Clone the repository and ask the agent to read `SKILL.md` before proposal work:

```sh
git clone https://github.com/aetox-skills/idea-to-architecture-agent.git
```

Prompt:

```txt
Use Idea To Architecture Agent to turn this raw idea into a reviewable
architecture proposal.
```
