# Conductor Maintenance Guide

This guide defines the procedures for project status reporting and git-aware reverts.

## 1. Status Reporting
1. Read `conductor/tracks.md`.
2. List all tracks in `conductor/tracks/` and read their `plan.md`.
3. Generate a summary including:
   - Total Phases and Tasks.
   - Completed/In-Progress/Pending counts.
   - Overall progress percentage.
   - Current active task and next pending action.

## 2. Git-Aware Reverts
This logic allows for reverting logical units of work (Tracks, Phases, or Tasks).

### Identification
1. Find the target in `plan.md` or `tracks.md`.
2. Extract the associated commit SHAs (Implementation commits and Plan-update commits).
3. If a Track is selected, find the "Track Creation" commit in `conductor/tracks.md` history.

### Execution
1. Propose the list of commits to be reverted to the user.
2. Run `git revert --no-edit <sha>` in reverse chronological order.
3. Handle merge conflicts by pausing and providing manual instructions.
4. Verify and correct the `plan.md` state after the reverts are complete.
