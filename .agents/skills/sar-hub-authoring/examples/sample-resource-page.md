---
title: "Garmin inReach Standard Field Presets & Team Setup"
description: "A standardized preset message template and map sharing workflow for Garmin inReach devices on Canadian Ground SAR incidents."
category: "Communications"
jurisdiction:
  - "National"
tags:
  - "inreach"
  - "satellite-comms"
  - "communications"
  - "caltopo"
  - "tracking"
maintainer: "Canadian GSAR Comms Working Group"
date_updated: 2026-10-19
---

# Garmin inReach Standard Field Presets & Team Setup

Satellite communicators like the Garmin inReach are standard safety gear for Canadian search teams working out of cell range. However, when every device on a team uses different preset messages or custom text formats, Incident Command Posts (ICPs) spend unnecessary time decoding check-ins instead of managing the search.

Standardizing preset messages across all team devices makes sure field updates are instant, consistent, and free of satellite character charges. This guide provides a field-tested preset message lineup and explains how to feed live inReach tracks directly into your incident map.

---

## Download Preset & Configuration Templates

<div class="grid cards" markdown>

-   :material-file-table-outline:{ .lg .middle } **Standard Message Lineup (.xlsx)**

    ---

    Spreadsheet template containing standard 3-button presets and quick-text messages ready to copy into your Garmin Explore team account.

    [:material-download: Download Preset Matrix (.xlsx)](../../assets/files/forms/inreach-presets-standard.xlsx){ .md-button .md-button--primary }

-   :material-file-pdf-box:{ .lg .middle } **CalTopo Feed Setup Checklist (.pdf)**

    ---

    Printable one-page field cheat sheet for linking an inReach group tracking feed into an active CalTopo map.

    [:material-download: Download Setup Checklist (.pdf)](../../assets/files/forms/caltopo-inreach-feed-checklist.pdf){ .md-button }

</div>

---

## Standard inReach Message Lineup

Garmin devices have three permanent "Check-in / Preset" buttons that send free, unlimited messages with your GPS location to pre-programmed team phone numbers or email addresses:

| Button | Standard Message | When Field Teams Send It | What Base Does With It |
| :--- | :--- | :--- | :--- |
| **Preset 1** | `CHECK-IN OK - Continuing Task` | Every 30 or 60 minutes during routine search operations. | Logs routine safety check-in on the radio/comms log. No reply required. |
| **Preset 2** | `DELAYED - All OK, terrain or obstacle slow` | When progress slows down due to blowdown, cliffs, or thick brush. | Updates estimated task completion time on the planning board. |
| **Preset 3** | `RETURNING TO BASE - Task complete or suspended` | When debriefed or instructed to return to ICP / staging. | Prepares debrief area and tracks team transit time. |

### Recommended Quick-Text Messages
Quick-texts are pre-typed custom messages that searchers can select quickly on their device screen without typing letter-by-letter:

1. `CLUE LOCATED - Holding position, standby for photos/coords`
2. `SUBJECT FOUND - Ambulatory / uninjured, standing by`
3. `SUBJECT FOUND - Non-ambulatory / medical support needed`
4. `RADIO DEAD ZONE - Switching primary comms to inReach`
5. `NEED ASSISTANCE - Request team support (non-emergency)`

---

## How to Set Up Team Devices

### Method 1: Set Up Default Presets in Garmin Explore (Team Admin)

To ensure all team inReach units share the exact same setup:

1. Log into your team's **Garmin Explore** portal (`explore.garmin.com`).
2. Go to **Plans & Devices** and select your team device profile.
3. Under **Messages**, set the 3 Preset Messages to match the table above.
4. Set the recipient address to your team's designated ops email or SMS dispatch number (e.g., your SAR trailer inbox or online dispatch software).
5. Sync each handheld unit using the Garmin Messenger or Explore app before placing it in the response vehicle.

---

### Method 2: Link Live inReach Tracking to CalTopo

If your team tracks field members live in CalTopo:

1. In Garmin Explore, navigate to the **Social** tab and confirm MapShare is turned on.
2. Copy your team's MapShare web feed link and feed password.
3. Open your active CalTopo incident map.
4. In the left-hand menu, click **Add** > **Live Tracking** > **Garmin inReach**.
5. Paste your feed URL and password. Choose your team's color and set tracking points to appear inside the `OPX - Ground Tracks` folder.

---

## Practical Field Tips

- **Antenna Direction in Dense Woods**: In wet, heavy boreal forest or coastal rainforest, keep the inReach mounted high on your backpack shoulder strap facing straight up. Stashing the unit in an inside jacket pocket can delay satellite message delivery by 15–30 minutes.
- **Cold Weather Battery Life**: At temperatures below -20°C, lithium batteries drain much faster if set to 2-minute tracking intervals. Set routine search tracking intervals to **10 minutes** to ensure the battery lasts through multi-day tasks.
- **InReach as Radio Backup**: If a ground team drops behind a ridge and loses radio contact with base, sending a quick Preset 1 confirms team safety while planning relocates the comms relay.

---

## Thanks & Credits

This configuration standard was compiled from field-tested setups shared by Canadian Ground SAR teams and provincial search communications coordinators.
