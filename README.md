# pi-skills

A collection of skills for [pi](https://github.com/badlogic/pi-mono), compatible with Claude Code and Codex CLI.

## Installation

Clone or download skills to your pi skills directory:

```bash
# User-level (available in all projects)
git clone https://github.com/badlogic/pi-skills ~/.pi/agent/skills/pi-skills

# Or project-level
git clone https://github.com/badlogic/pi-skills .pi/skills/pi-skills
```

## Available Skills

| Skill | Description |
|-------|-------------|
| [brave-search](brave-search/SKILL.md) | Web search and content extraction via Brave Search |
| [browser-tools](browser-tools/SKILL.md) | Interactive browser automation via Chrome DevTools Protocol |
| [vscode](vscode/SKILL.md) | VS Code integration for diffs and file comparison |

## Skill Format

Each skill follows the pi/Claude Code format:

```markdown
---
name: skill-name
description: Short description shown to agent
---

# Instructions

Detailed instructions here...
Helper files available at: {baseDir}/
```

The `{baseDir}` placeholder is replaced with the skill's directory path at runtime.

## Requirements

Some skills require additional setup:

- **brave-search**: Requires Node.js. Run `npm install` in the skill directory.
- **browser-tools**: Requires Chrome and Node.js. Run `npm install` in the skill directory.
- **vscode**: Requires VS Code with `code` CLI in PATH.

## License

MIT
