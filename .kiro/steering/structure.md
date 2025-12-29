# Project Structure

## Root Level Files
- **README.md**: Central inbox for all new items following "The Inbox Method"
- **PROCESS.md**: Defines the task management workflow and rules
- **tasks.md**: Main task tracking with To Do → In Progress → Done lifecycle
- **schedule.md**: Weekly scheduling template
- **metrics.md**: Performance tracking and completion rates
- **CNAME**: GitHub Pages hosting configuration

## Directory Organization

### `/docs/`
Research documentation and reference materials:
- **README.md**: Documentation index
- **ai-cli-research.md**: AI command-line tool research
- **business-research.md**: Business opportunities and resources
- **hwpc-notes.md**: Hardware/PC business notes
- **media-*.md**: Media consumption tracking
- **netbox-research.md**, **netstack-notes.md**: Network infrastructure research
- **random-links.md**: General link archive

### `/wip-detail/`
Detailed work-in-progress notes for specific projects:
- **README.md**: WIP index
- **LLC-EOY.md**: End-of-year business processes
- **Repair-2010Buick-ai.md**: Vehicle repair project details
- **[person]notes.md**: Individual contributor notes (catnotes, colenotes, etc.)
- **trinknotes[date].md**: Time-based project notes

### `/logs/`
Historical records and archived information (currently empty)

### `/_resources/`
Static assets and images for documentation

## File Naming Conventions
- Use kebab-case for multi-word filenames
- Include dates in format YYYYMM for time-based notes
- Use descriptive names that indicate content type (research, notes, etc.)
- Person-specific files use format: `[name]notes.md`

## Workflow Integration
- All new items start in **README.md** (inbox)
- Items are tagged with `@type:`, `@person:`, `@project:`, `@priority:` 
- Tasks move to **tasks.md** with Definition of Done
- Research moves to appropriate **docs/** file
- Complex projects get detailed files in **wip-detail/**