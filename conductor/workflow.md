# Project Workflow (Conductor Universal Skill)

## Guiding Principles
1. **The Plan is the Source of Truth:** All work tracked in `plan.md`.
2. **Universal Context:** The `conductor/` directory and the Conductor Skill provide the engineering foundation for *any* agent working on the project.
3. **OpenSkills Sync:** Run `openskills sync` whenever the Conductor Skill or available skills are modified to ensure all agents are updated.

## Task Workflow (Agent Agnostic)
1. **Invocation:** The user says "Let's start a new feature" or "I have a bug".
2. **Skill Activation:** 
   - **Claude Code:** Automatically invokes the Conductor Skill.
   - **Other Agents:** Invoke via `Bash("openskills read conductor")` as prompted by `AGENTS.md`.
3. **Spec -> Plan -> Implement:** The agent follows the defined Conductor protocol.
4. **Checkpointing:** Follow the existing "Phase Completion" protocol, ensuring commits and git notes are maintained.