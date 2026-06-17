# Amanda Cornett Harris — Portfolio Site

**Live site:** [amandacornettharris.ai](https://amandacornettharris.ai)

---

## Overview

Personal portfolio site for Amanda Cornett Harris — Customer Value, AI Transformation & Product and Design Strategy Executive. Built in collaboration with Claude.

---

## Tech Stack

- **Frontend:** Standalone HTML files, CSS, vanilla JavaScript
- **Fonts:** Inter (Google Fonts, weights 300–800)
- **Hosting:** Netlify (auto-deploys from `main`)
- **Design System:** Glass Design System v2.0 — documented in `DESIGN-SYSTEM.md`
- **No build step.** Every file is self-contained and deployable by copy/paste into GitHub's web editor.

---

## Pages

| File                  | Page           | Status          |
|-----------------------|----------------|-----------------|
| `index.html`          | Home           | ✅ Hero brand film |
| `impact-stories.html` | Impact Stories | ✅ Glass floating cards |
| `about.html`          | About          | ✅ Bio + testimonials carousel |
| `personal.html`       | Personal       | 🚧 Placeholder   |

---

## Design System

This site uses the **Glass Design System v2.0** (Option 2 Plus):

- **Glass chrome** on every page: gradient header, glass nav bar, centered glass "Let's Connect" CTA, glass footer
- **Floating glass cards** for every card and carousel: frosted panels with 3-layer depth shadows
- **Glass metrics strips** inside cards
- **Glass card buttons** for card CTAs
- **Hero brand film** on homepage: 7-scene animated narrative
- **Testimonials carousel** on about page: glass cards on blue gradient, 10s auto-advance

See `DESIGN-SYSTEM.md` for full token values, CSS specs, component patterns, and usage rules.

> **Rule:** Every card and carousel added to the site must use the glass card spec with floating shadows. No flat cards.

---

## Folder Structure

```
amandacornettharris-site/
├── index.html              Home — hero brand film
├── about.html              About — bio card + testimonials carousel
├── impact-stories.html     Impact Stories — floating glass cards
├── personal.html           Personal (placeholder)
├── images/
│   ├── agentforce-hero.jpg
│   ├── xd-team-hero.jpg
│   └── customer-cx-hero.jpg
├── DESIGN-SYSTEM.md        Component specs, tokens, patterns — v2.0
├── CHANGELOG.md            Session-by-session change log
└── README.md               This file
```

---

## Deployment

Every push to `main` auto-deploys to Netlify (~60 seconds).

**To update a page:**
1. Open the file on GitHub (click filename → pencil icon)
2. Select all (`Cmd+A`), delete, paste updated code
3. Write a commit message
4. Click **Commit changes directly to main**

**Batch update (recommended):** Press `.` on the repo page to open github.dev, edit all files in tabs, commit once.

---

## Working with Claude

At the start of each session:
1. Share the GitHub repo URL (public) or paste `DESIGN-SYSTEM.md`
2. Reference components by name (e.g. "glass card", "testimonials carousel", "hero film")
3. Claude generates complete, deployable HTML files

**Key constraint:** Files are standalone HTML — no shared CSS, no build tools, no framework.

---

## Contact

Amanda Cornett Harris
- Email: amandacornettharris@gmail.com
- LinkedIn: [linkedin.com/in/amandacharris](https://www.linkedin.com/in/amandacharris/)