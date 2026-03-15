# HWPC QBOL Notes

## Project: qb_migration
**Location:** Account/_tools/qb_migration
**Status:** In Progress - Task 25 reached

### Overview
Migration tooling for HWPC QuickBooks operations. Building tools to manage the transition and improve field service workflows.

## Project: route-ticket-printing
**Status:** New - spawned from qb_migration testing

### Background
During testing of the proto Route Ticket management portal (task 25 of qb_migration), the HWPC team provided early feedback that led to process modification needs. The route management process in QB2024 had created significant ticket management issues. The old paper ticket management process had served HWPC effectively in the past.

### Goal
Prepare and manage the HWPC field service team's route tickets outside of QBOL. Return to a more effective ticket management workflow that addresses the issues created by QB2024's route management.

### Key Decisions
- 2026-03-14: Created route-ticket-printing as separate feature project from qb_migration
- 2026-03-14: HWPC team feedback confirmed paper-based ticket management was more effective than QB2024 digital route management

### Next Steps
- [ ] Define route ticket format and fields
- [ ] Build printing workflow
- [ ] Test with HWPC field service team
- [ ] Integrate with qb_migration data pipeline
