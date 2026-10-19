---
title: "CalTopo (SARTopo) Incident Map Template and Folder Structure"
description: "A simple, field-tested folder structure and map template for Ground SAR teams using CalTopo, built from British Columbia SAR best practices."
category: "Mapping & GIS"
jurisdiction:
  - "National"
tags:
  - "caltopo"
  - "mapping"
  - "search-management"
  - "templates"
maintainer: "Bradley Parker (NB)"
date_updated: 2026-10-19
---

# CalTopo (SARTopo) Incident Map Template and Folder Structure

When a search call comes in, an incident map can get messy fast. Tracks from searchers start piling up, points get dropped without labels, and when another team arrives to help, nobody knows where to look. 

Setting up a clean folder structure before you start is one of the easiest ways to keep your search organized. It keeps clues easy to spot, makes sure safety hazards are never missed, and helps a fresh search manager step into the command post at 2:00 AM and understand the map in thirty seconds.

This guide shares a standard folder setup built and tested by **British Columbia Search and Rescue Association (BCSARA)** teams. It also lines up automatically with the folders created by **SAR Command Assist**.

---

## Download the Map Templates

You can download two ready-to-use template files in GeoJSON format:

<div class="grid cards" markdown>

-   :material-folder-check:{ .lg .middle } **Clean Template (Ready for a Call)**

    ---

    Contains all the standard folders and a first operational period (`OP1`). It is clean and empty, ready for a live search without needing to delete any notes or sample points.

    [:material-download: Download Clean Template (.geojson)](../../assets/files/geo/caltopo-sar-template-clean.geojson){ .md-button .md-button--primary }

-   :material-help-circle-outline:{ .lg .middle } **Guided Template (With Help Markers)**

    ---

    Contains the exact same folders, plus pink marker pins that explain what goes into each folder. Great for team training, new members, or practicing at the hall.

    [:material-download: Download Guided Template (.geojson)](../../assets/files/geo/caltopo-sar-template-guided.geojson){ .md-button }

</div>


---

## Three Ways to Use This Template

Choose the method that works best for your team's setup:

=== "Method 1: Copy from a Team Master Map (Best Practice)"

    If your team has a shared CalTopo account, this is the quickest method on a call:

    1. **Set up the master map once**: In your team's CalTopo account, start a new map and import either the clean or guided template file.
    2. **Name it clearly**: Name it something obvious, like `USE_ME_TEMPLATE` or `_TEMPLATE_DO_NOT_EDIT`.
    3. **Lock it down**: Set the map permission to **View Only** or **Locked** in your account settings so people don't accidentally edit the blank master during an active search. https://blog.caltopo.com/2024/09/18/new-feature-lockable-maps/
    4. Set your base layers, and other overlays (Such as Shared Locations so they are turned on by defauly when you copy the map) https://training.caltopo.com/all_users/base-layers/using-layers#default
    5. **Bookmark the link**: Save the link on the command trailer computer and in your team browser bookmarks.
    6. **When a callout happens**:
        - Open the `USE_ME_TEMPLATE` map.
        - Click **Export** on the left menu.
        - Under Format, pick **"Copy to new map"**.
        - Name the new map with your task number and location (for example: `Task 24-105 - Mount Douglas`) and you are ready to plan.

=== "Method 2: Import the File into a Blank Map"

    If you are using a personal CalTopo account or working on a fresh map offline:

    1. Open CalTopo and start a new, blank map.
    2. In the top-left menu, click **Import** > **Geospatial Data**.
    3. Select either `caltopo-sar-template-clean.geojson` or `caltopo-sar-template-guided.geojson` from your computer.
    4. Leave all the checkboxes checked and click **Import**.
    5. *(Optional)* If using the clean template, zoom to your search area and delete the temporary black box labeled **"Delete Me"**.

=== "Method 3: SAR Command Assist"

    If your team uses **SAR Command Assist**:

    - SAR Command Assist creates these exact same folders automatically when setting up a new incident map.
    - Because the folders match, maps created by hand and maps created through the software use the exact same layout.
    - You may still want to use a template map for base layers and overlays.

---

## Standard Folders & What Goes in Them

CalTopo lists folders in alphabetical order in the left menu. That is why the first two folders start with `01` and `02`: it forces your most important items (safety hazards, ICP, and the person's last location) to stay pinned at the very top where anyone can see them.

| Category | Folder Name | What Goes in Here | Helpful Tips & Field Rules |
| :--- | :--- | :--- | :--- |
| **Important Locations** | `01 Critical Points` | • LKP (Last Known Point) / IPP (Initial Planning Point)<br>• ICP (Command Post) location<br>• Staging areas and parking<br>• Helicopter landing zones (LZ) | Starts with `01` to stay at the top of your list. Use standard emergency symbols so anyone can recognize them. |
| | `01 Safety Issues` | • Known hazards in the search area<br>• Avalanche paths and cliff bands<br>• Swiftwater hazards or bad river crossings | **Keep this folder visible at all times**, especially when printing maps for field teams. Draw coloured shapes around dangerous areas. |
| **Local Knowledge & Clues** | `02 Points of Interest` | • Places the subject might walk toward (cabins, lookouts, lights)<br>• Water sources or shelters | Items or places that might attract the missing person. |
| | `02 Local Knowledge` | • Unmarked trails, old logging roads<br>• Notes from local landowners or hikers | Useful information gathered from family, witnesses, or locals who know the woods. |
| **Lost Person Behaviour** | `LPB - Profile Name` | • Distance rings drawn from the IPP<br>• Travel direction wedges | Rename this folder with who you are looking for (e.g. `LPB - Hiker` or `LPB - Child 1-3`). If you are comparing two profiles, make two folders. |
| **Clues** | `Clues - Active` | • Clues that searchers are currently checking<br>• Footprints, clothing, dropped gear | **Always write down the time, date, and who found the clue** in the marker description before sending another team out. |
| | `Clues - Discounted` | • Clues that turned out to belong to someone else | Move old or ruled-out clues here instead of deleting them. Keep this folder **hidden** so the map stays clean, but you keep a record. |
| **Tracks from Searchers** | `OPX - Ground Tracks` | • GPS tracks from ground search teams<br>• Live tracks sent from phones | Replace `X` with your operational period number (e.g. `OP1 - Ground Tracks`). Name each track with the assignment number and searcher callsign. |
| | `OPX - Air Tracks` | • Drone (RPAS) flight paths<br>• Helicopter and fixed-wing aircraft tracks | Keep air tracks in their own folder so they do not get mixed up with ground tracks. |
| | `OPX - Water Tracks` | • Boat, swiftwater, or kayak tracks | Keep boat tracks separate from shoreline ground searchers. |
| | `OPX - Marks` | • Temporary navigation points<br>• Markers dropped during the shift | General waypoints that do not fit into Clues or Safety. |
| | `OPX Travel Tracks` | • Tracks of teams driving to and from the search | When a team drives to their search area, move that driving track here. Keep this folder **hidden** so it does not clutter your search map. |
| **Team Assignments** | `Assignments` | • Search tasks that are planned and waiting | Put assignments here when planning. Group them by shift so you can hide old ones later. |
| | `In Progress Assignments` | • Tasks currently being searched | Move tasks here while teams are out in the bush if your command post tracks active tasks on the map. |
| | `Completed Assignments` | • Tasks that are finished and debriefed | Move finished tasks here once teams are back at base. Keep this folder hidden. |
| **Search Segments** | `Segmentation` | • Polygons dividing the search area into named zones | Search segment boundaries (e.g. `Segment 1`, `Segment 2`). |
| **Special Maps** | `Custom Maps` | • Custom trail maps or drone survey photos | A place for special map overlays or custom aerial photos. |

---

## Practical Tips for Keeping Maps Clean

### 1. Never Change the Master Template During a Search
Never do your live planning on the blank master template map. Always make a copy using **Export > "Copy to new map"**, or import the GeoJSON into a fresh map. If your team shares an account, lock the master map so only your mapping officer can edit it.

### 2. Move Old Clues, Never Delete Them
If a searcher finds a candy wrapper that turns out to be years old, **do not delete it from the map**. Move it into `Clues - Discounted` and turn off the folder's eyeball icon. Keeping ruled-out clues in a hidden folder keeps your active map clean while protecting the record for the police or coroner later.

### 3. Starting Day 2 (Moving to a New Shift)
When the first shift ends and a new operational period begins:
1. Turn off or lock the `OP1` folders.
2. Make new folders for the next shift (e.g. `OP2 - Ground Tracks`, `OP2 - Air Tracks`).
3. Move finished tasks into `Completed Assignments`.

### 4. Keep Safety Hazards Visible
Make sure the eye icon on `01 Safety Issues` stays turned on. When you print paper maps or send PDF task sheets to field searchers, red hazard boxes and notes should always be clearly visible.

### 5. Download Maps to Phones Before Leaving Base
Before teams leave the command post and lose cell service:
- Remind searchers to open the CalTopo app on their phones and download the offline map layer for the search area.
- Make sure they know how to record their track so it syncs back when they return to base.

---

## Thanks & Credits

This folder structure was created, tested, and shared by volunteer searchers across the **British Columbia Search and Rescue Association (BCSARA)**. Their willingness to share field-tested tools makes searches safer and better organized for teams all across Canada.
