---
title: "SAR Command Assist — ICS Paperwork Made Faster"
description: "A free Windows app that automates ICS forms and team assignments for SAR incident command teams, cutting paperwork time from hours to minutes during a live task."
category: "Search Management"
jurisdiction:
  - "National"
tags:
  - "ics-forms"
  - "incident-command"
  - "iap"
  - "team-assignments"
  - "windows"
  - "free"
  - "bcsara"
maintainer: "Dylan Baker, Campbell River SAR / BCSARA"
date_updated: 2026-10-20
---

# SAR Command Assist — ICS Paperwork Made Faster

If you've ever spent the midnight hours before an operational period re-typing the same task number, subject name, and safety plan into a dozen separate ICS forms, SAR Command Assist was built for you.

SAR Command Assist (also called **SAR Assist** or **ICA**) is a free Windows application developed by Dylan Baker of Campbell River Search and Rescue and now maintained under [BCSARA](https://www.bcsara.com). Its core idea is simple: **type something once, and the app puts it everywhere it's needed.** Enter your subject's name once, and it flows into the SMEAC briefing, the assignment forms, the ops plan, and the IAP automatically. Teams using the app regularly produce a full set of assignments for 20+ teams in under 30 minutes — paperwork that used to take all night.

The app has been used on large-scale responses across British Columbia, and it's completely free with no catch.

---

## Works Offline — No Internet Required

SAR Command Assist is designed to work fully offline, which matters a great deal in remote Canadian operations. All task data lives on your ICP laptop. Nothing is automatically sent anywhere.

**For teams working in a command post with multiple computers**, the app has a built-in local area network (LAN) sync mode that lets two or more laptops share the same live task over your CP's Wi-Fi or a simple router — no internet connection needed. Your Plans Section on one machine and your IC on another can both see assignments, communications logs, and IAP updates as they happen.

Internet Sync (described below) is a separate, optional feature you can turn on if you have connectivity and want to reach someone off-site.

---

## What's Included

SAR Command Assist handles the full ICS paperwork stack for a ground SAR task:

| Form | What It Does |
| :--- | :--- |
| **ICS 202** | Incident Objectives |
| **ICS 204** | Team Assignment & Debrief |
| **ICS 204C** | Clue Report |
| **ICS 205 / 205A** | Communications Plan and List |
| **ICS 206** | Medical Plan |
| **ICS 207** | Organization Chart |
| **ICS 211** | Check-In List |
| **ICS 213** | General Message |
| **ICS 214** | Unit Log |
| **ICS 215** | Operations Plan |
| **ICS 220** | Air Operations Summary |
| **ICS 301** | Subject Profile |
| **ICS 303** | Equipment Inventory |
| **ICS 305** | Safety Plan |
| **ICS 307** | Transport Plan |
| **ICS 309** | Radio Log |
| **SMEAC Briefing** | Full SMEAC-format team briefing sheet |

You can print individual forms, or package everything into a single PDF Incident Action Plan (IAP) for distribution or archiving.

---

## How to Get Started

### Step 1: Download and Install

1. Go to [sarassist.ca/Download](https://www.sarassist.ca/Download) and download the installer.
2. Run the installer on a Windows machine. The app is free, with no licence key or account required.
3. Launch **SAR Command Assist** from the Start menu.

> **Tip:** Install it on a dedicated laptop for your ICP. You can also install it on multiple machines — the licence allows unlimited installations.

Before your first callout, the SAR Assist team provides a set of downloadable quick-reference guides and a step-by-step walkthrough for initial setup. See the [Reference Documents](https://www.sarassist.ca/Support/Reference) page for the **Initial Setup** guide and the **Starting a New Task** walkthrough.

---

### Step 2: Enter Your Subject Profile

1. Open the **Subject Profile (ICS 301)** tab.
2. Fill in name, description, last known point (LKP), and relevant subject category (e.g., Hiker, Overdue Hunter, Despondent Person).
3. The subject's details will automatically carry into your SMEAC briefing and team assignment forms — no re-typing needed.

---

### Step 3: Generate Reflex Tasks

Based on the subject profile you set, the app can suggest and create a standard set of "reflex" tasks — common first assignments for that subject type.

1. Open the **Team Assignments** section.
2. Click **Reflex Tasking** to see suggested assignments for your subject category.
3. Select the tasks you want to create. The app populates the task descriptions from your preset library.
4. Adjust task boundaries, objectives, or safety notes as needed before printing.

You can build your own preset library of assignments and safety plans to match your team's local area and typical callout types.

---

### Step 4: Build Your IAP

1. Complete the remaining forms (Communications Plan, Medical Plan, Org Chart) as needed.
2. Click **Print** or **Save as PDF** to produce a complete Incident Action Plan package.
3. Share the PDF by email, USB drive, or distribute it live across your CP network using LAN Sync.

The [Printing Your Incident](https://www.sarassist.ca/downloads/SupportDocs/Printing%20your%20Incident.pdf) quick-reference guide walks through your options for producing and packaging the final IAP.

---

## Sharing Work in the Command Post (LAN Sync)

When you have two or more computers at your ICP, you don't need the internet to share a live task. SAR Command Assist's built-in **local network (LAN) sync** lets multiple machines on the same Wi-Fi or router work on the same task simultaneously.

This is useful when:
- Your Plans Chief is building assignments on one laptop while your IC reviews comms logs on another.
- You want a dedicated computer logging communications while a second machine handles IAP printing.
- You're running a complex task where splitting the work between two or three people at the same table makes a real difference at 03:00.

All data stays on your local network. Nothing leaves your CP.

---

## Collaborating Remotely (Internet Sync)

If your team has an internet connection and needs to bring in help from off-site, the optional **Internet Sync** feature lets two or more computers share the live task securely over the internet.

This is useful when:
- A Plans Chief or Search Manager is working remotely and needs to review or edit assignments.
- You want a second pair of eyes on the IAP from someone who can't travel to the ICP.
- You're running a multi-day task and want your home base to help prep the next operational period while your ICP team grabs some sleep.

### Privacy and Security

Task data handled through Internet Sync is protected by **256-bit end-to-end encryption**. Your data is encrypted on your own computer before it's ever sent anywhere. Even the server and the developer cannot read it.

Key points:
- **The server is in Canada.** Task data is stored on a Canadian server, not an offshore cloud provider.
- **The server is blind to your data.** Only computers holding the correct encryption key can read the task information. The server stores only encrypted blobs — it has no way to see who your subject is, what assignments you've created, or any other operational details.
- **Access is controlled by a randomly generated key.** When you start an Internet Sync, the app generates a unique encryption key. Only people you personally share that key with can join the task.
- **Internet sync is not backup.** It is intented for short term syncronizatin between devices. Your long-term file storage of inactive incidents needs to be handled elsewhere.

For full technical details, see the [Internet Sync page](https://www.sarassist.ca/Support/InternetSync) on the SAR Assist website. A long-form setup guide is also available at [Reference Documents > Start a new task with Internet Sync](https://www.sarassist.ca/downloads/SupportDocs/Start%20an%20Internet%20Sync%20task%20in%20SAR%20Command%20Assist%20%281%29.pdf).

---

## Member Sign-In and Status Tracking

### Tracking Who's In the Field

Once members are signed into the task, the app tracks:
- Which team each member is assigned to.
- Each team's current status (in the field, en route back, waiting at base).
- A colour-coded warning when a team misses a scheduled check-in.
- A reminder to call the Emergency Coordination Centre (ECC) when your check-in interval is up.

All communications can be logged (radio, inReach, cell, etc.) and exported to a standard **ICS 309 Radio Log**. The [Communications Log](https://www.sarassist.ca/downloads/SupportDocs/Communications%20Log.pdf) quick-reference guide covers the logging workflow.

### My SAR Assist (Mobile Companion App)

The **My SAR Assist** mobile app (Android and iOS, also free) pairs with SAR Command Assist at the ICP.

Members enter their personal details once in the app, which generates a personal QR code. At sign-in, they scan their phone at the ICP barcode reader, and their name, team, emergency contact, and qualifications are automatically added to the task — no paper forms, no re-typing names.

This is especially helpful on **mutual aid tasks**, where the command team may not know the incoming members. The QR scan instantly tells you how many trackers, managers, or swift-water technicians you have on hand.

- [Download My SAR Assist (iOS and Android)](https://www.sarassist.ca/Download)
- [Barcode Check-In quick-reference guide](https://www.sarassist.ca/downloads/SupportDocs/Barcode%20Check-In.pdf)
- [Learn more about barcode sign-in](https://www.sarassist.ca/MySarAssist#How)

---

## D4H Integration

If your team uses [D4H](https://d4h.com) for member records, you can import your member list directly into SAR Command Assist. This means you don't have to manually add members during a task — search for a name, select them, and they're added to an assignment or ICS role in seconds.

See the [D4H Sync guide](https://www.sarassist.ca/Support/D4HSync) for setup instructions.

---

## Practical Tips for the Field

- **Set up your preset library before the season starts.** Load in your common safety plans, operational area descriptions, and reflex task sets when there's no pressure. You'll save significant time on your next callout.
- **Keep a backup option ready.** The SAR Assist website includes a clear disclaimer: the app is provided as-is. Have blank paper ICS forms and a printer fallback ready, especially for your first few tasks while your team is getting familiar with it. SAR Assist makes it easy to print everything in standardized formats and hand off a complete paper package to the next OP if you transition at an ICP.
- **Use LAN Sync at the ICP first, Internet Sync only if you need off-site help.** For most tasks, keeping data on your local network is simpler and more reliable than depending on cellular or satellite connectivity.
- **Guard your Internet Sync key.** The encryption key is your only protection. Don't share it in a group chat. Share it directly with the specific people who need access.
- **Sign in members as they arrive, not in a batch at the end.** The communications log and team status features work best when check-ins are logged throughout the task, not reconstructed afterwards.

---

## Training and Support

SAR Assist has a full set of training materials. This page is just an introduction — head to the official resources for the full picture:

<div class="grid cards" markdown>

-   :material-school:{ .lg .middle } **Online Training**

    ---

    Free self-paced courses covering the full SAR Assist workflow, from initial setup through to closing a task.

    [:material-arrow-right: training.sarassist.ca](https://training.sarassist.ca/){ .md-button .md-button--primary }

-   :material-file-document-multiple:{ .lg .middle } **Quick-Reference Guides**

    ---

    Printable PDF guides covering Initial Setup, Starting a New Task, Creating Assignments, Communications Logging, Printing, Barcode Check-In, and more.

    [:material-arrow-right: Reference Documents](https://www.sarassist.ca/Support/Reference){ .md-button }

-   :material-play-circle:{ .lg .middle } **Tutorial Videos**

    ---

    Short walkthrough videos for each major feature in the app.

    [:material-arrow-right: Video Tutorials](https://www.sarassist.ca/Support/Videos){ .md-button }

-   :material-help-circle:{ .lg .middle } **FAQ & Support**

    ---

    Common setup and usage questions, plus a support ticket system for bug reports.

    [:material-arrow-right: FAQ](https://www.sarassist.ca/Support/FAQs){ .md-button }

</div>

You can also connect with other users and the development team on the [SAR Assist Discord](https://discord.gg/aRpjFh45WG).

---

## Thanks & Credits

SAR Command Assist was created by **Dylan Baker**, a SAR manager with **Campbell River Search and Rescue**, after experiencing first-hand the paperwork burden on a multi-day, 100+ searcher response. The app has been adopted by teams across British Columbia and beyond.

It is currently maintained under the **[British Columbia Search and Rescue Association (BCSARA)](https://www.bcsara.com)**.

If you find this tool useful in your operations, consider letting Dylan know — and if you have ideas for new features or preset libraries for your region, the [Discord community](https://discord.gg/aRpjFh45WG) is the best place to share them.
