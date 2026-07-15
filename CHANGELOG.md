# Changelog — Amanda Cornett Harris Portfolio Site

---

## 2026-07-14 — Editorial redesign complete across all 4 main pages

### Design direction
Full editorial redesign replacing the previous Inter/gradient/gradient-header design.
Canonical reference: `impact-stories.html`. All pages now match its CSS exactly.

**Design system:** Playfair Display (headlines, 700/900) + DM Sans (body/UI, 300–600).
Palette: `#FAFAF7` cream, `#1E2A3A` charcoal, `#1753C5` blue, `#9A6E3A` bronze, `#E8E4DC` border.
Nav: sticky cream bar, name left (Playfair 15px), links right (DM Sans 10px uppercase).
Footer: dark charcoal bg, IP disclaimer, Connect label, email + LinkedIn icon. No Slack link.

### Pages updated
- **`index.html`** — Editorial hero (headline + metrics stat stack + Benioff pull quote), 3 featured story cards
- **`impact-stories.html`** — Page header, 3 alternating featured story cards, divider, 6-card second-tier grid
- **`about.html`** — Rebuilt from old design: bio, Benioff pull quote, 6-entry career timeline
- **`personal.html`** — Rebuilt from old design: 5 alternating photo sections (horses, community, faith, family, outdoors) with placeholder panels

### Story sub-pages
- **`stories/xd-transformation.html`** — Confirmed correct. Editorial design, full story content, PDF artifact link, story navigation

### Docs
- `README.md` — Rewritten to reflect current design system, file structure, workflow
- `CHANGELOG.md` — This file
- `DESIGN-SYSTEM.md` — Rewritten for editorial direction
- `HANDOFF.md` — Rewritten with full session context and working conventions
- `IA.md` — Updated: 4-page nav + 9 story sub-pages, no Vault/Admin

### Repo
- `.gitignore` added — excludes `.claude/`, `.cursor/`, `.superpowers/`, resume, `.DS_Store`
- `docs/SITE-ARCHITECTURE.md` removed — superseded by `IA.md`
- `images/` — retained (empty, photos pending)
- `docs/` — retained (PDF artifacts go here when Amanda uploads them)

### Pending (next session)
- 8 remaining story sub-pages to build: help-salesforce, command-center, bnsf-digital-cx, trackathon, rail-recovery, bnsf-dex, account-status (content TBD), hfrei-reduction
- Account Status: Amanda to provide company, what she did, metric
- PDF: `docs/xd-transformation-deck.pdf` — Amanda to upload to GitHub manually
- Photos: `images/` — Amanda to upload professional headshot + personal photos

---

## 2026-06-09 — Session 1 (previous design)

Initial build using Inter font, gradient header, scroll-aware sticky nav, mobile bottom tab bar.
Four pages: index, about, impact-stories, personal (placeholder).
This design was fully replaced in the 2026-07-14 session.
