# AGENTS.md

## Repo Purpose

This is a **Codex skills repository** — a collection of agent skills (SKILL.md files) that can be installed and used by Codex sessions. Not an application codebase.

## Structure

```
skills/
├── <skill-name>/SKILL.md       # Source skill definitions (author-editable)
├── .agents/skills/<name>/SKILL.md  # Installed/deployed skill copies
├── skills-lock.json            # Lock file tracking installed skills with hashes
└── README.md                   # Minimal description
```

- `skills-lock.json` tracks installed skills with their GitHub source and `computedHash`. Update this when adding or removing skills.
- `.agents/skills/` mirrors installed skills — keep in sync with `skills-lock.json`.

## Skill File Format

Every `SKILL.md` must have a YAML frontmatter block:

```yaml
---
name: skill-name
description: One-line description used for skill discovery and auto-invocation matching
metadata:
  author: user-custom
  version: "1.0.0"
  category: category-name
allowed-tools: Read Fetch Bash   # space-separated list of permitted tools
---
```

- `description` is critical — Codex uses it to decide when to auto-invoke the skill.
- `allowed-tools` restricts which tools the skill can use; omit to allow all.

## Adding a New Skill

1. Create `<skill-name>/SKILL.md` with valid frontmatter + instructions.
2. Copy to `.agents/skills/<skill-name>/SKILL.md`.
3. Add an entry to `skills-lock.json` under `"skills"` with `source`, `sourceType`, and `computedHash`.

## Installed Skills

| Skill | Source | Purpose |
|---|---|---|
| `frontend-monthly-work-summary` | `wumyuan/skills` (GitHub) | Summarizes frontend monthly work logs from a URL |

## `my-skill/`

This is a template/placeholder skill with stub content. Not a real skill — use as a starting point when authoring new skills.

## No Build/Test/Lint

This repo has no build system, test runner, CI, or linter. There are no commands to run. Verification is manual: read the SKILL.md files for correctness and ensure `skills-lock.json` stays in sync.
