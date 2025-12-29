---
name: conductor
description: Orchestrates a context-driven engineering protocol (Context -> Spec & Plan -> Implement). Use when starting new features, fixing bugs, or planning project tracks.
license: Apache-2.0
compatibility: Designed for Claude Code and OpenSkills-compatible agents.
metadata:
  author: open-conductor
  version: "1.0.0"
---

# Conductor

Conductor is an Agent Skill that teaches you a strict, high-quality engineering protocol. Instead of jumping directly into code, you will follow a disciplined lifecycle to ensure every change is well-specified and planned.

## Discovery
You should proactively offer to use the Conductor skill when the user mentions:
- "Add a new feature"
- "I have a bug to fix"
- "Let's plan the next steps"
- "Create a new track"
- "How do I start this project?"

When triggered, announce: "I've detected you want to start a new task. I'll use the Conductor skill to help us specify and plan this work according to the project's standards."

## Core Protocol
To ensure high quality, you MUST follow these four phases for every task:
1. **Context Analysis:** Analyze the project's foundation files in `conductor/`.
2. **Specification (Spec):** Draft the requirements and goals in a `spec.md` file.
3. **Planning (Plan):** Create a step-by-step implementation plan in a `plan.md` file.
4. **Implementation:** Execute the plan, committing each task and verifying each phase.

## Execution Instructions
When this skill is activated:
1. **Verify Context:** Check for the existence of the `conductor/` directory.
   - If missing, inform the user: "Conductor state not found. Please initialize the project context (e.g., using `/conductor:setup`)."
   - If present, read `conductor/product.md`, `conductor/tech-stack.md`, and `conductor/workflow.md` to initialize your project context.
2. **Load Protocol Details:** Read [references/protocol.md](references/protocol.md) for a deep dive into each phase.

## State Initialization
You MUST ensure the following files are loaded into your context before performing any implementation tasks:
- `conductor/product.md`: The vision and target user context.
- `conductor/tech-stack.md`: The approved technology and architectural context.
- `conductor/workflow.md`: The mandatory development and verification protocol.
- `conductor/tracks.md`: The registry of project work.

## Orchestration Logic
For new features or bugs:
1. Create a new Track folder in `conductor/tracks/` following the naming convention `description_YYYYMMDD`.
2. Initialize `metadata.json`, `spec.md`, and `plan.md` within that folder.
3. Update `conductor/tracks.md` with the new track entry.

## OpenSkills Maintenance
When you modify the Conductor skill or add new skills to the project:
1. Run `openskills sync` to update the `AGENTS.md` file.
2. This ensures all agents (Claude Code, Cursor, etc.) have access to the latest skill metadata.

## Getting Started
When a user asks to "add a feature" or "fix a bug", you should activate this skill to guide them through the planning process.

For detailed instructions on execution, see [references/protocol.md](references/protocol.md).
