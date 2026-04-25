# Wip Integration Project

**Epic:** [README.md Current Epics](../README.md) - Wip repo + issue integration
**Status:** Starting - April 2026
**Persona doc:** [docs/ops-account-management.md](./ops-account-management.md)
**Source of truth:** [cat2net Google Sheet](https://docs.google.com/spreadsheets/d/1LdyZlFieSd_1APTbG0QahfwZgqBaA9PigO9_5SPSkmk/edit?gid=1959043129#gid=1959043129)

## Goal
Connect Wip (the AI assistant) to project repos, calendar, and communication channels so it can:
 - Surface open issues and blockers during daily check-ins
 - Pull repo activity summaries during weekly reviews
 - Coordinate across multiple project identities
 - Eventually auto-log check-ins from calendar/repo activity

---

## Wip Identity Setup

### Wip Persona
 - **Primary email:** wip@horseoff.com ✅ (Google Workspace - created 2026-04-25)
 - **Future alias:** wip@2cld.net (via Cloudflare email routing, not Google - avoid paid upgrade)
 - **Chrome profile name:** ho-wip ✅ (horseoff wip user, sync on)
 - **GitHub:** [ho-wip](https://github.com/ho-wip) ✅ (Google sign-in, collaborator on 2cld/wip)
 - **Gitea:** TBD (create on gitea.cat9.me with wip@horseoff.com)
 - **Purpose:** AI assistant identity - "persona brain" for managing and coordinating across all projects

### Step-by-Step: Create Wip Google Account

**⚠️ BLOCKER: 2cld.net domain alias investigation (2026-04-25)**

2cld.net is NOT showing in Google Admin → Manage domains for horseoff.com, but email to admin@2cld.net DOES deliver to admin@horseoff.com. Suspicion: legacy free Google Apps account (pre-2012) had 2cld.net added as domain alias when it was allowed, now hidden from modern admin UI.

**What we know:**
 - MX records for 2cld.net point to Google
 - Email sent to admin@2cld.net arrives at admin@horseoff.com inbox
 - Reply goes out as admin@horseoff.com (not admin@2cld.net)
 - "Send mail as" option for admin@2cld.net NOT found in Gmail settings
 - 2cld.net NOT visible in admin.google.com → Manage domains
 - horseoff.com is likely a legacy free Google Apps account with restricted domain management
 - Cloudflare only has 2cld.com, NOT 2cld.net
 - **Squarespace manages 2cld.net email** - has "Manage Google Workspace" and "Manage MX Records" buttons
 - Squarespace set up the MX records and Google Workspace connection for 2cld.net
 - klopfenstein.org uses Cloudflare email routing (different pattern)

**Investigation steps:**
 - [X] Check Squarespace for email forwarding → **FOUND: Squarespace manages Google Workspace for 2cld.net**
 - [X] Check Cloudflare → only has 2cld.com, not 2cld.net
 - [ ] Click "Manage Google Workspace" button in Squarespace 2cld.net settings - may expose domain admin
 - [ ] Check `admin.google.com/ac/domains` (direct link, may show more than new UI)
 - [ ] Check `admin.google.com/ac/owl/domainlist` (older admin page)
 - [ ] Run `dig MX 2cld.net +short` to confirm MX records
 - [ ] Check Apps → Google Workspace → Gmail → Routing for recipient address maps

**Decision:**
 - Use **wip@horseoff.com** as the primary identity for all services (GitHub, Gitea, Google)
 - Optionally add **wip@2cld.net** later as receive-only alias via Cloudflare email routing (like klopfenstein.org pattern)
 - Do NOT upgrade Google Workspace to paid - not worth it for a bot account
 - Move 2cld.net DNS to Cloudflare when ready for the alias

---

**Once the domain alias issue is resolved, proceed with these steps:**

1. **Login to Google Admin**
   - Go to [admin.google.com](https://admin.google.com)
   - Login as cat@horseoff.com (Workspace admin)

2. **Create the user**
   - Directory → Users → Add new user
   - First name: `wip`
   - Last name: `2cld`
   - Primary email: `wip@horseoff.com`
   - Set a strong password, store in your password manager

3. **Add 2cld.net alias**
   - Click on the new wip@horseoff.com user
   - User information → Alternate email addresses (aliases)
   - Add: `wip@2cld.net`
   - (This works because 2cld.net is already a secondary domain on the horseoff.com Workspace)

4. **Verify email works**
   - Send a test email to wip@2cld.net
   - Confirm it arrives at wip@horseoff.com inbox

5. **Setup Chrome profile**
   - chrome://settings/manageProfile
   - Profile name: `2cld-wip`
   - Sign in with wip@horseoff.com
   - Following the sorting pattern:
     - FirstName: `2cld-wip`
     - LastName: `2cld`
     - DisplayName: `2cld-wip 2cld`
   - Verify Sync is on

6. **Update cat2net**
   - Add wip@horseoff.com row to EmailMaintenance sheet
   - Add wip@2cld.net alias note
   - Update ops-account-management.md persona table

### Step-by-Step: Create Wip GitHub Account

1. **Create account**
   - Go to [github.com/signup](https://github.com/signup)
   - Use email: wip@horseoff.com
   - Username suggestion: `wip-2cld` or `2cld-wip`

2. **Generate personal access token**
   - Settings → Developer settings → Personal access tokens → Fine-grained tokens
   - Token name: `kiro-mcp`
   - Repository access: select `2cld/wip` (and any other repos Wip should read)
   - Permissions: Contents (read), Issues (read/write), Pull requests (read)
   - Copy token, store securely

3. **Add as collaborator to 2cld/wip**
   - Login as your main GitHub account (cat@horseoff.com / admin@2cld.net)
   - Go to github.com/2cld/wip → Settings → Collaborators
   - Invite the new wip account
   - Accept invite from wip account

4. **Configure Kiro MCP**
   - Store token in `.local/.env` (gitignored):
     ```
     GITHUB_PERSONAL_ACCESS_TOKEN=ghp_xxxxxxxxxxxxx
     ```
   - Add to `.kiro/settings/mcp.json`:
     ```json
     {
       "mcpServers": {
         "github": {
           "command": "uvx",
           "args": ["mcp-server-github"],
           "env": {
             "GITHUB_PERSONAL_ACCESS_TOKEN": "${GITHUB_PERSONAL_ACCESS_TOKEN}"
           }
         }
       }
     }
     ```
   - Restart Kiro / reconnect MCP

5. **Test**
   - Ask Wip to list recent commits on 2cld/wip
   - Ask Wip to list open issues
   - Verify commits show as wip-2cld in git log

### Step-by-Step: Create Wip Gitea Account

1. **Create account**
   - Go to [gitea.cat9.me](https://gitea.cat9.me)
   - Register with email: wip@horseoff.com
   - Username: `wip`

2. **Generate API token**
   - Settings → Applications → Generate New Token
   - Token name: `kiro-mcp`
   - Copy token, store in `.local/.env`

3. **Add to relevant orgs/repos**
   - Login as nsadmin or cat
   - Add wip user to nsadmin org with read access
   - Grant access to: ns-account, nsclai, nspwa, ns-site-template, docker-compose

4. **Configure Kiro MCP** (when Gitea MCP server is available)
   - May need custom API wrapper or generic REST MCP
   - Document approach once tested

### Step-by-Step: Setup Wip Google Calendar Access

1. **Calendar is already available** via the wip@horseoff.com Google account

2. **Share your calendars with Wip**
   - Open Google Calendar as your main persona
   - Settings → calendar → Share with specific people
   - Add wip@horseoff.com with "See all event details" permission
   - Repeat for each calendar Wip should see

3. **Configure Google Calendar MCP** (when available)
   - Will need OAuth2 or service account credentials
   - Store in `.local/.env`
   - Document approach once tested

---

## Integration Phases

### Phase 0: Identity Setup ← IN PROGRESS
 - [X] Create wip@horseoff.com in Google Workspace
 - [ ] Add wip@2cld.net alias (deferred - Cloudflare later)
 - [X] Setup Chrome profile (ho-wip)
 - [ ] Update cat2net + ops-account-management.md
 - [X] Set git identity for wip repo (ho-wip / wip@horseoff.com)
 - [X] Create GitHub account (wip@horseoff.com) → [ho-wip](https://github.com/ho-wip)
 - [X] Add as collaborator on 2cld/wip
 - [ ] Create Gitea account (wip@horseoff.com)

### Phase 1: GitHub (2cld/wip) ✅ COMPLETE
 - [X] Generate GitHub personal access token (classic, repo scope)
 - [X] Add wip as collaborator on 2cld/wip
 - [X] Configure GitHub MCP server in `.kiro/settings/mcp.json` (npx @modelcontextprotocol/server-github)
 - [X] Test: pull recent commits during daily check-in ✅
 - [X] Test: list open issues
 - [X] Documented in this file

### Phase 2: Gitea (cat9.me)
 - [ ] Generate Gitea API token
 - [ ] Add wip to nsadmin org
 - [ ] Configure Gitea MCP server or API access
 - [ ] Test: pull ns-account, nsclai, nspwa activity
 - [ ] Test: surface open issues per Epic
 - [ ] Document results in this file

### Phase 3: Google Calendar
 - [ ] Share calendars with wip@horseoff.com
 - [ ] Configure Google Calendar API / MCP access
 - [ ] Test: pull today's events during morning check-in
 - [ ] Test: auto-detect missed check-ins from calendar activity
 - [ ] Document results in this file

### Phase 4: Multi-Identity Coordination
 - [ ] Map project personas to accounts (see ops-account-management.md)
 - [ ] Wip can check email/notifications across personas
 - [ ] Wip can coordinate "other me's" across projects
 - [ ] Document identity patterns in PROCESS.md

---

## Links
 - [2cld/wip GitHub](https://github.com/2cld/wip)
 - [gitea.cat9.me](https://gitea.cat9.me)
 - [Google Admin](https://admin.google.com) (login as cat@horseoff.com)
 - [ops-account-management.md](./ops-account-management.md) - persona map
 - [cat2net Google Sheet](https://docs.google.com/spreadsheets/d/1LdyZlFieSd_1APTbG0QahfwZgqBaA9PigO9_5SPSkmk/edit?gid=1959043129#gid=1959043129)

## Notes
 - wip@horseoff.com is the mailbox, wip@2cld.net is the public-facing alias
 - Start with GitHub since wip repo is already there
 - Gitea may need custom API wrapper or generic REST MCP
 - Google Calendar is hardest but most impactful for daily planning
 - All credentials go in `.local/.env` (gitignored)
 - Wip identity accounts let you audit AI vs human activity in git log
