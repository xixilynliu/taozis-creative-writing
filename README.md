# Taozi's Creative Writing Skills

> A collection of creative writing skills for Claude Code / Ducc, curated by Taozi.

## What is this?

This is a skill library for AI-assisted creative writing. Each skill is a self-contained package that can be installed into Claude Code (or Ducc) to unlock specialized writing capabilities.

## Available Skills

| Skill | Description | Status |
|-------|-------------|--------|
| `novel-writing` | Long-form novel writing with plot structure, character development, and chapter planning | WIP |
| `podcast-script` | Podcast script writing with dialogue, pacing, and audio cues | WIP |
| `screenplay` | Screenplay / film script writing in standard format | WIP |
| `short-drama` | Short drama (micro-drama) script writing for social media | WIP |
| `lyrics` | Song lyrics writing with rhythm, rhyme, and emotional arc | WIP |

## Installation

Copy any skill directory into your Claude Code skills folder:

```bash
# For Ducc / Claude Code
cp -r skills/<skill-name> ~/.claude/skills/
```

Or install from the remote registry (if published):

```
/skill-recommender
```

## Skill Structure

Each skill follows the standard Claude Code skill format:

```
skills/<skill-name>/
  SKILL.md          # Manifest (YAML frontmatter) + full prompt
  scripts/          # (Optional) supporting scripts
  examples/         # (Optional) example outputs
```

### SKILL.md Format

```markdown
---
name: <skill-name>
description: <when and how to use this skill>
---

# Skill Title

<Full writing instructions, workflow, and constraints>
```

## Contributing

1. Create a new directory under `skills/`
2. Write your `SKILL.md` following the template in `templates/SKILL-TEMPLATE.md`
3. Add examples if helpful
4. Submit a PR

## License

MIT
