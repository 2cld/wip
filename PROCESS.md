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

## Task Formatting Guidelines

### Current Tasks Details Section

The `## Current Tasks details` section in `README.md` is your active workspace - it shows only tasks you're working on THIS WEEK.

**Keep 6-10 tasks maximum:**
- Tasks in your Top 3 Priorities
- Tasks touched in the past 5 days
- Tasks scheduled for this week (per `schedule.md`)

**All other tasks live in `tasks.md`:**
- Tasks not touched in 5+ days → move to `tasks.md`
- Future tasks not scheduled this week → keep in `tasks.md`
- Completed tasks → move to Done section in `tasks.md`

**Why this works:**
- README becomes your focused "active workspace"
- Collapsible format keeps 6-10 tasks scannable as one-liners
- Natural rotation: tasks age out after 5 days of inactivity
- Less scrolling, less clutter, better focus

### Collapsible Tasks with Subtasks

For tasks with multiple subtasks or long checklists in `README.md`, use HTML `<details>` tags for better readability. This keeps the Today section scannable while preserving all task details.

**Format:**
```html
<details>
<summary><strong>Task: Task Name Here</strong> <span>@type:task @priority:high @project:project-name</span></summary>

**Definition of Done:**
- [ ] Subtask 1
- [ ] Subtask 2
- [ ] Subtask 3

</details>
```

**Example:**
```html
<details>
<summary><strong>Task: Setup LLC payments</strong> <span>@type:task @priority:medium @project:cat9-acct-LLC</span></summary>

**Definition of Done:**
- [ ] FHKlopFarms Utilities
- [ ] FHKlopFarms IA Land Tax
- [ ] TreesAES Utilities
- [ ] TreesAES IA Land Tax

</details>
```

**Key formatting rules:**
- Use `<strong>` tags instead of `**` inside HTML elements
- Put `<span>` with tags inside the `<summary>` element
- Use standard markdown lists (not `<ol>` or `<li>`) inside `<details>`
- Add blank line after opening `<summary>` and before closing `</details>`
- No `<hr/>` separators between tasks - they add visual clutter

**When to use:**
- Epics with 3+ subtasks
- Tasks with detailed checklists (5+ items)
- Any task where the details would clutter the Today section

**When NOT to use:**
- Simple tasks with no subtasks
- Tasks in `tasks.md` (use standard markdown there)

## Daily Morning Routine

This is your daily habit-building process. Do this every morning before diving into work.

**Time Required:** 17-25 minutes

### Step 0: Sync Check (1 min)
1. Pull latest changes: `git pull origin main`
2. This ensures you're working with the latest version from https://wip.2cld.net
3. If you made edits on GitHub or another machine, they'll be merged automatically
4. Resolve any merge conflicts if they occur (rare, but possible)

### Step 1: Yesterday Review (5 min)
1. Look at your `# Yesterday` section in `README.md`
2. Move completed items to `Done` in `tasks.md`
3. Move incomplete items back to `# Today` or `# Inbox` for re-evaluation
4. Ask yourself: "What blocked me yesterday?"

### Step 2: Inbox Triage (5 min)
1. Review `# Inbox` section in `README.md`
2. Tag each item with `@type:`, `@priority:`, `@project:` as needed
3. Move urgent items to `# Today`
4. Move non-urgent tasks to `tasks.md` with a Definition of Done
5. Archive notes/links to appropriate `docs/` files

### Step 2.5: README Declutter (3 min)
1. Move completed items from `# Today` to `# Yesterday`
2. Delete old `# Yesterday` section (git history preserves it if needed)
3. Remove past-due items from `# Due Soon` (e.g., dates that have passed)
4. Quick scan of `# Open Projects` - any stale notes to move to docs/?
5. Review `## Current Tasks details` - keep only 6-10 active tasks:
   - Keep tasks in Top 3 Priorities
   - Keep tasks touched in past 5 days
   - Keep tasks scheduled for this week
   - Move inactive tasks back to `tasks.md`
6. Goal: Keep README focused on current week's work only

### Step 3: Priority Rating (3 min)
1. Review `# Today` section
2. Check `# Due Soon` - any items due within 5 days?
3. Pull urgent deadline items into `# Today` with `@priority:high`
4. Identify your top 3 priorities for today
5. Be honest: Can you realistically complete these today?
6. If not, move lower priority items back to `tasks.md`

### Step 4: Time Blocking (5 min)
1. Open your calendar (Google Calendar or Apple Calendar)
2. Block time for each priority task
3. Include buffer time between blocks
4. Schedule breaks and lunch
5. Note any meetings or commitments

### Step 5: Daily Check-In (2 min)
1. Update the `# Daily Check-In` section in `README.md`
2. Record today's date and your commitment
3. This creates accountability and a visible streak

### Step 6: Commit and Push (1 min)
1. Commit your changes: `git add . && git commit -m "Daily review YYYY-MM-DD @daily-review-YYYY-MM-DD"`
2. Push to GitHub: `git push origin main`
3. This syncs your work to https://wip.2cld.net
4. Tag format helps track daily review commits

**Pro Tips:**
- Do this routine at the same time every morning
- Keep it to 20 minutes max - don't overthink
- If you skip a day, don't beat yourself up - just restart tomorrow
- Review your weekly progress every Sunday evening

## Sunday Evening Review

This is your weekly planning session to set yourself up for success.

**Time Required:** 40-55 minutes

### Step 1: Week Retrospective (10 min)
1. Review what you accomplished this week
2. Update `metrics.md` with completion rates
3. Celebrate wins - what went well?
4. Identify blockers - what got in the way?

### Step 2: Due Soon Planning (15 min)
1. Review `# Due Soon` section in `README.md`
2. For each item, calculate days until deadline
3. Break down large deadline items into daily chunks
4. Schedule specific days in the upcoming week to work on each item
5. Add these scheduled chunks to your calendar with time blocks
6. Update calendar reminders if needed (7 days, 3 days, 1 day before)

### Step 3: Week Ahead Setup (10 min)
1. Review `schedule.md` and plan your week structure
2. Look at calendar commitments and meetings
3. Identify your 3 biggest goals for the week
4. Pre-populate Monday's `# Today` section with your top priorities

### Step 4: Weekly Cleanup (10 min)
1. **Archive old inbox entries:** Move `# Inbox` "Processed" entries older than 7 days to `logs/inbox-archive-YYYY-MM.md`
2. **Review Backlog:** Scan `# Backlog` section - delete dead items, move active ones to tasks.md
3. **Clean Due Soon:** Remove completed or past-due items from `# Due Soon`
4. **Declutter Open Projects:** Archive stale notes/links to appropriate docs/ files
5. **Clear Daily Check-In history:** Keep only the current week (Mon-Sun) in the Daily Check-In section - older entries are preserved in git history
6. Goal: Start the week with a clean, focused README.md

### Step 5: Reset and Commit (5 min)
1. Archive completed items from `# Yesterday`
2. Clean up your workspace (digital and physical)
3. Set your intention for the week ahead
4. Go into Monday ready to execute

**Pro Tips:**
- Do this at the same time every Sunday evening
- Don't schedule every minute - leave buffer time
- Be realistic about your capacity
- If you have a big deadline, protect focus time in your calendar
