# Canadian SAR Technology Hub 🇨🇦

A community-maintained, open-source directory of Ground Search and Rescue (GSAR) resources, technologies, procedures, training standards, and operational templates across Canada.

The website is generated automatically from this repository's Markdown files and published statically to **GitHub Pages**.

[View the live Canadian SAR Technology Hub (GitHub Pages)](https://bradley-parker.github.io/Canadian-SAR-Technology-Hub/)

---

## 🧭 Core Principles & Values

- **Practitioner-Driven & Field-Tested**: Every tool, template, and procedure reflects real-world operational experience from active Canadian SAR personnel.
- **Strictly Non-Commercial & Independent**: No sponsored posts or promotional marketing pitches. Unproven vendor claims are not published. (Affiliate links are only permitted with clear disclosure when proceeds directly benefit a volunteer SAR team or non-profit organization).
- **Objective Coverage of Commercial Tools**: Paid tools widely deployed by SAR teams (e.g., CalTopo, Garmin inReach, Starlink) are covered honestly, detailing field limitations, reliability in cold climates, and subscription costs.
- **Zero-Server / Purely Static**: Hosted on GitHub Pages with in-browser search and tag filtering. No external database or CMS.
- **Human-Readable & Portable**: All content is stored in standard Markdown with clean YAML frontmatter.

---

## 📁 Repository Structure

```text
├── AGENTS.md                      # AI and contributor style, tone, and operational guide
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── new-resource.yml       # Web form for contributors who don't use Git
│   │   └── config.yml
│   ├── PULL_REQUEST_TEMPLATE.md   # Checklist for pull requests
│   └── workflows/
│       ├── deploy.yml             # Auto-builds & deploys to GitHub Pages on push
│       └── validate-pr.yml        # Validates PRs against dead links and syntax
├── docs/                          # Operational site content
│   ├── index.md                   # Clean practitioner homepage
│   ├── tags.md                    # In-browser tag index
│   ├── downloads/
│   │   └── index.md               # Guide to downloadable files and attachments
│   ├── contributing/
│   │   ├── index.md               # Community contribution guide
│   │   ├── editorial-standards.md # Field testing & vendor neutrality policy
│   │   ├── template.md            # Copy-paste starting template for resources
│   │   ├── taxonomy.md            # Category, tag, and province guidelines
│   │   └── technical-guide.md     # Deep technical architecture & site mechanics
│   ├── resources/                 # Operational resource guides by domain
│   │   ├── mapping-gis/
│   │   ├── communications/
│   │   ├── search-management/
│   │   ├── field-hardware/
│   │   ├── training-standards/
│   │   └── medical-evacuation/
│   └── assets/                    # Images and downloadable binary blobs
│       ├── images/                # Screenshots, diagrams, photos
│       └── files/
│           ├── geo/               # .geojson, .gpx, .kml, .kmz
│           ├── forms/             # .docx, .xlsx, .pdf
│           └── configs/           # Device codeplugs, radio configs
├── mkdocs.yml                     # Site navigation, Material theme, & plugins
├── requirements.txt               # Build dependency list (for GitHub Actions)
└── README.md
```

---

## 🤝 How to Contribute

Anyone with a good idea, tool, or template is welcome to contribute!

### Method 1: Web-based Edit (Fastest)
1. On any page of the published website, click the **pencil icon** (:material-pencil:) at the top right.
2. Edit the Markdown directly in GitHub's web interface.
3. Click **Commit changes** to automatically open a Pull Request.

### Method 2: GitHub Issue Form (No Git Required)
If you prefer not to touch Markdown, open a **[New Resource Submission Issue](https://github.com/Bradley-Parker/Canadain-SAR-Technology-Hub/issues/new?template=new-resource.yml)**. Fill in the form fields and drag-and-drop any files or screenshots; maintainers will format it for you.

### Method 3: Pull Request with Template
1. Create a new `.md` file inside the appropriate `docs/resources/<category>/` directory.
2. Follow the template defined in [`docs/contributing/template.md`](docs/contributing/template.md).
3. Open a Pull Request. GitHub Actions will automatically validate formatting and link integrity.

---

## ⚙️ How It Works (For Maintainers)

- **Build Engine**: [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).
- **CI/CD**: GitHub Actions (`.github/workflows/deploy.yml`) runs on every push to `main`, builds the static site, and deploys it to GitHub Pages.
- **Local Preview (Optional)**:
  You don't need Python to contribute, but if you want to preview the site locally on your computer:
  ```bash
  pip install -r requirements.txt
  ```
  then
  ```bash
  mkdocs serve
  ```
  Then open `http://127.0.0.1:8000` in your web browser.

---

## 📜 License
Distributed under the Apache 2.0 License. See [LICENSE](LICENSE) for details.
