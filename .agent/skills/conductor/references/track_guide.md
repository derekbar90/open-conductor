# Conductor Track Creation Guide

This guide defines the process for initializing a new Track (Feature, Bug, or Chore).

## 1. Initialization
1. **Identify Description:** Get the track description from the user.
2. **Infer Type:** Classify as "Feature", "Bug", "Chore", or "Refactor".
3. **Verify Uniqueness:** Check `conductor/tracks/` to ensure a track with a similar name doesn't already exist.

## 2. Interactive Specification (`spec.md`)
Ask 3-5 sequential questions to define the scope. Present 3 suggested options + "Type your own".
- **Feature:** Focus on UI, logic, inputs/outputs, and user flow.
- **Bug:** Focus on reproduction steps, expected vs. actual behavior.
- **Other:** Focus on specific goals and success criteria.

**Drafting:** Generate a `spec.md` with Overview, Requirements, and Acceptance Criteria. Wait for user confirmation.

## 3. Plan Generation (`plan.md`)
Based on the `spec.md` and `conductor/workflow.md`:
1. Generate a hierarchical list of Phases and Tasks.
2. **Mandatory:** Inject a "Conductor - User Manual Verification" task at the end of every Phase.
3. **TDD Pattern:** If the workflow requires TDD, every feature task must have a "Write Tests" sub-task.

## 4. Artifact Creation
1. **Generate ID:** `shortname_YYYYMMDD`.
2. **Create Directory:** `conductor/tracks/<track_id>/`.
3. **Write Files:** Create `metadata.json`, `spec.md`, and `plan.md`.
4. **Update Registry:** Append the new track entry to `conductor/tracks.md`.
