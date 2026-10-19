---
title: Resource Page Template
description: Standard Markdown and YAML frontmatter template for adding a new resource to the hub.
---

# Resource Page Template

Copy and paste the template block below when creating a new `.md` file under `docs/resources/<category>/`.

```markdown
---
title: "Name of Tool, Template, or Procedure"
description: "A one or two sentence summary of what this resource does and who it helps."
category: "Mapping & GIS" # Options: Mapping & GIS, Communications, Search Management, Field Hardware, Training & Standards, Medical & Evacuation
jurisdiction:
  - "National" # Options: National, BC, AB, SK, MB, ON, QC, NB, NS, PE, NL, YT, NT, NU
tags:
  - "mapping"
  - "field-ops"
  - "caltopo"
maintainer: "Your Name or @GitHubUsername"
date_updated: 2026-10-13
---

# Name of Tool, Template, or Procedure

<!-- A brief introductory paragraph explaining what this is and its primary use case in Canadian SAR operations. -->

## Key Features & Overview
- Bullet point summarizing what it does
- Another key feature or capability
- Equipment or software required to use it

## Downloads & Attachments (Optional)
<!-- If you have attached files under docs/assets/files/, link them here: -->
- [Download GeoJSON Boundary Layer](../../assets/files/geo/example.geojson){ .md-button }
- [Download Briefing Sheet (.docx)](../../assets/files/forms/example.docx){ .md-button }

## Setup & How to Use
1. Step one on how to deploy or use this resource.
2. Step two with any helpful operational tips.
3. Common mistakes or field gotchas to avoid.

## Related Resources & External Links
- [Official Documentation or Website](https://example.com)
- [Associated Standard or SAR Manual](https://example.com)
```
