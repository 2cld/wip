[edit](https://github.com/2cld/wip/edit/main/README.md)

Click for [Meeting Link](https://meet.google.com/dov-vkev-tzm)

# Daily Check-In
**Current Streak:** 1 day | **Last Check-In:** 2026-04-05

## Today
**Top 3 Priorities for Sunday, April 5:**
1. ⚠️ CTrees 1040 (April 14 deadline - 9 days) - poke at it today
2. Sunday Evening Review ✓
3. QBOL RoutePrint - get ready for Mark Monday

### History

<details markdown="1">
<summary><strong>This Week</strong> </summary>

 - **2026-04-05 (Sun):** 🎯 CTrees 1040 + Sunday Evening Review + QBOL continued
 - **2026-04-04 (Sat):** ✓ QBOL RoutePrint + calendar entries + repo updates (missed wip check-in)
 - **2026-04-03 (Fri):** ✓ HWPC RoutePrint + QBOL route tickets all day
 - **2026-04-01 (Wed):** ✓ RoutePrint research + notes captured + ghadmin added to wip.2cld.net
 - **2026-03-31 (Tue):** ✓ HWPC migration to QBOL complete + paycheck issued ✓ + Trink proxmox auto-config started + netstack.org/2cld.net docs dig started
 - **2026-03-30 (Mon):** ✓ Arrived O'Fallon + setup ✓ 1040-X mailed ✓ insurance checked ✓ Kenton + SJen check-ins ✓ packed kit
- **2026-03-29 (Sun):** ✓ 1040-X signed + BHay 1040 FILED ✓ + ReportPrint/gReportPrint started + Steve Jennings call
- **2026-03-28 (Sat):** ✓ Traveled to Winfield + QB2020 up + customers imported
- **2026-03-27 (Fri):** ✓ QBOL invoice forms @ River Place + vehicle maintenance with Brad ✓ + Mark ran routes (good till 4/7) + QBOL final migration FAILED (8hr timeout) + Iowa wins 🏀 Iowa State out 😬

</details>

---

##### Current Epics

<details markdown="1">
<summary><strong>EPIC: QBOL HWPC Route Print with Invoice import / export</strong> </summary>

<span>@type:task @priority:high @project:[cat9-hwpc-qbol](./wip-detail/hwpc-qbol-notes.md)</span>

 - [cat9-hwpc-qbol wip-detail](./wip-detail/hwpc-qbol-notes.md)
 - [ns-account gitea](https://gitea.cat9.me/nsadmin/ns-account)
 - [hwpc.2cld.net](https://hwpc.2cld.net/) - operational docs, procedures, ToDo

**✅ RESOLVED (2026-04-01):** HWPC migration to QBOL complete - paycheck issued! QB2020 used as migration path.

**⚠️ NEXT:** RoutePrint invoice import to QBOL - Mark routes expire 4/7, must work by Monday.

**Definition of Done:**
 - [X] Route print functionality created
 - [X] Create Looney Tunes (LT) example Data
 - [X] Create LT smoke demo TRAINING-DEMO.md
 - [ ] Looney Tunes (LT) demo
   - [X] LT docs/explain
   - [X] LT docs/stepbystep
   - [ ] LT Video Demo
   - [ ] Post LT demo
   - [ ] remote access demo server
 - [ ] Imports cvs
   - [ ] Route ID import
   - [ ] customer import
   - [ ] customer service location import
   - [ ] customer invoice import
 - [ ] Export cvs
   - [ ] Route ID export
   - [ ] customer export
   - [ ] customer service location export
   - [ ] customer invoice export
 - [ ] Work out lifecycle demo
   - [ ] LT Route ID import
   - [ ] LT customer import
   - [ ] LT customer service location import
   - [ ] LT customer invoice import
 - [ ] Test Route Print with old QB2024
 - [ ] Test Route Print with new QBOL
 - Connect Wip to Google Calendar
 - separate Account data from qb_migration

</details>

<details markdown="1">
<summary><strong>EPIC: Netstack federation deployments</strong> </summary>

<span>@type:task @priority:high @project:[ns-site-template](https://gitea.cat9.me/nsadmin/ns-site-template)</span>

 - [trinknotes wip-detail](./wip-detail/trinknotes202503.md)
 - [ns-site-template gitea](https://gitea.cat9.me/nsadmin/ns-site-template)
 - [docker-compose gitea](https://gitea.cat9.me/nsadmin/docker-compose)

Working with Trink from O'Fallon through April on federation deployments.

**Definition of Done:**
 - [ ] Kickoff sync with Trink
 - [ ] Document target sites + federation topology
 - [ ] ns-site-template deployment plan
 - [ ] First site deployed + validated
 - [ ] Federation between sites working
 - [ ] Document deployment procedure 

</details>

<details markdown="1">
<summary><strong>EPIC: Wip repo + issue integration</strong> </summary>

<span>@type:task @priority:medium @project:[nsadmin](https://gitea.cat9.me/nsadmin)</span>

Connect Wip to project repos so it can monitor issue status, PRs, and project health during daily/weekly reviews.

**Definition of Done:**
 - [ ] Gitea API access from Wip context (ns-account, nsclai, nspwa, etc.)
 - [ ] GitHub API access from Wip context (2cld/wip)
 - [ ] Google Calendar API access from Wip context
 - [ ] Daily check-in can surface open issues / blockers from active Epics
 - [ ] Weekly review can pull repo activity summary per Epic
 - [ ] Document integration pattern in PROCESS.md

</details>

<details markdown="1">
<summary><strong>EPIC: Setup LLC payments</strong> </summary>

<span>@type:task @priority:medium @project:[cat9-acct-LLC](./wip-detail/LLC-EOY.md)</span>

**Definition of Done:**
 - [ ] FHKlopFarms Utilites
 - [ ] FHKlopFarms IA Land Tax
 - [ ] TreesAES Utilites
 - [ ] TreesAES IA Land Tax
 - [ ] TreesAES ACI*Windstream
 - [ ] TH Twig ACI*WINDSTREAM
 - [ ] TH Twig USCELL
 - [ ] Checkk Insurance payments @type:task @project:accounting
 - [ ] Make list of Rental jobs @type:task @project:property

</details>

<details markdown="1">
<summary><strong>EPIC: MediaVolume cleanup old data</strong> </summary>

<span>@type:task @priority:medium @project:[ops-storage-management](./docs/ops-storage-management.md)</span>

**Definition of Done:**
 - [ ] Document storage
 - [ ] tar CATPhotos
 - [ ] Document proceedure in [docs/ops-storage-management.md](docs/ops-storage-management.md)
 - [X] git commit Account
 - [X] Backup Account
 - [X] tar CATMusic 13G
 - Fix cf TV network at BFletch @type:task @project:personal
 - Fix iPhone storage @type:task @project:personal
 - Fix iWatch connection @type:task @project:personal
 - Setup remote storage cf wf sl @type:task @project:nsadmin
 - video monitors online @type:task @project:personal
 - ha frigit @type:task @project:personal
 - ha tivo @type:task @project:personal
 - Review sl.2cld.net network and storage stuff @type:task @project:nsadmin

</details>

---

# Inbox
**Items to be processed and tagged during morning routine**

 - Gus: Plex UI file organization for movies and music @type:task @project:gus @priority:medium
 - Trink: Proxmox NAS rebuild - tie into netstack.org properly @type:task @project:nsadmin @priority:high

---

###### Other

<details markdown="1">
<summary><strong>Calendar Event Monitor</strong> </summary>

# Calendar Event Monitor
**Format:** YYYY-MM-DD - Task Description

 - **2026-04-01:25** - Gus visit and appointments @type:event @priority:high @project:gus

 - **2026-04-14** - ~~1040 2025 BHay Send~~ ✓ FILED 2026-03-29 @project:accounting
 - **2026-04-14** - ⚠️ 1040 2025 CTrees Send @type:task @priority:high @project:accounting

 - **2026-05-01** - Wendell Sanders honored @ ISU Ames @type:event @priority:high @project:personal
 - **2026-05-01** - Touch base MaRay + Aunt Carol (en route to Ames) @type:task @priority:medium @project:personal

 - **2026-04-30** - IA 1065 manual file [googleai instructions](https://share.google/aimode/wgpBIcMB9nfwryieG) @type:link @project:accounting
 - **2026-04-30** - IA 1065 no income or expense [Googleai](https://share.google/aimode/NtFvRnACVfHpMpn8Q) @type:link @project:accounting

 - **2026-09-30** - IA auto-extension if no tax payment - Cheaper eTax forms [olt.com](https://www.olt.com/main/oltstateff/ia.php) @type:link @project:accounting

</details>

---

<details markdown="1">
<summary><strong>Yesterday tasks</strong> </summary>

# Yesterday (Sat Apr 4)
✓ QBOL RoutePrint work continued
✓ Calendar entries + repo updates
- Missed wip check-in (streak reset from 35 → 1)

</details>

---

<details markdown="1">
<summary><strong>Open code Projects</strong> </summary>

**Projects getting active attention**

## nsadmin [https://gitea.cat9.me/nsadmin](https://gitea.cat9.me/nsadmin)
 - [nsqbooks](https://gitea.cat9.me/nsadmin/nsqbooks) 
   - [issues](https://gitea.cat9.me/nsadmin/nsqbooks/issues)
   - ?? cat9fin cat C:/Users/cat/code/nsqbooks
 - [ns-site-template](https://gitea.cat9.me/nsadmin/ns-site-template) 
   - [issues](https://gitea.cat9.me/nsadmin/ns-site-template/issues)
   - ?? none
 - [nsclai](https://gitea.cat9.me/nsadmin/nsclai) 
   - [issues](https://gitea.cat9.me/nsadmin/nsclai/issues)
   - ?? nsUb2404hv nsadmin ~/code/nsclai
   - IronClaw [https://github.com/nearai/ironclaw](https://github.com/nearai/ironclaw)
   - 4 and 8 node ai clusters [yt](https://www.youtube.com/watch?v=QJqKqxQR36Y)
   - Review [yt-Lex OpenClaw AI dev workflow](https://youtu.be/wKy1_KLcxcs?si=OUDFe3NGp_ilSfY-)
   - Economist [notebookLM](https://notebooklm.google.com/notebook/5881d15d-7b82-4002-8613-df59b6eece4c)
 - [nsmedia](https://gitea.cat9.me/nsadmin/nsmedia) 
   - [issues](https://gitea.cat9.me/nsadmin/nsmedia/issues)
   - ?? 
 - [nsgctime](https://gitea.cat9.me/nsadmin/nsgctime) 
   - [issues](https://gitea.cat9.me/nsadmin/nsgctime/issues)
   - ?? nsUb2404hv nsadmin ~/code/nsclai
 - [nscallbot](https://gitea.cat9.me/nsadmin/nscallbot) 
   - [issues](https://gitea.cat9.me/nsadmin/nscallbot/issues)
   - ?? nsUb2404hv nsadmin ~/code/nsclai
 - [nspwa](https://gitea.cat9.me/nsadmin/nspwa) 
   - [issues](https://gitea.cat9.me/nsadmin/nspwa/issues)
   - nsUb2404hv nsadmin ~/code/nspwa
 - [nspwa-test](https://gitea.cat9.me/nsadmin/nspwa-test) 
   - [issues](https://gitea.cat9.me/nsadmin/nspwa-test/issues)
   - nsUb2404hv nsadmin ~/code/nspwa-test
 - [gitea-to-github](https://gitea.cat9.me/nsadmin/gitea-to-github) 
   - [issues](https://gitea.cat9.me/nsadmin/gitea-to-github/issues)
   - ?? 
 - [docker-compose](https://gitea.cat9.me/nsadmin/docker-compose) 
   - [issues](https://gitea.cat9.me/nsadmin/docker-compose/issues)
   - nsUb2404hv nsadmin ~/code/docker-compose
   - nsUb2404hv nsadmin ~/code/docker
 - [2cld](https://gitea.cat9.me/nsadmin/2cld) 
   - [issues](https://gitea.cat9.me/nsadmin/2cld/issues)
   - ?? 

## hwpc
 - [hwpc.2cld.net](https://hwpc.2cld.net) - primary ops site
 - [ns-account gitea](https://gitea.cat9.me/nsadmin/ns-account) - dev repo
 - [hwpc github](https://github.com/2cld/hwpc)
 - [hwpc-gs](https://github.com/grasshorse/hwpc-gs)
 - [hwpc-bug](https://github.com/grasshorse/hwpc-bug)

## Account https://gitea.cat9.me/cat
 - [catnotes](https://gitea.cat9.me/cat/catnotes)
 - [cat9llc](https://gitea.cat9.me/cat/cat9llc)
 - need to arch [Account]()

</details>

---

##### Reference

<details markdown="1">
<summary><strong>Projects</strong> </summary>

**Project reference links getting active attention**

 - [Wip-detail](./wip-detail/)
 - [tasks](./tasks)
 - [notes](./docs/)
   - [docs/random-links.md](./docs/random-links.md)
   - [docs/ai-cli-research](./docs/ai-cli-research)
 - [tbd]()

</details>
