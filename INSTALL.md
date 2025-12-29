# Installation Guide: Conductor Universal Skill

Conductor is designed to be portable across all major AI coding agents (Claude Code, Cursor, Windsurf, Aider) using the **OpenSkills** standard.

## Prerequisites
- **Node.js 20.6+** (required for the OpenSkills CLI)
- **Git**

---

## Method 1: Universal Installation (Recommended)
Use this method for Cursor, Windsurf, Aider, or if you use multiple agents in the same project.

### 1. Install OpenSkills CLI
```bash
npm i -g openskills
```

### 2. Install the Conductor Skill
You can install Conductor from a local clone or directly from GitHub:

**From Local Path:**
```bash
openskills install /path/to/open-conductor --universal
```

**From GitHub:**
```bash
openskills install gemini-cli-extensions/conductor --universal
```

### 3. Sync Discovery
Ensure your project's `AGENTS.md` is updated so all agents can "see" Conductor:
```bash
openskills sync
```

---

## Method 2: Claude Code Native
If you only use Claude Code, you can install the skill manually.

1. **Create the skills directory:**
   ```bash
   mkdir -p .claude/skills/
   ```
2. **Symlink or Copy the skill:**
   ```bash
   ln -s /path/to/open-conductor/.agent/skills/conductor .claude/skills/conductor
   ```
3. **Restart Claude Code.**

---

## First Run: Initializing a Project

Once installed, Conductor is "discovered" automatically by your agent when you mention planning or features. To force an initialization:

1. **Start a conversation** with your agent.
2. **Invoke Conductor:**
   - Say: *"I want to set up Conductor for this project."*
   - Or manually read it: `openskills read conductor`
3. **Follow the Prompts:** Conductor will detect that the project is not yet initialized and will guide you through creating the `conductor/` directory and project context.
