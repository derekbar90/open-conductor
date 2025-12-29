# Conductor Implementation Guide

This guide defines the execution loop for implementing tasks within a track.

## 1. Track Selection
1. Parse `conductor/tracks.md`.
2. Identify the first track not marked as `[x]`.
3. Update its status to `[~]`.

## 2. Implementation Loop
For each task in the track's `plan.md`:
1. **Mark In-Progress:** Change `[ ]` to `[~]`.
2. **Follow Workflow:** Execute the steps in `conductor/workflow.md` (TDD, commits, git notes).
3. **Record SHA:** Append the short commit SHA and mark as `[x]`.

## 3. Phase Completion
When a phase concludes (indicated by the Verification meta-task):
1. Execute the "Phase Completion Verification and Checkpointing Protocol" from `workflow.md`.
2. Propose manual verification steps to the user.
3. Create a checkpoint commit.

## 4. Documentation Synchronization
Once the track is `[x]`:
1. Analyze `spec.md` for permanent changes to the product or tech stack.
2. Propose updates to `conductor/product.md` and `conductor/tech-stack.md`.
3. **Strict Control:** Only update `product-guidelines.md` if the spec explicitly mandates a strategic shift.

## 5. Track Cleanup
Prompt the user to:
- **Archive:** Move folder to `conductor/archive/` and remove from `tracks.md`.
- **Delete:** Permanently remove the folder and registry entry.
- **Skip:** Keep as is.
