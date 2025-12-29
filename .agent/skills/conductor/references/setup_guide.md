# Conductor Setup Guide

This guide defines the interactive process for initializing the Conductor context in a project.

## 1. Resume Check
Before starting, check for `conductor/setup_state.json`. 
- If it exists, read the `last_successful_step` and announce: "Resuming setup from [STEP]."
- Proceed to the next logical section.

## 2. Project Discovery (Interactive)
1. **Analyze Maturity:** Classify the project as **Brownfield** (Existing) or **Greenfield** (New).
   - **Brownfield Indicators:** `.git`, dependency manifests (`package.json`, etc.), or source code folders (`src/`, `app/`).
2. **Handle Brownfield:**
   - Announce: "Existing project detected."
   - Request permission for a read-only scan.
   - Analyze `README.md` and manifests to infer the tech stack and project goal.
3. **Handle Greenfield:**
   - Announce: "New project detected."
   - Run `git init` if `.git` is missing.
   - Ask the user: "What do you want to build?"

## 3. Collaborative Documentation
For each document below, ask a maximum of 5 sequential questions. Present 3 suggested options + "Type your own" + "Autogenerate".

- **Product Guide (`product.md`):** Focus on target users, core vision, and key features.
- **Product Guidelines (`product-guidelines.md`):** Focus on tone, documentation standards, and brand identity.
- **Tech Stack (`tech-stack.md`):** Focus on languages, frameworks, and architectural patterns.

## 4. Asset Selection
1. **Code Style Guides:** List available guides from `assets/templates/code_styleguides/`. Recommend based on the inferred tech stack.
2. **Workflow:** Copy `assets/templates/workflow.md` to `conductor/workflow.md`. Offer customization for test coverage and commit frequency.

## 5. Finalization
- Create `conductor/tracks.md`.
- Commit all files with `conductor(setup): Add conductor setup files`.
- Update `setup_state.json` to `3.3_initial_track_generated`.
