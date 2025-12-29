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

## Core Protocol
1. **Context:** Analyze existing project context (`conductor/product.md`, `conductor/tech-stack.md`, etc.).
2. **Spec:** Draft a detailed specification for the task.
3. **Plan:** Create an actionable step-by-step implementation plan.
4. **Implement:** Execute the plan following the project's workflow (e.g., TDD).

## Getting Started
When a user asks to "add a feature" or "fix a bug", you should activate this skill to guide them through the planning process.

For detailed instructions on execution, see [references/protocol.md](references/protocol.md).
