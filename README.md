# AI Security Engineer Portfolio

[![Site](https://img.shields.io/badge/Site-Live-3dff8b?style=flat-square)](https://et-sec.github.io/portfolio/)
[![CISSP](https://img.shields.io/badge/ISC2-CISSP-3dff8b?style=flat-square)](https://www.credly.com/badges/3bf52a18-c630-4a8f-a170-56ca462f3608)
[![SecurityX](https://img.shields.io/badge/CompTIA-SecurityX-3dff8b?style=flat-square)](https://www.credly.com/badges/15cf6f50-9a78-4405-9cde-3998c8117f84)
[![SSCP](https://img.shields.io/badge/ISC2-SSCP-3dff8b?style=flat-square)](https://www.credly.com/badges/3d58011f-2130-4a86-818d-f8bc414bbb41)
[![CCNA](https://img.shields.io/badge/Cisco-CCNA-3dff8b?style=flat-square)](https://www.credly.com/badges/6b1b0280-9d26-4b26-a368-0094ee0096b4)

**[et-sec.github.io/portfolio](https://et-sec.github.io/portfolio/)**: seven clickable architecture views of a multi-cloud reference platform, its threat model, the AI trust boundary, and the GRC library of 57 documents that proves the controls. One page, no build step. The same platform design has run on three clouds as Terraform: AWS, then DigitalOcean, now Oracle Cloud ARM.

Built and maintained by [Emmanuel Tigoue](https://www.linkedin.com/in/emmanuel-tigoue) | AI Security Engineer | Atlanta, GA

---

## The seven views

Each view sits inline on the page and has its own full page under `views/`. Every box is clickable and opens the controls behind it, each control's row in the System Security Plan, and the file in the source repo that proves it.

| View | What it shows |
|------|---------------|
| [Topology and flows](https://et-sec.github.io/portfolio/views/topology.html) | One hardened host, three trust segments, and every request, AI, audit, and change path |
| [Multi-cloud planes](https://et-sec.github.io/portfolio/views/multi-cloud.html) | Edge on Cloudflare, runtime on Oracle Cloud, security plane on AWS, what crosses between them, and what a lost account reaches |
| [Threat model](https://et-sec.github.io/portfolio/views/threat-model.html) | Six attacker positions, the wall that meets each one, and the residual |
| [Identity and access](https://et-sec.github.io/portfolio/views/identity-access.html) | Four privilege tiers, every credential with its lifetime, and what a stolen one reaches |
| [AI trust boundary](https://et-sec.github.io/portfolio/views/ai-trust.html) | Five models, three trust levels, every crossing out of the host, and what stands in front of it |
| [Control layers](https://et-sec.github.io/portfolio/views/control-layers.html) | Seven barrier layers, each with its NIST 800-53 Rev 5 controls |
| [Authorization boundary](https://et-sec.github.io/portfolio/views/authorization-boundary.html) | The boundary, the inherited controls, and every crossing with the control that governs it |

Every view is sanitized: no addresses, ports, hostnames, account IDs, regions, or image versions.

## The rest of the page

| Section | Contents |
|---------|----------|
| Certifications, experience, education | Cert cards with Credly verification links. Two roles with metric grids: CoreDirective (AI Security Engineer) and Texaco (IT Security and Operations Manager). Georgia State University, BA in Economics |
| Security engineering | STRIDE decomposition (29 threats), attack paths through the AI pipeline (7), one attack walked phase by phase, framework coverage by threat, and application security proof cards that link into the GRC library |
| AI security and governance | ISO 42001, ISO 27701, and NIST AI RMF cards, one shipped Falco rule with its breakdown, and an interactive decision tree for whether an AI system should ship |
| Governance, risk, and compliance | Library stats, control status, NIST 800-53 coverage by family (140 controls cited), and the incident response flow for a compromised container |
| Blog | Short notes on AI security, GRC, and building things, with the full feed on LinkedIn |

## How the numbers and drawings stay true

- Every number on the page sits inside a `<!-- METRIC:key -->` marker and is written from `metrics.yaml` in [cyber-squire1](https://github.com/ET-sec/cyber-squire1) by `scripts/sync_portfolio.py`. If the page and that file disagree, the page is wrong.
- Six views are generated from Python data files in `docs/architecture/views/` of the same repo, and the topology view is written by hand beside them. `scripts/sync_views.py` publishes all seven here, as `views/*.html` and as the inline `<!-- VIEW:slug -->` blocks in `index.html`.
- The `portfolio-sync` workflow in that repo runs on every pull request and push: it regenerates the views, checks the numbers against `metrics.yaml`, checks the published views against their sources, and runs the public checks (OPSEC, writing tells, control ids, cited paths, external links). Any drift fails the run.
- Change a fact once in the source repo, regenerate, sync, open a pull request here.

## Repository

```
.
├── index.html                                The whole site, one page, no build step
├── views/                                    Seven full page views, generated upstream
├── Emmanuel_Tigoue_AISecurity_Engineer.pdf   The resume the site links to
├── emmanuel-tigoue.jpg                       The photo on the page, metadata stripped
├── favicon.svg                               The tab icon
├── robots.txt                                Crawler rules
├── sitemap.xml                               The page list for search engines
└── .well-known/security.txt                  The security contact
```

Google Fonts (IBM Plex Sans, JetBrains Mono), dark and light themes, and a Content Security Policy in the page head.

## Links

- **Live:** [et-sec.github.io/portfolio](https://et-sec.github.io/portfolio/)
- **Resume:** [PDF](Emmanuel_Tigoue_AISecurity_Engineer.pdf)
- **Source repo:** [cyber-squire1](https://github.com/ET-sec/cyber-squire1): Terraform, the GRC library, CI/CD pipelines, the view generators
- **LinkedIn:** [linkedin.com/in/emmanuel-tigoue](https://www.linkedin.com/in/emmanuel-tigoue)
- **Credly:** [All certifications](https://www.credly.com/users/emmanuel-tigoue)
