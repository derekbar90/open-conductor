# Conductor Protocol Details

This reference document defines the specific actions you must take during each phase of the Conductor protocol.

## 1. Context Analysis
Before any development, you MUST understand the project's foundation.
- Read `conductor/product.md` to understand the vision and target users.
- Read `conductor/tech-stack.md` to identify approved languages and frameworks.
- Read `conductor/workflow.md` to understand testing and commit requirements.
- Analyze the existing directory structure to infer architectural patterns.

## 2. Specification (Spec)
A spec defines *what* is being built and *why*. It must include:
- **Goal:** A concise statement of the desired outcome.
- **Requirements:** A bulleted list of functional and non-functional requirements.
- **Components:** A list of the files or modules that will be affected.
- **Verification:** How the user will know the task is successful.

## 3. Planning (Plan)
A plan defines *how* the spec will be implemented. It must be broken down into:
- **Phases:** Logical groups of related tasks.
- **Tasks:** Atomic, actionable items.
- **Checkpoint Tasks:** Every phase MUST end with a "User Manual Verification" task as defined in the project workflow.

## 4. Implementation
Execute the plan following the project workflow:
- **Sequential Execution:** Complete tasks one by one in the order defined in `plan.md`.
- **TDD Pattern:** Write tests -> Run tests (fail) -> Implement code -> Run tests (pass) -> Refactor.
- **Git Discipline:** Commit each task with a descriptive message and attach a summary via `git notes`.
- **Status Updates:** Update `plan.md` status (`[ ]` -> `[~]` -> `[x]`) after each step.
