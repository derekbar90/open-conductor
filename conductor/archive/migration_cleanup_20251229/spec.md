# Specification: Universal Skill Migration & Cleanup

## Goal
To make the Conductor Agent Skill fully self-contained and portable by migrating all interactive logic from legacy `.toml` files into Markdown guides and removing dead files.

## Requirements
- **Logic Portability:** All interactive questions and state checks from `setup.toml`, `newTrack.toml`, etc., must be transcribed into the Skill's `references/`.
- **Zero Redundancy:** The `commands/` directory and `gemini-extension.json` must be removed once the Skill is fully functional.
- **Improved Discovery:** The `SKILL.md` must be updated to route users to the correct guides for Setup, New Tracks, and Implementation.
- **Asset Referencing:** The Skill must reference templates now located in `assets/templates/`.

## Components
1. **`.agent/skills/conductor/references/`**: Will now contain `setup_guide.md`, `track_guide.md`, `implementation_guide.md`, and `maintenance_guide.md`.
2. **`.agent/skills/conductor/SKILL.md`**: Updated orchestration logic.
3. **`AGENTS.md`**: Updated to reflect the complete skill.
