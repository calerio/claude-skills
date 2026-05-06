# Claude Skills

A collection of custom skills for Claude Code and Claude.ai. Each skill is a structured markdown prompt that teaches the assistant how to perform a specific task.

## Skills

| Skill | Description | Status |
|-------|-------------|--------|
| [critical-evaluation](critical-evaluation/) | Structured, topic-agnostic framework for critically analysing articles, essays, opinion pieces, news reports, and academic papers. Combines multiple analytical lenses (claim taxonomy, speech act analysis, rhetorical devices, falsifiability, intent classification, and more) into one coherent evaluation. | Ready |
| [lecture-explainer](lecture-explainer/) | Turns pasted lecture slides, textbook excerpts, or problem sets into proper study notes — every definition, theorem, and proof unpacked with intuition and worked examples. | Ready |

## Installing a skill

### In Claude.ai (web or desktop app)

1. **Enable the prerequisite.** Open Claude.ai and go to **Settings → Capabilities**. Turn on **Code execution and file creation** — skills won't run without this.
2. **Download the skill folder.** Either clone this repo (`git clone https://github.com/calerio/claude-skills.git`) or grab a single folder via [download-directory.github.io](https://download-directory.github.io/).
3. **Confirm the skill file is named `SKILL.md`.** Claude.ai expects exactly that filename at the folder's root, with YAML frontmatter (`name`, `description`) at the top. If the folder ships a different filename (e.g. `<name>.md` or `<name>.skill`), rename or copy it to `SKILL.md` before zipping.
4. **Zip the folder — folder at ZIP root, not nested.** From the parent directory:
   ```bash
   zip -r my-skill.zip my-skill/
   ```
   Important: the ZIP must contain the skill folder as its root, not wrapped inside a subfolder.
5. **Upload it.** In Claude.ai, click your name (bottom-left) → **Customize Claude → Skills → + Create skill → Upload**. Drop in the ZIP.
6. **Toggle the skill on** in the Skills list. Custom skills are private to your account.

Test by sending a message that should match the skill's trigger conditions, and check the model's thinking trace to confirm the skill loaded.

### In Claude Code (CLI)

Copy the skill folder into your Claude Code skills directory:

```bash
cp -r critical-evaluation/ ~/.claude/skills/
```

Claude Code auto-discovers skills under `~/.claude/skills/<name>/` (looking for either `SKILL.md` or `<name>.md` inside) and applies them when the description's trigger conditions match. No restart required.

For project-scoped skills, drop them under `.claude/skills/` inside your repo instead of `~/.claude/skills/`.

## Authoring a skill

Each skill is a folder containing a single `SKILL.md` with YAML frontmatter:

```yaml
---
name: my-skill
description: >
  When to trigger the skill. Be specific about phrases and contexts —
  Claude uses this to decide whether to invoke the skill.
---

# Skill body
…instructions for Claude…
```

Constraints (per Anthropic's spec):
- `name` — lowercase, letters / numbers / hyphens only, max 64 chars
- `description` — max 200 chars; this is the trigger contract, so make it specific

See Anthropic's [official skill docs](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills) and the [Use Skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude) help center article for the full spec.

## License

This project is licensed under the Apache License 2.0 — see the [LICENSE](LICENSE) file for details.
