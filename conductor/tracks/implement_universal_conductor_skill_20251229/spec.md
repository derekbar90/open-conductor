# Specification: Universal Conductor Agent Skill

## Goal
To implement a portable Agent Skill named "Conductor" that teaches AI agents a context-driven engineering protocol. This skill must be compatible with Claude Code and other agents via OpenSkills.

## Requirements
- **Format:** Must strictly follow the Anthropic Agent Skills specification.
- **Discovery:** Must trigger on keywords like "feature", "bug", "plan", and "conductor".
- **Protocol:** Must implement the Spec -> Plan -> Implement loop.
- **State Store:** Must use the project's `conductor/` directory for metadata and state.
- **Progressive Disclosure:** Must keep the main `SKILL.md` under 500 lines by moving details to `references/`.
- **Universal Compatibility:** Must support both native `Skill()` tools and `openskills read` CLI commands.

## Components
1. **`.agent/skills/conductor/SKILL.md`**: The entry point.
2. **`.agent/skills/conductor/references/protocol.md`**: Detailed execution instructions.
3. **`AGENTS.md`**: Project-level discovery file for non-native agents.
