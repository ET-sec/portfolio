# Emmanuel Tigoue - AI Security Engineer Portfolio

[![Live Site](https://img.shields.io/badge/Site-Live-3dff8b?style=flat-square)](https://et-sec.github.io/portfolio/)
[![CISSP](https://img.shields.io/badge/CISSP-Certified-ffc247?style=flat-square)](https://www.credly.com/users/emmanuel-tigoue)
[![SecurityX](https://img.shields.io/badge/SecurityX-Certified-3dff8b?style=flat-square)](https://www.credly.com/users/emmanuel-tigoue)
[![SSCP](https://img.shields.io/badge/SSCP-Certified-3dff8b?style=flat-square)](https://www.credly.com/users/emmanuel-tigoue)
[![CCNA](https://img.shields.io/badge/CCNA-Certified-3dff8b?style=flat-square)](https://www.credly.com/users/emmanuel-tigoue)

Portfolio for AI security engineering work: a multi-cloud reference platform, its threat model, the AI trust boundary, and the GRC library that documents it. One Terraform codebase proven on AWS, DigitalOcean, and Oracle Cloud ARM.

## What's Here

### Platform
Seven architecture views drawn from the reference design, each with its own full-size page under `views/`:
topology and flows, multi-cloud planes, threat model, identity and access, AI trust, control layers, authorization boundary.
Every view is sanitized: no addresses, ports, hostnames, account IDs, or image versions. Live state per control lives in the POA&M, not on the drawings.

### Certifications, Experience, Education
Cert cards with Credly verification links. Two roles with metric grids: CoreDirective (AI Security Engineer) and Texaco (IT Security and Operations Manager).

### Security Engineering
Threat model view, STRIDE decomposition (29 threats), attack trees (7 paths), red team walkthrough, framework coverage matrix, identity and access view, application security proof cards linking to the GRC documents.

### AI Security and Governance
Framework cards (ISO 42001, ISO 27701, NIST AI RMF), the AI trust view, a shipped Falco rule with its breakdown, and an interactive deployment decision tree.

### GRC
Control layers view, 57-document library stats, NIST 800-53 coverage by family, POA&M scorecard, IR flowchart, authorization boundary view.

## How the numbers and drawings stay true

- Numbers on the page sit inside `<!-- METRIC:key -->` markers and are written from `metrics.yaml` in the [cyber-squire1](https://github.com/ET-sec/cyber-squire1) repo by `scripts/sync_portfolio.py`.
- The architecture views are generated from Python data files in `docs/grc/diagrams/views/` of the same repo (`render_views.py`), then published here by `scripts/sync_views.py`, which writes `views/*.html` and the inline `<!-- VIEW:slug -->` blocks in `index.html`. `--check` fails on drift.
- Change a fact once in the source repo, regenerate, sync, open a PR.

## Stack

Single `index.html` with CSS and JS inline, plus seven standalone view pages. No build step, no dependencies. Google Fonts (IBM Plex Sans, JetBrains Mono). Dark and light themes.

## Links

- **Live:** [et-sec.github.io/portfolio](https://et-sec.github.io/portfolio/)
- **Infrastructure repo:** [cyber-squire1](https://github.com/ET-sec/cyber-squire1) (GRC library, CI/CD pipelines, Terraform, view generators)
- **LinkedIn:** [Emmanuel Tigoue](https://www.linkedin.com/in/emmanuel-tigoue)
- **Credly:** [Certifications](https://www.credly.com/users/emmanuel-tigoue)
