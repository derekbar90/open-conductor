# Tech Stack: Conductor (Universal Agent Skill)

## 1. Core Platform
*   **OpenSkills / Anthropic Agent Skills:** The standard for implementing portable AI agent behaviors.
*   **Claude Code:** Native support via `.claude/skills/`.
*   **OpenSkills CLI:** Enables discovery and invocation in non-native agents via `openskills read conductor`.

## 2. Implementation
*   **Skill Definition (`SKILL.md`):** Strict YAML + Markdown following the Anthropic specification.
*   **Universal AGENTS.md:** Uses OpenSkills XML format (`<available_skills>`) for cross-agent discovery.
*   **Directory Structure:**
    - `.claude/skills/conductor/` (or `.agent/skills/conductor/` in universal mode).
    - `conductor/`: The project-specific data store.

## 3. Tooling
*   **openskills CLI:** For installing, syncing, and reading the Conductor skill.
*   **Git:** For versioning both code and Conductor's context artifacts.
