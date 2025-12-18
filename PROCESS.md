# Process and Rules

This document outlines the process for managing tasks in this repository.

## Task Management Workflow: The Inbox Method

Our workflow starts with `README.md` as the central "inbox" for all incoming information. The goal is to process this inbox regularly, so it remains current and serves as a historical log.

**1. Capture:**
All new ideas, notes, links, and tasks are first added to `README.md`. The format is flexible.

**2. Process and Tag:**
On a regular basis, we will review every item in `README.md`. Each item will be given one or more tags to provide structure. The standard format is `@key:value`. These tags are appended to the item's line directly within `README.md`.

*   **Core Tags:**
    *   `@type:task` - An actionable item that needs to be done.
    *   `@type:note` - Information to be logged, documented, or archived.
    *   `@type:link` - A URL that needs to be saved or reviewed.
*   **Optional Tags:**
    *   `@person:[name]` - Assigns the item to a specific person (e.g., `@person:mark`).
    *   `@project:[name]` - Associates the item with a project (e.g., `@project:hwpc`).
    *   `@priority:[level]` - Sets the urgency (e.g., `@priority:high`).

**3. Route and Link:**
Once an item is tagged, it is moved from `README.md` to its correct destination. After moving, the original item in `README.md` is updated with a link to its new location, creating a reference.

*   `@type:task` items are moved to the `To Do` section of `tasks.md`.
*   `@type:note` items are moved to a relevant document in `docs/` or a new file in `logs/`.
*   `@type:link` items can be archived in a relevant document.

This turns `README.md` into a persistent log of all captured items and where they were routed, rather than an inbox that gets emptied.

The `tasks.md` file then follows a simple `To Do` -> `In Progress` -> `Done` lifecycle for all committed tasks.

## Handling Complex Tasks (Epics)

A complex task that consists of multiple sub-tasks is called an "Epic".

*   An Epic is represented as a main task item.
*   Its sub-tasks are listed as a nested list underneath it.
*   An Epic is only considered "Done" when all of its sub-tasks are completed.

## Definition of Done (DoD)

To ensure clarity and avoid ambiguity, every task or Epic moved into the "To Do" stage **must** have a "Definition of Done" (DoD).

*   The DoD is a checklist of criteria that must be met for the task to be considered complete.
*   For an Epic, the DoD should include the completion of all sub-tasks and any other final requirements (e.g., documentation, deployment).

### Example of an Epic with a DoD:

```markdown
## To Do

- [ ] **Epic: Set up new development environment** (Priority: High)
    - **Definition of Done:**
        - [ ] All sub-tasks are completed.
        - [ ] The new environment is documented in `docs/environment_setup.md`.
    - **Sub-tasks:**
        - [ ] Research and choose a new code editor.
        - [ ] Install and configure the chosen editor with project plugins.
        - [ ] Write a script to automate dependency installation.
        - [ ] Run all project tests successfully in the new environment.
```
