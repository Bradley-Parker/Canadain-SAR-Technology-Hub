# AGENTS.md — Canadian SAR Technology Hub Guidelines

This document establishes the operational principles, editorial philosophy, tone, and technical architecture for anyone (human or AI) contributing to or maintaining the **Canadian SAR Technology Hub**.

---

## 1. Mission & Audience

The **Canadian SAR Technology Hub** is a practitioner-led, community-maintained knowledge directory for Canadian Ground Search and Rescue (GSAR). Its mission is to connect searchers, incident commanders, and tech specialists with field-tested tools, procedures, and templates that make missions safer and more effective.

### Primary Personas

1. **The Operational Practitioner (Read-First Focus)**
   - *Who they are*: Ground searchers, team leaders, search managers, and equipment officers looking for reliable solutions, field templates, or technical guidance.
   - *What they need*: Direct, actionable answers, candid evaluations, downloadable operational assets (GPX, GeoJSON, forms), and clear instructions.
   - *Design mandate*: **Never confront this user with site mechanics, web development jargon, or git workflows.** The site should read like an operational field resource, not a software repository.

2. **The Community Contributor**
   - *Who they are*: Dedicated SAR volunteers who have developed a great tool, workflow, or template and want to share it.
   - *What they need*: A warm, low-friction, non-intimidating way to share content without requiring software engineering skills.

---

## 2. Core Values & Editorial Standards

### 🛡️ Field-Proven Experience Over Vendor Pitches
Every resource, hardware review, and workflow featured here must reflect the **real-world experience of SAR professionals and ground teams** who have deployed and tested it in operational or rigorous training environments.

- **No Sales Pipeline / No Sponsored Posts**: This hub is strictly non-commercial. There are no sponsored posts, paid endorsements, or marketing copy. 
- **Affiliate Links**:
Affiliate links are permitted when clearly disclosed. Any proceeds must benefit the contributor's SAR team, SAR organization, or another community-serving initiative. Affiliate links must not intentionally provide a worse price or experience than a standard purchase link. Resource listings and recommendations must remain unbiased regardless of affiliate relationships.

Example: 
Website:
https://example.com/product

Affiliate Link (Benefits York Sunbury Ground Search & Rescue):
https://affiliate.example.com/product
- **Balanced Perspective on Commercial Tools**: Ground SAR teams regularly rely on paid and proprietary tools (e.g., CalTopo, Garmin inReach, Starlink, FLIR sensors, specialized RPAS platforms). These are fully welcomed and encouraged — **provided they are evaluated from the practitioner's perspective**. 
- **The "Tested in the Field" Standard**: We do not publish speculative vendor press releases or promote unverified claims. A product or procedure must have genuine operational utility demonstrated by active SAR personnel.
- **Honest Assessments**: Reviews and guides should openly note limitations, battery life in -25°C conditions, canopy penetration issues, licensing costs, and training overhead alongside the benefits.

### 🇨🇦 Canadian Ground SAR Context
Content should respect the operational realities of Canadian search and rescue:
- **Jurisdictional Diversity**: Acknowledge provincial standards and associations (e.g., BCSARA / EMCR, OSARVA, SARVAC, SARNCO, FQSA) and partner agencies (RCMP, OPP, Sûreté du Québec, Parks Canada, CAF / JRCC).
- **Environmental Realities**: Canadian terrain ranges from coastal temperate rainforest to prairie bluffs, dense boreal forest, muskeg, mountainous alpine, and Arctic tundra. Tools must be evaluated in context of extreme weather, sub-zero cold, and remote operations where cellular and grid infrastructure do not exist.

---

## 3. Voice, Tone & Writing Style

### 📰 Plain Language & Readability Standard (The "Ground Searcher" Rule)
Content must be accessible, warm, and practical for Canadians of all backgrounds, ages, and education levels—from an 18-year-old student recruit to a 60-year-old retired teacher serving as Search Manager. Write like a clear Canadian community newspaper or a government document for citizens, **never like a tech startup pitch, corporate board room, or academic paper**.

- **Plain Everyday English (Target Grade 6–8 Reading Level)**:
  - Keep sentences short and direct.
  - Choose simple, familiar words over complex ones (e.g., use *set up* instead of *provision*, *use* instead of *leverage*, *work together* instead of *interoperability*, *method* instead of *modality*).
  - Use active voice: *"Search managers can copy this template"* instead of *"This template can be leveraged by incident management personnel"*.
- **Strictly Ban Corporate, Consultant & Tech Buzzwords**:
  - Never use phrases like *"highest-leverage operational improvements"*, *"streamline workflows"*, *"holistic paradigms"*, *"force multiplier"*, or *"optimize operational synergies"*.
  - If a sentence sounds like it belongs in a business pitch deck or a software press release, strip it down to plain field talk.
- **Operational & Pragmatic**: Use common Canadian SAR terms naturally (*LKP*, *IPP*, *POA*, *POD*, *Hasty Search*, *ICP*, *Tasking*), but explain them briefly on first mention so newer volunteers are never left behind.
- **Objective & Tested**: Give honest, practical advice based on real deployments. Focus on what works, what breaks in the cold, and how to keep things simple when people are tired at 03:00.

---

## 4. Technical Architecture & Clean Separation

To protect the read-first user persona from technical clutter, maintain a strict separation between **Operational Content** and **Platform Mechanics**:

### Content Hierarchy
- `docs/resources/<category>/`: Pure operational guides, tool overviews, and field reviews. **Zero discussion of Git, Markdown compilation, or repository infrastructure.**
- `docs/whats-new.md`: Reverse-chronological dated log capturing major operational resource additions and revisions, with direct links to the articles and git diffs.
- `docs/downloads/`: Straightforward download directory for non-text operational files (.gpx, .geojson, .docx, .xlsx, .pdf).
- `docs/contributing/`: Dedicated home for all contributor guidance:
  - `docs/contributing/index.md`: Friendly overview on how to suggest edits or submit tools.
  - `docs/contributing/editorial-standards.md`: The field-proven, vendor-neutral ethos.
  - `docs/contributing/technical-guide.md`: Deeper technical details (how GitHub Pages, MkDocs, frontmatter, and GitHub Actions work) kept cleanly tucked inside.
  - `docs/contributing/template.md`: Frontmatter and markdown template for new entries.
  - `docs/contributing/taxonomy.md`: Accepted categories, tags, and province codes.

### 📰 "What's New" & Changelog Protocol
To keep search managers and practitioners up-to-date with field-proven developments:
- **Location**: All updates are maintained in `docs/whats-new.md` in reverse chronological order.
- **Inclusion Criteria**: Record only **major operational changes**:
  - New resource pages or newly added downloadable operational files (GPX, GeoJSON, checklists).
  - Substantial revisions to existing guides (e.g., revised radio plans, updated safety warnings, updated battery benchmarks).
  - *Do NOT record*: Minor typo fixes, style adjustments, dependency updates, or site infrastructure tweaks.
- **Entry Structure**:
  - Date header (e.g., `### YYYY-MM-DD` or monthly group).
  - Quick 1-2 sentence operational summary describing what changed and why it matters in the field.
  - Direct link to the updated article: `[:material-arrow-right-circle: Resource Name](path/to/resource.md)`.
  - Link to git commit or PR diff: `[:octicons-git-compare-16: View Commit / Diff](https://github.com/Bradley-Parker/Canadain-SAR-Technology-Hub/commit/<sha>)` or `[:octicons-git-pull-request-16: PR #X](https://github.com/Bradley-Parker/Canadain-SAR-Technology-Hub/pull/X)`.
- **Frontmatter Maintenance**: Whenever an existing resource is updated, always bump its `date_updated: YYYY-MM-DD` frontmatter field.

### Frontmatter Standard
Every resource document under `docs/resources/` must start with clean YAML frontmatter:
```yaml
---
title: "Clear, Descriptive Resource Name"
description: "A 1-2 sentence operational summary for cards and search indexes."
category: "Category Name"
jurisdiction:
  - "National" # or specific provinces: BC, AB, ON, etc.
tags:
  - "relevant-tag"
maintainer: "Practitioner Name or Team"
date_updated: YYYY-MM-DD
---
```

### Binary Blobs & Assets
- Store images in `docs/assets/images/`.
- Store downloadable operational files in `docs/assets/files/` (`geo/`, `forms/`, `configs/`).
- Do not check build artifacts or auto-generated directories (`site/`, `.cache/`, `venv/`) into git.

---

## 5. Environment & Tooling Guidelines (for AI Agents & Automation)

When running terminal commands, builds, or scripts in this repository:
- **Python Virtual Environment (`.venv`)**:
  - Always use the workspace's local virtual environment located at `.venv\`.
  - For Python commands, explicitly invoke `.\.venv\Scripts\python.exe` or activate via `.\.venv\Scripts\Activate.ps1`.
  - For MkDocs and other CLI utilities installed in the venv, invoke `.\.venv\Scripts\mkdocs.exe` or run via `.\.venv\Scripts\python.exe -m mkdocs <command>`.
  - Do not rely on global or system-wide Python or CLI tools, as project dependencies (`mkdocs-material`, plugins) are isolated in `.venv\`.
