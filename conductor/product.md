# Initial Concept
Conductor is a Universal Agent Skill (compatible with Claude Code and OpenSkills) that enables Context-Driven Development. It teaches AI agents to act as proactive project managers following a strict protocol (Context -> Spec & Plan -> Implement).

# Product Guide: Conductor (Universal Agent Skill)

## Vision
To transform AI coding agents into rigorous engineering partners. Conductor ensures that instead of reactive coding, agents follow a structured lifecycle where every feature or bug fix is properly specified and planned before implementation begins.

## Target Users
- **Developers using Claude Code, Cursor, Windsurf, or Aider:** Who want a consistent, disciplined workflow across any agent.
- **Engineering Teams:** Who want to maintain a shared, version-controlled source of truth for project context.

## Core Goals
- **Multi-Agent Compatibility:** Works natively in Claude Code and via OpenSkills in Cursor, Windsurf, and Aider.
- **Progressive Disclosure:** Keeps the agent's context clean by loading detailed instructions only when "Conductor" is invoked.
- **AGENTS.md Integration:** Automatically synchronizes with OpenSkills' `<available_skills>` format for universal discovery.

## Key Features
- **Universal Discovery:** Triggered by phrases like "add a feature" or "start a plan" across all supported agents.
- **Managed Implementation:** Agents follow `plan.md` tasks sequentially, maintaining state in the `conductor/` directory.
- **Logical Reverts:** Git-aware undo operations based on the task/phase structure.
