---
title: "SAR Duty — D4H Administration Tool"
description: "A free, open-source web app that sits on top of D4H to automate tax credit letters, digital ID cards, door attendance, and mileage tracking for Canadian SAR team administrators."
category: "Team Administration"
jurisdiction:
  - "National"
tags:
  - "d4h"
  - "administration"
  - "id-cards"
  - "open-source"
maintainer: "Canadian SAR Technology Hub"
date_updated: 2026-10-19
---

# SAR Duty — D4H Administration Tool

If your team uses [D4H](https://d4h.com/) to track members and incidents, you already know it is good at what it does. But there are some jobs D4H does not do — and those jobs tend to land on one or two volunteers who spend hours each year filling in the gaps by hand.

**SAR Duty** is a free and open source web tool built by a BC SAR volunteer to handle exactly those tasks. It reads your team's D4H data and automates the paperwork around it — things like generating tax credit letters, issuing digital ID cards, and recording door attendance. Anyone with **Owner or Editor access in D4H** can sign their team up and start using it.

SAR Duty has been used by teams for several years, most notably for issuing tax credit letters (see the SRVTC below) and calculating member mileage for reimbursement. Active development picked up significantly in Fall 2026, and early feedback from teams has been very positive.

!!! note "Who This Is For"
    SAR Duty is most useful for the people managing your team's D4H account — typically the team admin, training officer, or operations coordinator. If you have **Editor or Owner access** in D4H and find yourself doing a lot of repetitive paperwork, this tool is worth a look.

---

## What SAR Duty Does

### Tax Credit Letters (SRVTC)

The [Search and Rescue Volunteer Tax Credit (SRVTC)](https://www.canada.ca/en/revenue-agency/services/tax/individuals/topics/about-your-tax-return/tax-return/completing-a-tax-return/deductions-credits-expenses/line-31220-volunteer-firefighters-amount-line-31240-search-rescue-volunteers-amount.html) lets eligible SAR volunteers claim a federal tax credit if they complete 200 or more hours of qualifying service in a year. Tracking those hours and producing a signed letter for each qualifying member is a manual job — or it was.

SAR Duty reads each member's attendance from D4H, calculates their hours, generates a tax credit letter, and emails it to them directly. Letters can be verified online at [verify.sarduty.com/letters](https://verify.sarduty.com/letters), which gives the CRA a simple way to confirm the hours are real.

### Member ID Cards

SAR Duty can issue a digital ID card to each member, stored in their Apple Wallet or Google Wallet. The card includes a QR code that anyone — an RCMP officer, Parks Canada warden, or property owner — can scan to verify the member's SAR affiliation. No printing required, and cards are always current.

### Door Attendance

Using a phone, an admin can record who arrives and leaves a training night or mission debrief at the door — then push that attendance directly into D4H. This removes the paper sign-in sheet and the manual entry step that follows it.

### Mileage Tracking

SAR Duty helps calculate member mileage for reimbursement, pulling from the same D4H activity data your team already maintains.

!!! tip "Still Growing"
    SAR Duty is under active development. New features are being added regularly. Check [sarduty.com](https://sarduty.com) for what is current — this page covers the core capabilities but may not reflect the latest additions.

---

## Getting Started

SAR Duty connects to D4H using a D4H access key. You need **Owner or Editor access** to your team in D4H to sign up.

1. Go to [sarduty.com](https://sarduty.com) and click **Sign up a team**.
2. Enter your D4H access key when prompted.
3. SAR Duty will pull your team's data from D4H and you can begin using the features.

That's it. There is no software to install, and members do not need to create accounts — their D4H records are the source.

---

## Cost & Hosting

The hosted version at [sarduty.com](https://sarduty.com) is currently available **at no cost**. It is run by Gerry, a BC SAR volunteer who built the tool for the SAR community and is offering it free of charge.

Because this is a one-person volunteer effort, that may change over time. If cost or continuity is a concern for your team, SAR Duty is **fully open source**:

> **Source code:** [github.com/gshaw/sarduty](https://github.com/gshaw/sarduty)

Any team or organization with technical capacity can run their own instance. This makes SAR Duty a sustainable option even if the hosted version changes in the future.

---

## Practical Notes

- **D4H access is required.** SAR Duty is not a standalone tool — your team must already be using D4H for member and activity tracking.
- **Editor or Owner access needed.** Basic D4H member accounts cannot sign up a team. You need Editor or Owner permissions.
- **Tax letters depend on accurate D4H data.** If attendance records in D4H are incomplete or missing, the hours calculation will reflect that. Make sure your D4H data is clean before generating letters each year.
- **SRVTC eligibility is set by the CRA.** SAR Duty automates the letter-writing, but your team's management remains responsible for confirming which members meet the 200-hour threshold and qualify under the program rules.
- **Internet connection required.** SAR Duty is a web app — it is not designed for use in areas without connectivity.

---

## Thanks & Credits

SAR Duty was built and is maintained by **Gerry Shaw**, a BC SAR volunteer. The tool grew out of the real administrative burden SAR teams face each year and reflects genuine field experience with D4H and the SRVTC program. The project is open source and welcomes contributions from the SAR community.

- Website: [sarduty.com](https://sarduty.com)
- Source code: [github.com/gshaw/sarduty](https://github.com/gshaw/sarduty)
- Letter verification: [verify.sarduty.com/letters](https://verify.sarduty.com/letters)
