# Wip Integration Project

**Epic:** [README.md Current Epics](../README.md) - Wip repo + issue integration
**Status:** Starting - April 2026

## Goal
Connect Wip (the AI assistant) to project repos, calendar, and communication channels so it can:
 - Surface open issues and blockers during daily check-ins
 - Pull repo activity summaries during weekly reviews
 - Coordinate across multiple project identities
 - Eventually auto-log check-ins from calendar/repo activity

## Wip Identity Setup
Wip gets its own accounts to maintain audit trail (who did what):

 - [ ] GitHub account for Wip (wip-bot or similar)
 - [ ] Gitea account for Wip on cat9.me
 - [ ] Google account for Wip (calendar, email)
 - [ ] Document account credentials securely

### Identity Pattern
Each "project persona" has its own email/account for tracking:
 - **wip@** - the AI assistant identity
 - **cat@** - personal/cat9 work
 - **ghadmin@** - hwpc/grasshorse work
 - etc.

This lets you see in commit history and email threads exactly which context was active.

## Integration Phases

### Phase 1: GitHub (2cld/wip)
 - [ ] Create Wip GitHub account
 - [ ] Generate personal access token
 - [ ] Configure GitHub MCP server in `.kiro/settings/mcp.json`
 - [ ] Test: pull recent commits during daily check-in
 - [ ] Test: list open issues
 - [ ] Document setup in this file

### Phase 2: Gitea (cat9.me)
 - [ ] Create Wip Gitea account on gitea.cat9.me
 - [ ] Generate API token
 - [ ] Configure Gitea MCP server or API access
 - [ ] Test: pull ns-account, nsclai, nspwa activity
 - [ ] Test: surface open issues per Epic
 - [ ] Document setup in this file

### Phase 3: Google Calendar
 - [ ] Create Wip Google account
 - [ ] Configure Google Calendar API access
 - [ ] Test: pull today's events during morning check-in
 - [ ] Test: auto-detect missed check-ins from calendar activity
 - [ ] Document setup in this file

### Phase 4: Multi-Identity Coordination
 - [ ] Map project personas to accounts (cat@, ghadmin@, wip@, etc.)
 - [ ] Wip can check email/notifications across personas
 - [ ] Wip can coordinate "other me's" across projects
 - [ ] Document identity patterns in PROCESS.md

## MCP Configuration Pattern
```json
{
  "mcpServers": {
    "github": {
      "command": "uvx",
      "args": ["mcp-server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "<wip-bot-token>"
      }
    }
  }
}
```

## Links
 - [2cld/wip GitHub](https://github.com/2cld/wip)
 - [gitea.cat9.me](https://gitea.cat9.me)
 - [Kiro MCP docs](https://kiro.dev/docs/mcp)

## Notes
 - Start with GitHub since wip repo is already there
 - Gitea needs MCP server or custom API wrapper
 - Google Calendar is hardest but most impactful for daily planning
 - Wip identity accounts let you audit AI vs human activity
