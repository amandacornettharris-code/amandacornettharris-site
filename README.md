# Amanda Cornett Harris — Portfolio Site

**Live site:** [amandacornettharris.ai](https://amandacornettharris.ai)

## Overview
Personal portfolio site for Amanda Cornett Harris — Customer Adoption, AI Transformation & Product Strategy Executive. Built in collaboration with Claude.

## Tech Stack
- **Frontend:** HTML, CSS, vanilla JavaScript
- **Fonts:** Inter (Google Fonts)
- **Hosting:** Netlify (auto-deploys from `main`)
- **Design System:** Custom — documented in `DESIGN-SYSTEM.md`

## Pages
| File | Page | Status |
|---|---|---|
| `index.html` | Home | ✅ Live |
| `impact-stories.html` | Impact Stories | ✅ Live |
| `about.html` | About | ✅ Live (old header — needs update) |
| `personal.html` | Personal | 🚧 Placeholder |

## Folder Structure
```
amandacornettharris-site/
├── index.html
├── about.html
├── impact-stories.html
├── personal.html
├── images/
│   ├── agentforce-hero.jpg
│   ├── xd-team-hero.jpg
│   └── customer-cx-hero.jpg
├── DESIGN-SYSTEM.md
├── CHANGELOG.md
└── README.md
```

## Deployment
Every push to `main` auto-deploys to Netlify.

**To update a page:**
1. Edit the file on GitHub (pencil icon)
2. Paste updated code
3. Commit to `main`
4. Netlify deploys in ~60 seconds

Amanda deploys by copy-pasting code directly into GitHub's web editor (no git CLI, no build step, no framework — every HTML file is standalone).

## Images
Hero images for Impact Story cards should be screenshots of PDF cover slides:
- `agentforce-hero.jpg` — TDX presentation slide 1 (blue/purple with robot)
- `xd-team-hero.jpg` — BNSF Experience Design Team slide 1 (green with team photo)
- `customer-cx-hero.jpg` — BNSF Digital Customer Experience slide 1 (locomotive)

Place in the `images/` folder at root level. Not yet deployed — pages currently fall back to gradient placeholders via `onerror` on the `<img>` tags.

## Design System
See `DESIGN-SYSTEM.md` for full component documentation including:
- Color palette
- Typography
- Button system (5 variants × 3 sizes × 4 states)
- Impact Story cards
- Page chrome (header, nav, footer)

## Contact
Amanda Cornett Harris
- Email: amandacornettharris@gmail.com
- LinkedIn: linkedin.com/in/amandacharris
- Phone: 918-208-8884
