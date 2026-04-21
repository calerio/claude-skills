# Claude Skills

A collection of custom skills for Claude Code and other AI coding assistants. Each skill is a structured markdown prompt that teaches the assistant how to perform a specific task.

## Skills

| Skill | Description | Status |
|-------|-------------|--------|
| [critical-evaluation](critical-evaluation/) | Structured, topic-agnostic framework for critically analysing articles, essays, opinion pieces, news reports, and academic papers. Combines multiple analytical lenses (claim taxonomy, speech act analysis, rhetorical devices, falsifiability, intent classification, and more) into one coherent evaluation. | Ready |

## Usage

These skills are designed for use with [Claude Code](https://docs.anthropic.com/en/docs/claude-code) and compatible AI assistants. To use a skill:

1. Copy the skill's `.md` file into your assistant's skills directory (e.g., `~/.claude/skills/` for Claude Code or `.cursor/skills/` for Cursor)
2. The assistant will automatically apply the skill when the trigger conditions described in the skill's `description` field are met

Each skill follows a standard format with YAML frontmatter containing:
- `name` — unique identifier
- `description` — trigger conditions and capabilities

## License

This project is licensed under the Apache License 2.0 — see the [LICENSE](LICENSE) file for details.
