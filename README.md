# Amanda Cornett Harris — Portfolio Site

Personal portfolio site for Amanda Cornett Harris — Customer Adoption, AI Transformation & Product Strategy Executive. 20+ years building zero-to-one products, platforms, and transformations across AI, enterprise SaaS, and industrial operations at scale.

## Live Site

Target: [amandacornettharris.ai](https://amandacornettharris.ai) — confirm domain is live before sharing.

## Tech Stack

- **Frontend:** Vanilla HTML, CSS — no framework, no build step
- **Fonts:** Playfair Display + DM Sans (Google Fonts)
- **Hosting:** Netlify — auto-deploys from `main` branch (~60 sec after push)
- **Deploy workflow:** Amanda copies full file contents into GitHub web editor → commit → Netlify deploys

## File Structure

```
amandacornettharris-site/
├── index.html                  Home
├── about.html                  About Amanda
├── impact-stories.html         Impact Stories (featured + grid)
├── personal.html               Personal (horses, community, faith, family, outdoors)
├── stories/
│   ├── xd-transformation.html  ✅ Built
│   ├── help-salesforce.html    ⚠ Needs build
│   ├── command-center.html     ⚠ Needs build
│   ├── bnsf-digital-cx.html    ⚠ Needs build
│   ├── trackathon.html         ⚠ Needs build
│   ├── rail-recovery.html      ⚠ Needs build
│   ├── bnsf-dex.html           ⚠ Needs build
│   ├── account-status.html     ⚠ Content TBD
│   └── hfrei-reduction.html    ⚠ Needs build
├── docs/                       PDF artifacts (Amanda adds manually)
├── images/                     Photos (Amanda adds manually)
├── DESIGN-SYSTEM.md            Full design spec
├── HANDOFF.md                  Session history + working conventions
├── IA.md                       Information architecture
├── CHANGELOG.md                Change log
└── README.md                   This file
```

## Design System

See `DESIGN-SYSTEM.md` for the full spec. Quick reference:

| Token | Value | Use |
|---|---|---|
| Page cream | `#FAFAF7` | Page background |
| Charcoal | `#1E2A3A` | Primary text, footer bg |
| Blue | `#1753C5` | Metric numbers |
| Bronze | `#9A6E3A` | Active nav, labels, accents |
| Border | `#E8E4DC` | All dividers |
| Headline font | Playfair Display 700/900 | All headings |
| Body font | DM Sans 300/400/500/600 | All body + UI |

## Deployment

Every push to `main` triggers a Netlify deploy.

**Amanda's update workflow:**
1. Open the file on GitHub (pencil icon → edit)
2. Select all → paste updated file content
3. Commit to `main`
4. Netlify deploys in ~60 seconds

Every HTML file is self-contained with inline `<style>`. No shared stylesheet, no build step.

## Adding Content

**Photos:** Upload to `images/` via GitHub → add file. Reference as `images/filename.jpg`.

**PDF artifacts:** Upload to `docs/` via GitHub → add file. Reference as `docs/filename.pdf`.

**New story sub-pages:** Use `stories/xd-transformation.html` as the template. Relative paths: `../index.html`, `../impact-stories.html`, `../images/`, `../docs/`.

## Contact

Amanda Cornett Harris
- Email: amandacornettharris@gmail.com
- LinkedIn: [linkedin.com/in/amandacharris](https://www.linkedin.com/in/amandacharris/)
