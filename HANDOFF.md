# HANDOFF — Amanda Cornett Harris Portfolio Site
Last updated: 2026-07-16. All four main pages are live on the editorial design.
Two story sub-pages are now built (`xd-transformation.html`, `help-salesforce.html`);
the remaining 6 are unbuilt. The Help.Salesforce.com sub-page no longer carries a
Sources/footnotes section (removed) — its metrics are the site's live public counters.

**Deck-link pattern (available, not currently used by any card):** A featured card's
"Read the story" CTA *can* point to a PDF in `docs/` instead of a sub-page, opening in a
new tab via `target="_blank" rel="noreferrer"`. Use hyphenated, space-free filenames in
`docs/` so hrefs need no URL-encoding. The Help.Salesforce.com card briefly used this, but
now links to the built `stories/help-salesforce.html` sub-page; the deck lives on that page
under "Source Material" instead. When Amanda uploads a PDF via GitHub's web editor, confirm
the branch is `main` and the file lands in `docs/`.

**Featured-card image convention:** All three featured "spotlight" cards keep their hero
image on the **same (right) edge** — the `nth-child(even)` grid-swap was removed so headlines
align down one left axis (lower eye-tracking load). Real product screenshots go through
`img.story-photo` (`object-fit:cover; object-position:center`). Because the card image panel
is narrow/portrait (~340px) and screenshots are wide, don't drop a raw browser grab in — it
crops to junk. Instead: strip all browser/site chrome, then compose the product hero as a
rounded, shadowed frame centered on a matching brand gradient (see
`images/help-salesforce-hero.png`, built from the deck's slide 1 via PIL). The 3 spotlight
cards are DUPLICATED verbatim in BOTH `index.html` and `impact-stories.html` — edit both.

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
├── index.html                  ✅ LIVE — editorial design
├── about.html                  ✅ LIVE — editorial design + testimonial carousel
├── impact-stories.html         ✅ LIVE — editorial design
├── personal.html               ✅ LIVE — editorial design
├── stories/
│   ├── xd-transformation.html  ✅ BUILT — editorial design, live (template for the rest)
│   ├── help-salesforce.html    ✅ BUILT — card links here; deck under "Source Material"
│   ├── command-center.html     ⚠️ Not built — linked from index + impact-stories
│   ├── bnsf-digital-cx.html    ⚠️ Not built — linked from index + impact-stories
│   ├── trackathon.html         ⚠️ Not built — linked from impact-stories
│   ├── rail-recovery.html      ⚠️ Not built — linked from impact-stories
│   ├── bnsf-dex.html           ⚠️ Not built — linked from impact-stories
│   ├── account-status.html     ⚠️ Not built — content TBD (Amanda to provide)
│   └── hfrei-reduction.html    ⚠️ Not built — content available (PDF pg 6)
├── docs/
│   ├── SITE-ARCHITECTURE.md    ✅ Current — full page/nav/file structure reference
│   ├── help-salesforce-deck.pdf    ✅ In repo — Help.Salesforce.com Impact Story deck (10 pages); linked from the sub-page
│   ├── 5-key-mindset-shifts.pdf    ✅ In repo — TDX deck; linked from Help.SF sub-page "Source Material"
│   └── xd-transformation-deck.pdf  ← Amanda must add this manually to repo
├── images/
│   └── help-salesforce-hero.png    ✅ Card hero for Help.SF (framed slide-1 product shot on gradient)
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

## 5. Current state: main pages live, story sub-pages are the remaining work

The editorial redesign is **live across all four main pages** (index, about,
impact-stories, personal). Since the initial redesign, two follow-up changes shipped:
- **Testimonial carousel on `about.html`** — Broadsheet style with blue accent
- **Mobile nav** — stacked layout + active underline, applied to all pages

**What IS done:**
- All four main pages — editorial design, live
- `stories/xd-transformation.html` — full story sub-page (canonical template)
- `stories/help-salesforce.html` — full story sub-page (Help.Salesforce.com)
- `DESIGN-SYSTEM.md`, `docs/SITE-ARCHITECTURE.md`, `IA.md` — current

**What still needs to be built:**
- The 6 unbuilt story sub-pages (see §6). All are already linked from
  impact-stories.html (and two from index.html), so those links currently 404.

Use `stories/xd-transformation.html` as the canonical template for story sub-pages.
Use `DESIGN-SYSTEM.md` as the canonical spec for all design decisions.

---

## 6. Story sub-pages — status

| File | Story | Status | Notes |
|---|---|---|---|
| `stories/help-salesforce.html` | Help.Salesforce.com | ✅ Done | Built from the xd-transformation template. Featured card (in BOTH index + impact-stories) links here. Two cleared decks linked under "Source Material" (`help-salesforce-deck.pdf`, `5-key-mindset-shifts.pdf`). Metrics now use the site's live public counters: **4.75M+ Agentforce conversations** and **2.3M+ requests handled by humans** (chat + Agentforce, cumulative since October 2024, "as of July '26" disclaimer). The Sources/footnotes section was removed. Guardrails: never link/describe the "SF Chat Modernization" deck (Salesforce-internal only); TDX presentation was co-authored by Amanda but delivered on stage by Emily Winslow & Nimma Bhusri; **NEVER reintroduce the 82% self-service / co-sourced 2.2M+ stat — internal evidence shows it's contrived and it was deliberately removed.** |
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
command-center → help-salesforce → bnsf-digital-cx → trackathon → rail-recovery →
bnsf-dex → xd-transformation → account-status → hfrei-reduction

Featured-card order (index.html + impact-stories.html): Command Center first, then
Help.Salesforce.com, then BNSF Digital CX — Command Center is the more recent work.

---

## 7. Content Amanda still needs to provide

- [ ] PDF: `docs/xd-transformation-deck.pdf` — must be added to GitHub repo manually
- [ ] Account Status story: company name, what she did, result/metric
- [ ] Product screenshots for the Command Center + BNSF cards (still CSS placeholders; the
      Help.Salesforce.com card now uses a real framed screenshot — see image convention in intro)
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
