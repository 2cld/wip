# ops-device-management

Managing devices for family and clients across multiple organizations.

## iPhone Device Management

### iPhone Cleanup Procedure
Context: When inheriting or repurposing an iPhone (like mom's old phone) - need a standard process to ensure clean handoff.

**External References:**
- Apple Support: [What to do before selling/giving away iPhone](https://support.apple.com/en-us/HT201351)
- Apple Support: [Transfer data from previous iPhone](https://support.apple.com/en-us/HT201269)
- User tracking: [cat2net users](https://docs.google.com/spreadsheets/d/1LdyZlFieSd_1APTbG0QahfwZgqBaA9PigO9_5SPSkmk/edit?gid=1959043129#gid=1959043129)

**Process:**
1. **Backup current data** (if needed)
   - iCloud backup or iTunes/Finder backup
   - Verify backup completed successfully
2. **Sign out of accounts**
   - Settings > [Your Name] > Sign Out (iCloud)
   - Settings > iTunes & App Store > Sign Out
3. **Erase device**
   - Settings > General > Transfer or Reset iPhone > Erase All Content and Settings
   - Enter passcode if prompted
4. **Remove from Find My**
   - Should happen automatically during erase
   - Verify at icloud.com/find
5. **Document transfer**
   - Update device ownership in [cat2net users](https://docs.google.com/spreadsheets/d/1LdyZlFieSd_1APTbG0QahfwZgqBaA9PigO9_5SPSkmk/edit?gid=1959043129#gid=1959043129)
   - Note: Previous owner, new owner, date transferred

**Current Tasks:**
- [ ] Mom's iPhone cleanup - [Task in README](../README.md#inbox)

---

## Apple Watch Management

### Watch Transfer Procedure
Context: Transferring Apple Watch from Clint - need to unpair from his iPhone and pair to mine.

**External References:**
- Apple Support: [Unpair and erase Apple Watch](https://support.apple.com/en-us/HT204568)
- Apple Support: [Set up Apple Watch](https://support.apple.com/en-us/HT204505)
- User tracking: [cat2net users](https://docs.google.com/spreadsheets/d/1LdyZlFieSd_1APTbG0QahfwZgqBaA9PigO9_5SPSkmk/edit?gid=1959043129#gid=1959043129)

**Process:**
1. **Unpair from previous iPhone** (Clint's phone)
   - Keep watch and iPhone close together
   - Open Watch app on iPhone
   - Go to My Watch tab > All Watches
   - Tap info button next to watch > Unpair Apple Watch
   - Enter Apple ID password to remove Activation Lock
   - Creates automatic backup
2. **Erase watch** (if not done during unpair)
   - Settings > General > Reset > Erase All Content and Settings
3. **Pair to new iPhone** (my phone)
   - Bring watch close to iPhone
   - Wait for "Use your iPhone to set up this Apple Watch" message
   - Tap Continue
   - Follow on-screen instructions
4. **Restore from backup** (optional)
   - Choose backup from Clint's watch if keeping settings
   - Or set up as new watch
5. **Document transfer**
   - Update device ownership in [cat2net users](https://docs.google.com/spreadsheets/d/1LdyZlFieSd_1APTbG0QahfwZgqBaA9PigO9_5SPSkmk/edit?gid=1959043129#gid=1959043129)
   - Note: Previous owner (Clint), new owner, date transferred

**Current Tasks:**
- [ ] iWatch transfer from Clint - [Task in README](../README.md#inbox)

---

## Device Inventory

Track all managed devices in [cat2net users](https://docs.google.com/spreadsheets/d/1LdyZlFieSd_1APTbG0QahfwZgqBaA9PigO9_5SPSkmk/edit?gid=1959043129#gid=1959043129)

**Device Types:**
- iPhones
- Apple Watches
- iPads
- Macs
- Windows PCs
- Android devices

### Phone Inventory (2026-04-26)

| # | Device | OS | Name | Status | Account | Target Use |
|---|--------|-----|------|--------|---------|------------|
| 1 | iPhone 11 Pro | iOS | Alice's iPhone | Active - on Brad's family plan | Brad's iCloud | Personal / Wip voice input - NEEDS CLEANUP |
| 2 | iPhone 6 | iOS 12.5.5 | Chris Trees iPhone6 | Powers up, cracked screen | christrees | Parts / archive |
| 3 | iPhone 6 | iOS 15.6.1 | Alice's iPhone (2) | Powers up, lock code known | Alice's iCloud | Cleanup candidate |
| 4 | iPhone 8 | iOS 15.5 | CATiPhone8 | Working, Ting Wi-Fi carrier | cat | Best candidate - has carrier |
| 5 | iPhone 8 | iOS ?? | Andrea's iPhone 8 | Locked - passcode unknown | Andrea's iCloud | Need passcode or reset |
| 6 | iPhone 8 | iOS ?? | Unknown | Dead screen, vibrates on home button | Unknown | Parts / screen swap |
| 7 | Essential PH-1 | Android | PH-1 (Chris Trees) | Working, cracked bottom screen | christrees | HWPC field service test |
| 8 | Alcatel | Windows Phone | TBD | Charging | TBD | Curiosity / archive |

### Phone Cleanup Process (per device)
 - [ ] Power on, check current state
 - [ ] Document: model, iOS/Android version, storage, current account
 - [ ] Backup any needed data
 - [ ] Sign out of all accounts (iCloud, Google, etc.)
 - [ ] Factory reset
 - [ ] Setup with appropriate account (personal, HWPC, or test)
 - [ ] Test: web browsing works
 - [ ] Test: Google Calendar access (for Wip voice input)
 - [ ] Test: HWPC RP web access (for field service suitability)
 - [ ] Update inventory table above
 - [ ] Update cat2net

### Multi-Purpose Testing Goals
 - **Personal/Wip:** Can this phone do voice → Google Calendar for Wip check-ins?
 - **HWPC Field Service:** Can Mark use this for hwpc-rp ticket management? (nspwa offline-first)
 - **Federation Node:** Document as client device in netstack federation topology
 - Results go to:
   - This doc (inventory + status)
   - [hwpc.2cld.net](https://hwpc.2cld.net) (HWPC field test results)
   - ns-site-template / federation docs (client portal management)
