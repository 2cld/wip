[edit](https://github.com/2cld/wip/edit/main/README.md)

Click for [Meeting Link](https://meet.google.com/dov-vkev-tzm)

# Daily Check-In
**Current Streak:** 13 days | **Last Check-In:** 2026-04-17

## Today
**Top 3 Priorities for Friday, April 17:**
1. HWPC continued from Winfield
2. Call Brad Nordyke about trip to see Steve
3. Netstack / media cleanup

### History

<details markdown="1">
<summary><strong>This Week</strong> </summary>

 - **2026-04-17 (Fri):** 🎯 HWPC from Winfield + Brad Nordyke call + netstack
 - **2026-04-16 (Thu):** ✓ Arrived Winfield + setup + long visit with Bev and Tim
 - **2026-04-15 (Wed):** ✓ HWPC reconciles + Mark review ✓ + emailed MaRay ✓
 - **2026-04-14 (Tue):** ✓ HWPC (few hrs) + NS template deployment test for sl.2cld.net (github push issues cf vs sl repo)
 - **2026-04-13 (Mon):** ✓ HWPC all day + new dentist check with Steve + FIELD-SESSIONS.md triage T1-21 + Mark meeting 5-6 more routes printed
 - **2026-04-12 (Sun):** ✓ Sunday Evening Review + Mark review - first batch of routes processed ✓
 - **2026-04-11 (Sat):** ✓ HWPC mobile-first UI + media data cleanup started + netstack federation started + NAS died (DS-411+II)
 - **2026-04-10 (Fri):** ✓ CTrees extension filed ✓ + hwpc-rp ONLINE + phone tested ✓
 - **2026-04-09 (Thu):** ✓ HWPC all day + AR + Tax sync implemented + SEED process working
 - **2026-04-08 (Wed):** ✓ HWPC - A/R sync approach decided (monthly QBOL reconciliation)
 - **2026-04-07 (Tue):** ✓ HWPC + routes for Mark + MaRay + Aunt Carol check-ins ✓
 - **2026-04-06 (Mon):** ✓ Gus dentist + HWPC + Mark meeting

</details>

---

##### Current Epics

<details markdown="1">
<summary><strong>EPIC: QBOL HWPC Route Print with Invoice import / export</strong> </summary>

<span>@type:task @priority:high @project:[cat9-hwpc-qbol](./wip-detail/hwpc-qbol-notes.md)</span>

 - [cat9-hwpc-qbol wip-detail](./wip-detail/hwpc-qbol-notes.md)
 - [ns-account gitea](https://gitea.cat9.me/nsadmin/ns-account)
 - [hwpc-rp production](http://rp.hwpc.net:5005/routes/monthly-dashboard) http://10.147.17.218:5005/routes
 - [FIELD-SESSIONS](tbd) in cat2fin C:\cat9finshare\Account\hwpc-rp\docs\FIELD-SESSIONS.md
 - [hwpc.2cld.net prod](https://hwpc.2cld.net:5005/routes) - operational docs, procedures, ToDo

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

 - Call Brad Nordyke about trip to see Steve before he leaves @type:task @project:personal @priority:medium (this week)
 - NAS repair: Synology DS-411+II - CR1220 coin battery + diagnose @type:task @project:nsadmin @priority:high
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
 - **2026-04-14** - 1040 2025 CTrees - EXTENSION FILED (auto-file test via Account tools) @type:task @priority:medium @project:accounting
 - **2026-10-15** - ⚠️ 1040 2025 CTrees Send (extended deadline) @type:task @priority:high @project:accounting - tickler: Sun + Thu

 - **2026-05-01** - Wendell Sanders honored @ ISU Ames @type:event @priority:high @project:personal
 - **2026-05-01** - Touch base MaRay + Aunt Carol (en route to Ames) @type:task @priority:medium @project:personal
 - **2026-05-01** - Cousin Neil at Aunt Carol's + Wendell + Brian in area @type:note @project:personal
 - **TBD** - Tell MaRay when in Mt. Pleasant (visit him + his mom) @type:task @priority:medium @project:personal

 - **2026-04-30** - IA 1065 manual file [googleai instructions](https://share.google/aimode/wgpBIcMB9nfwryieG) @type:link @project:accounting
 - **2026-04-30** - IA 1065 no income or expense [Googleai](https://share.google/aimode/NtFvRnACVfHpMpn8Q) @type:link @project:accounting

 - **2026-09-30** - IA auto-extension if no tax payment - Cheaper eTax forms [olt.com](https://www.olt.com/main/oltstateff/ia.php) @type:link @project:accounting

</details>

---

<details markdown="1">
<summary><strong>Yesterday tasks</strong> </summary>

# Yesterday (Thu Apr 16)
✓ Arrived Winfield + setup
✓ Long visit with Bev and Tim

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
