---
title: Resource Page Template
description: Standard Markdown and YAML frontmatter template for adding a new resource to the hub.
---

# Resource Page Template

Copy and paste the template block below when creating a new `.md` file under `docs/resources/<category>/`. 

!!! tip "Using AI Agents (Antigravity & Others)"
    If you are using Antigravity or an agent tool, this repository includes the **`sar-hub-authoring`** skill located at `.agents/skills/sar-hub-authoring/SKILL.md`. Simply ask the agent to *"use the sar-hub-authoring skill to draft this guide"* and it will automatically apply the layout, plain language tone, and publication checklist.

```markdown
---
title: "Name of Tool, Template, or Procedure"
description: "A one or two sentence plain-English summary of what this resource does and who it helps."
category: "Mapping & GIS" # Options: Mapping & GIS, Communications, Search Management, Field Hardware, Training & Standards, Medical & Evacuation
jurisdiction:
  - "National" # Options: National, BC, AB, SK, MB, ON, QC, NB, NS, PE, NL, YT, NT, NU
tags:
  - "relevant-tag"
maintainer: "Your Name or @GitHubUsername"
date_updated: YYYY-MM-DD
---

# Name of Tool, Template, or Procedure

<!-- Open with 1-2 paragraphs in plain everyday English (target Grade 6–8). Explain the real-world operational problem this solves and why it matters at 2:00 AM in the command trailer. -->

---

## Download Operational Templates (Optional)

<!-- Use Material cards for prominent downloads. If providing templates, offer a Clean version and a Guided version when helpful. -->

<div class="grid cards" markdown>

-   :material-folder-check:{ .lg .middle } **Clean Template (Ready for a Call)**

    ---

    Contains empty folders and structure ready for live mission tasking.

    [:material-download: Download Clean Template (.geojson)](../../assets/files/geo/example-clean.geojson){ .md-button .md-button--primary }

-   :material-help-circle-outline:{ .lg .middle } **Guided Template (With Notes & Markers)**

    ---

    Contains the same structure plus instructional markers explaining what goes where.

    [:material-download: Download Guided Template (.geojson)](../../assets/files/geo/example-guided.geojson){ .md-button }

</div>

---

## How to Use This Resource

<!-- Break workflows into sequential H3 headings. Avoid horizontal tabs so steps are not cut off on mobile devices. -->

### Method 1: [Recommended Workflow]

1. Numbered, step-by-step instructions.
2. Bold action verbs first.
3. Include external links to official tools or manuals.

---

### Method 2: [Alternative or Offline Workflow]

1. Step one.
2. Step two.

---

## Practical Tips for the Field

- **Cold Weather Performance**: How it behaves in -20°C conditions.
- **Keeping Maps & Data Clean**: Moving old items instead of deleting to preserve coroner/police audit trails.
- **Before Leaving Cell Coverage**: Offline mobile app syncing steps.

---

## Thanks & Credits

Developed and tested by [SAR Team or Contributor Name].
```
