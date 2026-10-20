---
name: sar-hub-authoring
description: >-
  Standardized guide and workflow for drafting, formatting, and publishing operational resources
  on the Canadian SAR Technology Hub. Use when creating or revising resource articles, integrating
  templates (CalTopo, GeoJSON, GPX, forms), enforcing plain-language tone (Grade 6–8), and ensuring
  consistent layout and site navigation.
---

# SAR Hub Resource Authoring Skill

This skill teaches agents and contributors how to take raw field knowledge, templates, SOPs, or vendor-neutral tools and publish them as clean, accessible, practitioner-focused resources for the **Canadian SAR Technology Hub**.

---

## 1. The Persona & The "Ground Searcher" Tone

All content on this hub must be written for the **Operational Practitioner**:
- **Target Reader**: Anyone from an 18-year-old student recruit to a 55-year-old retired teacher or tradesperson volunteering as Search Manager.
- **Tone**: Warm, clear, direct, and practical—like a well-written Canadian community newspaper or a Parks Canada field guide.
- **Reading Level**: Target **Grade 6–8**. Keep sentences short, active, and conversational.
- **The 02:00 Test**: If an exhausted search manager arriving at an Incident Command Post (ICP) at 2:00 AM cannot understand the instruction in 30 seconds, rewrite it.

### Words to Avoid vs. Words to Use

| ❌ Banned Corporate / Tech Jargon | ✅ Plain Field Replacement |
| :--- | :--- |
| "highest-leverage operational improvements" | "one of the easiest ways to keep your team organized" |
| "provisioning" / "deprovisioning" | "setting up", "creating", "removing" |
| "leverage" | "use", "rely on" |
| "interoperability" | "working smoothly together", "sharing data" |
| "tracking modality" | "GPS type", "tracking method" (phone, inReach, GPS) |
| "force multiplier" | "helpful tool", "huge time saver" |
| "streamline workflows" | "keep things simple", "save time" |
| "holistic paradigm" | "complete picture", "practical approach" |
| "situational awareness" *(overused)* | "so everyone sees the same picture" |

---

## 2. Standard Resource Page Anatomy

When authoring a resource under `docs/resources/<category>/<slug>.md`, follow this exact structural flow:

```markdown
---
title: "Clear, Actionable Title"
description: "A 1-2 sentence plain-English summary of what this tool does and who it helps."
category: "Mapping & GIS" # Options: Mapping & GIS, Communications, Search Management, Field Hardware, Training & Standards, Medical & Evacuation
jurisdiction:
  - "National" # Options: National, BC, AB, SK, MB, ON, QC, NB, NS, PE, NL, YT, NT, NU
tags:
  - "relevant-tag-1"
  - "relevant-tag-2"
maintainer: "Team Name or Contributor"
date_updated: YYYY-MM-DD
---

# Clear, Actionable Title

[1-2 paragraphs introducing what problem this solves in the field. Open with the real-world headache it prevents, why it matters, and who champion/tested it.]

---

## Download Operational Templates (If Applicable)

[Use Material cards for prominent download buttons. When offering templates, provide a Clean version ready for calls and a Guided version with help markers.]

<div class="grid cards" markdown>

-   :material-folder-check:{ .lg .middle } **Clean Template (Ready for a Call)**

    ---

    Contains empty folders and structure ready for live mission tasking.

    [:material-download: Download Clean Template (.geojson)](../../assets/files/geo/filename-clean.geojson){ .md-button .md-button--primary }

-   :material-help-circle-outline:{ .lg .middle } **Guided Template (With Notes & Markers)**

    ---

    Contains the same structure plus instructional markers explaining what goes where.

    [:material-download: Download Guided Template (.geojson)](../../assets/files/geo/filename-guided.geojson){ .md-button }

</div>

---

## How to Use This Resource

[Break procedures into sequential H3 headings (e.g., ### Method 1, ### Method 2). DO NOT use horizontal tabs (`=== "..."`) because long tab titles wrap or truncate on mobile screens and hide critical steps.]

### Method 1: [Recommended Workflow]

1. Numbered, step-by-step instructions.
2. Bold action verbs first.
3. Include external reference links where helpful.

---

### Method 2: [Alternative or Offline Workflow]

1. Step one.
2. Step two.

---

## Standard Reference Table / Data Dictionary

[When defining folders, radio channels, or equipment kits, use a clear Markdown table:]

| Category | Item Name | What Goes in Here | Helpful Tips & Field Rules |
| :--- | :--- | :--- | :--- |
| **Section** | `Item 1` | • Clear bullet points | Plain explanation of field rules |

---

## Practical Tips for the Field

[3-5 bulleted operational gotchas: cold weather limitations, preserving audit trails, shifting operational periods, offline caching before leaving cell coverage.]

---

## Thanks & Credits

[Acknowledge the volunteers, teams, and associations (e.g., BCSARA, OSARVA, SARVAC) who developed, tested, and shared the resource.]
```

---

## 3. Asset Management Rules

1. **Keep Assets Independent**:
   Always save downloadable files (.geojson, .gpx, .kml, .docx, .xlsx, .pdf) in `docs/assets/files/`:
   - `docs/assets/files/geo/` for spatial layers and map templates.
   - `docs/assets/files/forms/` for briefing sheets, ICS forms, and debrief templates.
   - `docs/assets/files/configs/` for radio profiles, app config files, and device backups.
2. **Never Embed Binary Blobs Directly**: Keep the file standalone so teams can download, update, or link to the asset file independently of the article.
3. **Format Clean JSON/GeoJSON**: Use 2-space indentation so version diffs are human-readable in git.

---

## 4. The 5-Step Publishing Checklist

Every time a new resource is added to the hub, execute all 5 steps:

- [ ] **Step 1: Save the asset files** into `docs/assets/files/<subfolder>/` using lowercase hyphenated names.
- [ ] **Step 2: Create the resource page** under `docs/resources/<category>/<resource-slug>.md` using the standard frontmatter and plain-language anatomy.
- [ ] **Step 3: Update the Category Directory Index** in `docs/resources/<category>/index.md` by adding a card linking to the new page.
- [ ] **Step 4: Update Site Navigation** in `mkdocs.yml` under `nav > Resources > <Category>`.
- [ ] **Step 5: Log in the Changelog** in `docs/whats-new.md` under the current month with a concise summary and link.
