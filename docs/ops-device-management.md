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

### iPhone 11 Pro Cleanup (Device #1 - "Alice's iPhone")

**Context:** This is the daily driver. Was Alice's (mom), on Brad's family plan. After Pixel 7 broke in Hawaii, lots of Chris's Google stuff migrated here (Google Auth, MS Auth, airline tickets, etc.). Need to extract everything before removing from Brad's account.

**⚠️ DO NOT factory reset until all steps are complete.**

#### Phase 1: Document what's on the phone
 - [ ] List all signed-in accounts (Settings → top of screen, Mail, etc.)
      - alicetrees@icloud.com (users account)
      - Mail Accounts
         - iCloud: alicetrees@icloud.com
         - gmail: alktrees@gmail.com
      - Google has
         - alktrees@gmail.com
         - christrees@gmail.com
         - thtwigllc@gmail.com
         - ghadmin@horseoff.com
 - [ ] Export Google Authenticator codes
 - [ ] Screenshot Microsoft Authenticator accounts
 - [ ] Note any airline apps with active tickets/loyalty accounts
 - [ ] Check for any other 2FA apps (Authy, etc.)
 - [ ] Document which phone numbers are tied to this device for SMS 2FA

#### Phase 2: Move authenticator apps FIRST (before anything else)
 - [ ] Google Authenticator: export/transfer to another device (#4 CATiPhone8 or #7 PH-1)
   - Open Google Auth → menu → Transfer accounts → Export
   - Scan QR on target device
 - [ ] Microsoft Authenticator: backup to cloud / transfer
   - Settings → Backup → ensure cloud backup is on
   - Restore on target device
 - [ ] Any other 2FA: document and transfer

#### Phase 3: Extract data
 - [ ] Photos: check what's in iCloud (Brad's plan) vs local
   - Download all photos from iCloud before removing from Brad's plan
   - Move to Google Photos (christrees@gmail.com) or local backup
 - [ ] Google Timeline data: check if accessible via Google Maps → Timeline
   - Export from [timeline.google.com](https://timeline.google.com) if available
 - [ ] Contacts: verify synced to Google (christrees@gmail.com)
 - [ ] Notes: check for any Apple Notes that need saving
 - [ ] Voicemail: save any important voicemails
 - [ ] Text messages: any important threads to archive?

#### Phase 4: Broken Pixel 7 data recovery
 - [ ] Check if Pixel 7 powers on at all (even with cracked screen)
 - [ ] If screen works partially: connect to Wi-Fi, verify Google backup
 - [ ] Google Timeline: should be in Google account already (cloud-synced)
 - [ ] Photos: check Google Photos (christrees@gmail.com) for auto-backup
 - [ ] If screen dead: try USB-C to HDMI adapter for screen output
 - [ ] Last resort: professional data recovery

#### Phase 5: Remove from Brad's account
 - [ ] Confirm all photos are off iCloud
 - [ ] Sign out of Brad's iCloud (Settings → [name] → Sign Out)
 - [ ] Remove from Brad's Family Sharing
 - [ ] Remove from Find My (Brad may need to do this from his end)
 - [ ] Factory reset
 - [ ] Setup fresh with christrees@gmail.com / c9t@me.com

#### Phase 6: Setup as personal device
 - [ ] Sign in with own iCloud (c9t@me.com)
 - [ ] Add Google account (christrees@gmail.com) for Calendar, Mail, Contacts
 - [ ] Configure Siri → Google Calendar (for Wip voice input)
 - [ ] Install: Google Auth, MS Auth, Google Maps, GitHub mobile
 - [ ] Test: voice → Google Calendar event with #cat9-wip code
 - [ ] Update inventory table above

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

| # | Device | OS | Name | Status | Account | Target Use | Network |
|---|--------|-----|------|--------|---------|------------|---------|
| 1 | iPhone 11 Pro | iOS | Alice's iPhone | Active - on Brad's family plan | Brad's iCloud | Personal / Wip voice input - NEEDS CLEANUP | USCellular TreesAES |
| 2 | iPhone 6 | iOS 12.5.5 | Chris Trees iPhone6 | Powers up, cracked screen | christrees | Parts / archive | ?? na |
| 3 | iPhone 8 | iOS 15.6.1 | Alice's iPhone (2) | Powers up, lock code known | Alice's iCloud | Cleanup candidate | ?? na |
| 4 | iPhone 8 | iOS 15.5 | CATiPhone8 | Working, Ting Wi-Fi carrier | cat | Best candidate - has carrier | Ting |
| 5 | iPhone 8 | iOS ?? | Andrea's iPhone 8 | Locked - passcode unknown | Andrea's iCloud | Need passcode or reset | ?? na |
| 6 | iPhone 8 | iOS ?? | Unknown | Dead screen, vibrates on home button | Unknown | Parts / screen swap | ?? na |
| 7 | Essential PH-1 | Android | PH-1 (Chris Trees) | Working, cracked bottom screen | christrees | HWPC field service test | ?? na |
| 8 | Alcatel | Windows Phone | TBD | Charging | TBD | Curiosity / archive | Ting |

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
