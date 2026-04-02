# HWPC QBOL Notes

**Operational detail lives at:** [https://hwpc.2cld.net/](https://hwpc.2cld.net/)

## Project: qb_migration
**Location:** Account/_tools/qb_migration
**Repo:** [ns-account gitea](https://gitea.cat9.me/nsadmin/ns-account)
**Status:** ✅ Migration complete - paycheck issued 2026-03-31

### Key Milestones
 - 2026-03-14: route-ticket-printing spawned from qb_migration testing
 - 2026-03-21: Production customer/route import working, full month auto-scheduled
 - 2026-03-22: QB2024→QBOL migration started (Mar 22 backup)
 - 2026-03-27: Final QBOL migration failed (8hr import timeout)
 - 2026-03-28: QB2020 up + customers imported as alternative path
 - 2026-03-31: HWPC migration to QBOL complete - paycheck issued

## Project: route-ticket-printing
**Status:** In Progress - RoutePrint invoice import to QBOL target before Apr 5

### Goal
Prepare and manage the HWPC field service team's route tickets outside of QBOL.

### Next Steps
 - [ ] RoutePrint invoice import to QBOL (gcode to QBOL)
 - [ ] Test on developer.intuit.com
 - [ ] Define route ticket format and fields
 - [ ] Build printing workflow
 - [ ] Test with HWPC field service team

### Links
 - [hwpc.2cld.net QBOL section](https://hwpc.2cld.net/) - print ticket procedures, tax reports, ToDo
 - [ns-account gitea](https://gitea.cat9.me/nsadmin/ns-account) - dev repo
