# HANDOFF — Amanda Cornett Harris Portfolio Site
Last updated: 2026-07-14. Reflects the editorial redesign completed in the July 2026 sessions.

---

## 1. Who this is for

Amanda Cornett Harris — Customer Adoption, AI Transformation & Product Strategy Executive.
20+ years. Currently UX Architect at Salesforce. Previously led Experience Design and
Digital Customer Experience at BNSF Railway.

- Email: amandacornettharris@gmail.com
- LinkedIn: https://www.linkedin.com/in/amandacharris/
- Phone: 918-208-8884
- Target domain: amandacornettharris.ai (confirm with Amanda before assuming it's live)

Resume source: `Amanda_Cornett_Harris_Resume_June_2026.txt` — source of truth for
bio/experience content. Site should complement it, not duplicate verbatim.

---

## 2. Repo & deployment model — CRITICAL

- **GitHub repo:** github.com/amandacornettharris-code/amandacornettharris-site
- **Hosting:** Netlify, auto-deploys from `main` branch (~60 sec after push)
- **Amanda's workflow:** Copy-paste full file contents into GitHub's web editor
  (pencil icon → paste → commit). She does NOT use git CLI or a local dev environment.
- **No build step, no framework.** Every HTML file is fully standalone with inline
  `<style>` and `<script>`. This is intentional — keeps her copy/paste workflow simple.
- **Always give Amanda complete, ready-to-paste files** — not diffs or snippets.
  Her editing method is "replace the whole file."

---

## 3. Current file structure

```
amandacornettharris-site/
├── index.html                  ⚠️ OLD design — needs rebuild to editorial spec
├── about.html                  ⚠️ OLD design — needs rebuild to editorial spec
├── impact-stories.html         ⚠️ OLD design — needs rebuild to editorial spec
├── personal.html               ⚠️ OLD design — needs rebuild to editorial spec
├── stories/
│   ├── xd-transformation.html  ✅ BUILT — editorial design, live
│   ├── help-salesforce.html    ⚠️ Stub or missing — needs build
│   ├── command-center.html     ⚠️ Stub or missing — needs build
│   ├── bnsf-digital-cx.html    ⚠️ Stub or missing — needs build
│   ├── trackathon.html         ⚠️ Stub or missing — needs build
│   ├── rail-recovery.html      ⚠️ Stub or missing — needs build
│   ├── bnsf-dex.html           ⚠️ Stub or missing — needs build
│   ├── account-status.html     ⚠️ Content TBD — Amanda has not provided details
│   └── hfrei-reduction.html    ⚠️ Content available (PDF pg 6) — needs build
├── docs/
│   ├── SITE-ARCHITECTURE.md    ✅ Current — full page/nav/file structure reference
│   └── xd-transformation-deck.pdf  ← Amanda must add this manually to repo
├── images/                     ← All photos go here; currently empty
├── DESIGN-SYSTEM.md            ✅ Current — full editorial design spec
├── HANDOFF.md                  This file
├── IA.md                       ✅ Current — information architecture
├── CHANGELOG.md                Session history
└── README.md                   Project overview
```

---

## 4. Design system — quick reference

Full spec: `DESIGN-SYSTEM.md`. Essentials:

**Aesthetic:** Editorial — warm, authoritative, magazine-quality.
Think Bloomberg Businessweek profile of the most interesting executive in the room.

**Fonts:**
- Headlines: `Playfair Display` — 700, 900 (italic variants of both)
- Body/UI: `DM Sans` — 300, 400, 500, 600
- Both loaded via Google Fonts

**Colors:**
- Blue: `#1753C5` — metric numbers, CTAs
- Charcoal: `#1E2A3A` — primary text, footer bg
- Page cream: `#FAFAF7` — page background
- Bronze: `#9A6E3A` — nav active, section labels, pull quote bars, CTAs
- Border: `#E8E4DC` — all borders and dividers

**Nav:** Sticky, cream bg, name left (Playfair 15px 700), links right (DM Sans 10px uppercase).
Active state: bronze color + 2px bronze bottom border. No hamburger on mobile.

**Footer (every page):** Dark charcoal (`#1E2A3A`) bg. IP disclaimer italic. "Connect"
bronze label. Copyright left, email + LinkedIn SVG icon right. No Slack link.

**Accessibility:** WCAG 2.0 AA. Skip links, aria-current, aria-label on icon links,
visible focus rings on all interactive elements.

---

## 5. Current state: the redesign is in mockups, not live HTML

The editorial redesign was completed as browser companion mockups and one story sub-page.
**The four main HTML files (index, about, impact-stories, personal) still have the old design.**

**What IS done (new editorial design):**
- `stories/xd-transformation.html` — full story sub-page, ready to paste
- `DESIGN-SYSTEM.md` — fully rewritten for editorial direction
- `docs/SITE-ARCHITECTURE.md` — new, documents full site structure
- `IA.md` — updated for new architecture

**What still needs to be built (in priority order):**
1. `impact-stories.html` — 3 featured cards + 6 grid cards (mockup exists as reference)
2. `index.html` — editorial hero, metrics, pull quote, 3 featured work cards
3. `about.html` — bio, visual timeline, How I Work section
4. `personal.html` — 5 photo sections (horses, community, faith, family, outdoors)
5. 8 remaining story sub-pages (see §6)

**Reference mockups** (in browser companion session, not on disk):
- Homepage mockup: hero grid, Benioff pull quote, 3 work cards
- Impact stories mockup: featured alternating layout + 6-card grid

Use `stories/xd-transformation.html` as the canonical template for story sub-pages.
Use `DESIGN-SYSTEM.md` as the canonical spec for all design decisions.

---

## 6. Story sub-pages — status

| File | Story | Status | Notes |
|---|---|---|---|
| `stories/help-salesforce.html` | Help.Salesforce.com | ⚠️ Build needed | Salesforce; featured card |
| `stories/command-center.html` | Command Center | ⚠️ Build needed | Salesforce; featured card |
| `stories/bnsf-digital-cx.html` | BNSF Digital CX | ⚠️ Build needed | BNSF; featured card |
| `stories/trackathon.html` | Trackathon | ⚠️ Build needed | BNSF |
| `stories/rail-recovery.html` | Rail Recovery Turnaround | ⚠️ Build needed | BNSF |
| `stories/bnsf-dex.html` | BNSF DEX Transformation | ⚠️ Build needed | BNSF |
| `stories/xd-transformation.html` | Transforming Experience Design | ✅ Done | BNSF; links to PDF artifact |
| `stories/account-status.html` | Account Status | ⚠️ Content TBD | Amanda to provide company + what + metric |
| `stories/hfrei-reduction.html` | HFREI Reduction | ⚠️ Build needed | Content from PDF page 6 |

**Story sub-page template:** `stories/xd-transformation.html`
- Back link → `../impact-stories.html`
- Company badge, story title (Playfair 48px, italic em = bronze), lede
- Metrics bar (blue numbers, border top/bottom)
- Sections: label + heading + body text
- Before/After grid, Snapshot panel (dark bg, bronze numbers), Pull quotes
- Artifact CTA card (PDF link) if applicable
- Story navigation (prev/next) at bottom
- Footer identical to all pages

**Story navigation order** (for prev/next links):
help-salesforce → command-center → bnsf-digital-cx → trackathon → rail-recovery →
bnsf-dex → xd-transformation → account-status → hfrei-reduction

---

## 7. Content Amanda still needs to provide

- [ ] PDF: `docs/xd-transformation-deck.pdf` — must be added to GitHub repo manually
- [ ] Account Status story: company name, what she did, result/metric
- [ ] Product screenshots for impact story cards (card image placeholders are gray boxes)
- [ ] Professional headshot (about page, homepage)
- [ ] Personal page photos: horses, community, faith, family, outdoors

---

## 8. Working conventions

- Always deliver **complete, ready-to-paste HTML files** — not diffs or snippets.
- Every file stays standalone (inline CSS/JS) — no shared stylesheet or JS bundle.
- Maintain WCAG 2.0 AA on every change.
- Use `stories/xd-transformation.html` as the template for all story sub-pages.
- Zero hallucination: all content from resume or user-provided materials only.
  State what's unknown rather than inventing plausible details.
- When Amanda provides content (quotes, metrics, copy), use it verbatim or close to it.
- No dates on impact story cards (Amanda requested removal).
- Stripe unused content rather than hiding it — keep files clean.

---

## 9. Suggested first message to a new Claude instance

"I'm continuing work on my portfolio site. Read HANDOFF.md first, then
DESIGN-SYSTEM.md and docs/SITE-ARCHITECTURE.md. I want to tackle [whatever
Amanda wants next — likely rebuilding index.html or impact-stories.html to the
editorial design]."
