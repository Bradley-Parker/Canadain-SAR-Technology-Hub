---
title: Technical Architecture & Site Mechanics
description: Technical details for maintaining the static site generator, frontmatter schemas, asset pipelines, and automated builds.
---

# Technical Architecture & Site Mechanics

This document outlines the technical underpinnings of the Canadian SAR Technology Hub for maintainers, developers, and technically-minded contributors.

---

## 1. Architectural Philosophy

The technical design prioritizes **extreme portability, zero hosting cost, and zero server maintenance**:

- **100% Static**: Built with [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/). Compiles pure Markdown into static HTML, CSS, and client-side JavaScript.
- **Client-Side Search**: Search indexing occurs at build time via MkDocs. Full-text search and tag filtering run entirely in the visitor's browser without external databases or cloud search APIs.
- **Zero Proprietary Formats**: All textual content is stored as human-readable Markdown with standard YAML frontmatter. If the site generator ever changes, the underlying content remains fully portable and readable.
- **GitHub Pages Hosting**: Automated builds and deployments run on GitHub Actions whenever changes are merged into `main`.

---

## 2. Directory Layout

```text
├── .github/
│   ├── ISSUE_TEMPLATE/        # Issue forms for web-based submissions
│   └── workflows/
│       ├── deploy.yml         # CI/CD deployment to GitHub Pages
│       └── validate-pr.yml    # Build validation and link checking for PRs
├── docs/                      # Pure Markdown content
│   ├── index.md               # Site homepage
│   ├── whats-new.md           # Reverse-chronological changelog & updates
│   ├── tags.md                # Generated tag index
│   ├── downloads/             # Attachment library guide
│   ├── contributing/          # Community, editorial, and technical guides
│   ├── resources/             # Operational resources grouped by domain
│   └── assets/                # Images and binary blobs
│       ├── images/            # Screenshots and illustrations
│       └── files/             # Downloadable .gpx, .geojson, .docx, .xlsx, .pdf
├── mkdocs.yml                 # Navigation, theme, and plugin configuration
└── requirements.txt           # Python dependencies for the build environment
```

---

## 3. Frontmatter Specification

Every resource file under `docs/resources/` should include YAML frontmatter at the top:

```yaml
---
title: "Resource Name"
description: "A 1-2 sentence summary displayed on search results and category overviews."
category: "Mapping & GIS" # Match primary navigation categories
jurisdiction:
  - "National"            # Or provincial codes: BC, AB, SK, MB, ON, QC, NB, NS, PE, NL, YT, NT, NU
tags:
  - "caltopo"
  - "mapping"
maintainer: "Name or Team"
date_updated: YYYY-MM-DD
---
```

---

## 4. Binary Blobs & File Attachments

The Canadian SAR Technology Hub stores supporting non-text operational assets directly within the git repository under `docs/assets/files/`.

Any file committed here is automatically packaged by GitHub Actions and hosted statically on GitHub Pages, allowing files to be downloaded or imported directly into search and rescue software without external cloud storage dependencies.

### Directory Layout & Supported Formats

Non-markdown attachments are organized by domain under `docs/assets/files/`:

- **Geospatial Layers (`docs/assets/files/geo/`)**:
  - *Formats*: `.geojson`, `.gpx`, `.kml`, `.kmz`
  - *Target Applications*: CalTopo / SARTopo, Garmin BaseCamp, handheld GPS units, QGIS, Avenza Maps.
- **Operational Forms & Templates (`docs/assets/files/forms/`)**:
  - *Formats*: `.pdf`, `.docx`, `.xlsx`
  - *Target Applications*: Incident briefings, debrief sheets, search logs, medical packaging forms, ICS templates.
- **Device Configurations & Codeplugs (`docs/assets/files/configs/`)**:
  - *Formats*: `.json`, `.xml`, `.dat`, `.csv`
  - *Target Applications*: Radio channel codeplugs, GPS profile configs, software display layouts.

### How to Add & Link Files

1. **Place your file** in the appropriate subdirectory under `docs/assets/files/` using concise, hyphenated, lowercase names (e.g., `caltopo-standard-grid.geojson`).
2. **Link to the file** in your Markdown resource page using Material for MkDocs button syntax:

```markdown
<!-- Standard Download Button -->
[Download Grid Overlay (GeoJSON)](../../assets/files/geo/standard-grid.geojson){ .md-button }

<!-- Emphasized Primary Action Button -->
[Download Incident Form (.docx)](../../assets/files/forms/incident-briefing.docx){ .md-button .md-button--primary }
```

### Contributor Best Practices for Binary Assets

- **Privacy & Data Sanitization**: Operational forms and logs must be completely sanitized. Ensure no mission-specific personal identifiable information (PII), lost person details, or sensitive operational logs are committed.
- **File Size Discipline**: Keep files as lightweight as possible (ideally under 10 MB). Avoid committing multi-gigabyte raster map tiles or raw aerial video to git; for large datasets, provide instructions and external links to authoritative open-data portals.
- **Clean Git Tracking**: Avoid committing temporary application lock files (`.~lock.*`, `~$*.docx`, `.DS_Store`, or OS thumbs).

---

## 5. Local Development & Preview (Optional)

You do **not** need to run the site locally to contribute. However, if you want to preview the rendered site locally before opening a pull request:

### Using Python
```powershell
pip install -r requirements.txt
mkdocs serve
```
Then visit `http://127.0.0.1:8000`.

### Using Docker
```powershell
docker run --rm -it -p 8000:8000 -v "${PWD}:/docs" squidfunk/mkdocs-material
```
Then visit `http://localhost:8000`.
