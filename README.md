# LLM Skills

A collection of reusable skills for different LLM coding assistants, starting with claude specifically once i have used in my day to day workflow

## What are Skills?

Skills are instruction files that give LLMs specialized capabilities. Instead of repeating prompts, you drop a skill file into your project and the LLM follows those instructions automatically.

## Installation

### Claude Code

1. Copy the skill directory to your project:
   ```bash
   cp -r claude/<skill-name>/ /path/to/your-project/.claude/skills/
   ```

2. Reload Claude Code (restart the session or run `/refresh`)

3. The skill is now available. Claude will automatically use it when relevant, or you can invoke it directly.

**Example:**
```bash
# Add code-reviewer skill to your project
cp -r claude/code-reviewer/ ~/my-app/.claude/skills/
```

## Available Skills

### Claude

| Skill | Description |
|-------|-------------|
| [code-reviewer](claude/code-reviewer/) | Code review agent for comprehensive analysis of code quality, security, performance, and architecture. Supports modes: quick scan, deep dive, security focus, performance focus, architecture review. |

## Skill Structure

Each skill directory contains a `SKILL.md` file with:

```yaml
---
name: skill-name
description: "What the skill does"
---

# Skill instructions follow...
```

## Contributing

Add new skills by creating a directory under the appropriate LLM folder with a `SKILL.md` file.
