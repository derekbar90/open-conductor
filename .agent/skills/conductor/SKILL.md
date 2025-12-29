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
1. **Load Protocol Details:** Read [references/protocol.md](references/protocol.md) for a deep dive into each phase.
2. **Initialize State:** Check if a `conductor/` directory exists. If not, inform the user they must run the initialization process (e.g., `/conductor:setup`).
3. **Orchestrate Work:** For new features or bugs, create a new Track folder in `conductor/tracks/` and initialize its `spec.md` and `plan.md`.
4. **Maintain Plan:** Keep the `plan.md` updated as you progress, marking tasks as in-progress `[~]` or completed `[x]`.

## Getting Started
When a user asks to "add a feature" or "fix a bug", you should activate this skill to guide them through the planning process.

For detailed instructions on execution, see [references/protocol.md](references/protocol.md).
