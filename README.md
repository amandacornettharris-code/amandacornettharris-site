# Amanda Cornett Harris — Portfolio Site

**Live site:** [amandacornettharris.ai](https://amandacornettharris.ai)

---

## Overview

Personal portfolio site for Amanda Cornett Harris — Customer Value, AI Transformation & Product and Design Strategy Executive. Built in collaboration with Claude.

---

## Tech Stack

- **Frontend:** Standalone HTML files, CSS, vanilla JavaScript
- **Fonts:** Inter (Google Fonts, weights 400–800)
- **Hosting:** Netlify (auto-deploys from `main`)
- **Design System:** Glass Design System v2.0 — documented in `DESIGN-SYSTEM.md`
- **No build step.** Every file is self-contained and deployable by copy/paste into GitHub's web editor.

---

## Pages

| File                  | Page           | Status          |
|-----------------------|----------------|-----------------|
| `index.html`          | Home           | ✅ Live          |
| `impact-stories.html` | Impact Stories | ✅ Live          |
| `about.html`          | About          | ✅ Live          |
| `personal.html`       | Personal       | 🚧 Placeholder   |

---

## Design System

This site uses the **Glass Design System v2.0** (Option 2 Plus):

- **Glass chrome** on every page: gradient header, glass nav bar, glass "Let's Connect" CTA, glass footer
- **Glass cards** for every card and carousel: frosted white panels with backdrop-filter blur
- **Glass metrics strips** inside cards
- **Glass card buttons** for card CTAs

See `DESIGN-SYSTEM.md` for full token values, CSS specs, component patterns, and usage rules.

> **Rule:** Every card and carousel added to the site must use the glass card spec. No flat cards.

---

## Folder Structure

```
amandacornettharris-site/
├── index.html              Home page
├── about.html              About page
├── impact-stories.html     Impact Stories page
├── personal.html           Personal page (placeholder)
├── images/
│   ├── agentforce-hero.jpg     TDX slide screenshot (purple)
│   ├── xd-team-hero.jpg        BNSF XD Team slide (green)
│   └── customer-cx-hero.jpg    BNSF locomotive slide (blue)
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
3. Write a commit message (e.g. `index.html — glass design system v2`)
4. Click **Commit changes directly to main**
5. Netlify deploys automatically

**Recommended commit order when updating all files:**
1. `DESIGN-SYSTEM.md`
2. `CHANGELOG.md`
3. `README.md`
4. `index.html`
5. `about.html`
6. `impact-stories.html`
7. `personal.html`

---

## Images

Hero images for Impact Story cards are screenshots of PDF cover slides. Place in the `images/` folder at root level.

| File                       | Story              | Color    |
|----------------------------|--------------------|----------|
| `images/agentforce-hero.jpg` | Salesforce / TDX | Purple   |
| `images/xd-team-hero.jpg`    | BNSF XD Team     | Green    |
| `images/customer-cx-hero.jpg`| BNSF Digital CX  | Blue     |

Cards display gradient fallbacks until images are added.

---

## Working with Claude

This site is built in collaboration with Claude (claude.ai). At the start of each session:

1. Share the URL of the GitHub repo (public) or paste the current `DESIGN-SYSTEM.md` content
2. Reference the component you want to build by name (e.g. "glass card", "glass metrics strip")
3. Claude will generate complete, deployable HTML files ready to paste into GitHub

**Key constraint:** Files are standalone HTML — no shared CSS files, no build tools, no framework.

---

## Contact

Amanda Cornett Harris
- Email: amandacornettharris@gmail.com
- LinkedIn: [linkedin.com/in/amandacharris](https://www.linkedin.com/in/amandacharris/)
- Phone: 918-208-8884