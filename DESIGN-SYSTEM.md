# Design System — Amanda Cornett Harris Portfolio

## Brand Direction
**Positioning:** "The person you call when the big thing needs to become real."
**Aesthetic:** Editorial — warm, authoritative, magazine-quality. Think Bloomberg Businessweek profile of the most interesting executive in the room.
**Emotional arc for visitors:**
1. **Land** → "This person operates at a level most people don't."
2. **Scroll** → "These numbers are real — this is enterprise scale."
3. **Explore** → "She doesn't just talk about transformation, she shows it."
4. **Leave** → "I need to talk to her."

---

## Color Palette

### The Two-Role Rule — do not break this

The site runs on **three** colors (blue, bronze, charcoal). A designer argued for two;
we kept three on one condition, written here so it is never violated: **blue and bronze
have separate, non-overlapping jobs, and they must never compete on the same element.**

- **Blue (`#1753C5`) = data + primary action.** Metric numbers, statistics, the one
  primary action in a view. If it's a number that proves impact or the single thing you
  most want clicked, it's blue.
- **Bronze (`#9A6E3A`) = editorial structure.** Section labels, eyebrows, hairline rules,
  pull-quote bars, active-nav underline, figure tags. Bronze frames and organizes; it
  never carries data and is never the primary action.
- **Never on the same element.** A single element gets blue *or* bronze, never both
  fighting for the eye. A bronze section label above a blue metric is correct (different
  elements, different jobs). A number rendered half-blue-half-bronze, or a button that is
  bronze *and* sits on a blue field competing for "click me," is not.

If, as pages accumulate, these roles start to blur — bronze creeping onto data, blue
creeping onto structure — that is the signal the designer was right: collapse to blue as
the only accent and demote bronze to a hairline. Until then, three colors stand.

### Primary
| Name | Hex | Usage |
|---|---|---|
| Blue | `#1753C5` | Metric/stat numbers; the single primary action in a view |
| Charcoal | `#1E2A3A` | Primary text, footer background, dark UI, default CTA text |
| Charcoal Mid | `#5A6678` | Body text, card descriptions |
| Page Cream | `#FAFAF7` | Page background — warm white, not pure white |

### Accent
| Name | Hex | Usage |
|---|---|---|
| Bronze | `#9A6E3A` | Editorial structure only: section labels, pull-quote bars, active-nav underline, hairline rules, figure tags, CTA hover |
| Bronze Warm | `#E8C89D` | Bronze on dark backgrounds (footer, dark hero) |
| Border | `#E8E4DC` | All borders, dividers, card edges |
| Muted Text | `#8A8A7A` | Nav links (inactive), stat labels, metadata |
| Card Cream | `#F5F2EC` | Before/After "after" cell, service chips hover |

### Dark (Footer / Story snapshots)
| Name | Hex | Usage |
|---|---|---|
| Footer Bg | `#1E2A3A` | Site footer background |
| Footer Text | `rgba(255,255,255,0.35)` | Disclaimer text on dark |
| Footer Links | `rgba(255,255,255,0.55)` | Email, icon links on dark |
| Snapshot Num | `#E8C89D` | Large numbers on dark snapshot panels |

---

## Typography

### Font Families
- **Headlines:** `'Playfair Display', serif` — loaded via Google Fonts
  - Used for: hero headlines, page titles, story titles, card headlines, metric numbers, pull quotes
  - Weights: 700, 900 (italic variants of both)
- **Body / UI:** `'DM Sans', sans-serif` — loaded via Google Fonts
  - Used for: nav, body text, labels, captions, CTAs, metadata
  - Weights: 300, 400, 500, 600

### Type Scale
| Element | Font | Size | Weight | Color | Notes |
|---|---|---|---|---|---|
| Nav name | Playfair Display | 15px | 700 | Charcoal | letter-spacing: -0.01em |
| Nav links | DM Sans | 10px | 500 | `#8A8A7A` | 0.14em spacing, uppercase |
| Nav active | DM Sans | 10px | 500 | Bronze | bronze bottom border |
| Hero headline | Playfair Display | 52px | 900 | Charcoal | -0.025em, italic em = bronze |
| Page title | Playfair Display | 48px | 900 | Charcoal | -0.025em |
| Story title | Playfair Display | 48px | 900 | Charcoal | -0.025em, italic em = bronze |
| Section heading | Playfair Display | 26px | 700 | Charcoal | -0.01em |
| Card headline (featured) | Playfair Display | 22px | 900 | Charcoal | -0.01em |
| Card headline (grid) | Playfair Display | 15px | 700 | Charcoal | -0.01em |
| Metric number | Playfair Display | 32px | 900 | Blue | -0.02em |
| Pull quote | Playfair Display | 18px | 400 italic | `#3D4F63` | line-height: 1.65 |
| Body text (story) | DM Sans | 15px | 300 | `#5A6678` | line-height: 1.85 |
| Body text (page) | DM Sans | 15px | 300 | `#5A6678` | line-height: 1.75 |
| Card brief | DM Sans | 13px | 300 | `#5A6678` | line-height: 1.75 |
| Section label | DM Sans | 10px | 600 | Bronze | 0.25em spacing, uppercase |
| Stat label | DM Sans | 9px | 400 | `#8A8A7A` | 0.12em spacing, uppercase |
| CTA text | DM Sans | 10–11px | 600 | Charcoal | 0.14–0.15em spacing, uppercase |

---

## Navigation

### Desktop Nav
- Background: `#FAFAF7` (page cream)
- Border-bottom: `1px solid #E8E4DC`
- Position: sticky, top 0, z-index 100
- Name: left-aligned, Playfair Display 15px 700
- Links: right-aligned, DM Sans 10px 500, uppercase, 0.14em spacing
- Active: color `#9A6E3A`, border-bottom `2px solid #9A6E3A`
- Hover: color `#1E2A3A`
- Padding: `0 48px` (desktop), `0 20px` (mobile)

### Mobile
- Nav collapses — bottom safe-area padding added to page content
- No hamburger. No overlay. Nav links visible in header.

---

## Page Layout

### Max Width
- All content sections: `max-width: 1100px; margin: 0 auto`
- Story sub-pages: `max-width: 780px; margin: 0 auto`

### Section Padding
- Desktop: `padding: 64px 48px`
- Mobile: `padding: 40px 20px`

---

## Components

### Hero (Homepage)
- Grid: `1fr 220px` — headline left, metrics stacked right
- Headline: Playfair Display 52px 900, italic bronze em
- Byline: DM Sans 15px 300, max-width 440px
- CTA: underline style, DM Sans 11px 600 uppercase, transitions bronze on hover
- Metrics: stacked with `1px solid #E8E4DC` dividers top/bottom

### Pull Quote
- Left: `3px solid #9A6E3A` bar
- Text: Playfair Display 18px italic
- Attribution: DM Sans 10px 600 uppercase bronze

### Featured Story Cards (Impact Stories page)
- Layout: alternating grid `1fr 340px` / `340px 1fr` (even cards flip)
- Image panel: min-height 260px, illustrative color treatment
- Body: `40px 44px` padding
- Company badge: DM Sans 9px 600 uppercase bronze
- Results row: borderless, sits on `border-top: 1px solid #F0EDE6`
- CTA: underline style, bronze on hover

### Grid Story Cards (Impact Stories page — second tier)
- 3-column grid, 24px gap
- Image: 120px height
- Body: 20px padding
- Same company badge + headline + brief + result + CTA pattern

### Story Sub-Pages
- Back link at top → `../impact-stories.html`
- Metrics bar: flex row, `border-top/bottom: 1px solid #E8E4DC`
- Before/After grid: 2-col, `#fff` / `#F5F2EC`, divided by `1px #E8E4DC`
- Snapshot panel: `#1E2A3A` bg, `#E8C89D` numbers
- Story navigation: prev/next links at bottom before footer
- Deck/artifact CTA: card with icon, title, subtitle, `↗` arrow

### Footer (all pages)
```
┌─────────────────────────────────────────────────────────┐
│  All work examples shown are accessible via public      │
│  domain or are summative communications and do not      │
│  compromise protected company IP.            [italic]   │
├─────────────────────────────────────────────────────────┤
│  CONNECT  [label]                                        │
│  © 2026 Amanda Cornett Harris    email  [LI icon]       │
└─────────────────────────────────────────────────────────┘
```
- Background: `#1E2A3A`
- Disclaimer: 11px italic `rgba(255,255,255,0.35)`, border-bottom `rgba(255,255,255,0.08)`
- Connect label: DM Sans 10px 600 uppercase bronze
- Copyright: DM Sans 11px `rgba(255,255,255,0.25)`
- Email: DM Sans 12px `rgba(255,255,255,0.55)` → white on hover
- LinkedIn: SVG icon, same color treatment, links to `https://www.linkedin.com/in/amandacharris/`
- **No Slack link** — removed (external users cannot reach internal Slack)

---

## Site Architecture

See `docs/SITE-ARCHITECTURE.md` for full structure. Summary:

| File | Page |
|---|---|
| `index.html` | Home |
| `about.html` | About Amanda |
| `impact-stories.html` | Impact Stories |
| `personal.html` | Personal |
| `stories/help-salesforce.html` | Story sub-page |
| `stories/command-center.html` | Story sub-page |
| `stories/bnsf-digital-cx.html` | Story sub-page |
| `stories/trackathon.html` | Story sub-page |
| `stories/rail-recovery.html` | Story sub-page |
| `stories/bnsf-dex.html` | Story sub-page |
| `stories/xd-transformation.html` | Story sub-page ✅ built |
| `stories/account-status.html` | Story sub-page (content TBD) |
| `stories/hfrei-reduction.html` | Story sub-page (content TBD) |
| `docs/xd-transformation-deck.pdf` | Source artifact (Amanda to add) |
| `images/` | All photos |

---

## Deployment Model

- **Hosting:** Netlify, auto-deploys from `main` branch of GitHub repo
- **Amanda's workflow:** Copy-paste full file contents into GitHub web editor → commit → Netlify deploys (~60 seconds)
- **No build step, no framework.** Every HTML file is standalone with inline `<style>` and `<script>`.
- Story sub-pages use relative paths: `../index.html`, `../impact-stories.html`, `../images/`, `../docs/`
- Always deliver complete, ready-to-paste files — not diffs or snippets

---

## Accessibility
- All text meets WCAG 2.0 AA contrast (4.5:1 minimum)
- Skip-to-main-content link on every page
- `aria-current="page"` on active nav items
- `aria-label` on icon-only links (LinkedIn)
- `role="main"` on `<main>`, `role="contentinfo"` on `<footer>`
- All images require `alt` text
- Keyboard navigable throughout
- Focus: visible outline on all interactive elements
