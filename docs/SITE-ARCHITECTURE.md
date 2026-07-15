# Site Architecture

## Main Pages

| File | Page | Contents |
|---|---|---|
| `index.html` | Home | Hero · Metrics · Pull quote · 3 featured story cards · Footer |
| `about.html` | About Amanda | Bio · Visual timeline · How I Work · Team photos · Footer |
| `impact-stories.html` | Impact Stories | 3 featured cards + 6 grid cards · Each links to sub-page · Footer |
| `personal.html` | Personal | 5 photo sections: Horses · Community · Faith · Family · Outdoors · Footer |

## Impact Story Sub-Pages (`stories/` directory)

### Featured
| File | Story |
|---|---|
| `stories/help-salesforce.html` | Help.Salesforce.com |
| `stories/command-center.html` | Command Center |
| `stories/bnsf-digital-cx.html` | Creating BNSF's Digital Customer Experience |

### Additional
| File | Story |
|---|---|
| `stories/trackathon.html` | Trackathon |
| `stories/rail-recovery.html` | Rail Recovery Turnaround |
| `stories/bnsf-dex.html` | BNSF DEX Transformation |
| `stories/xd-transformation.html` | Transforming Experience Design |
| `stories/account-status.html` | Account Status *(content pending)* |
| `stories/hfrei-reduction.html` | HFREI Reduction *(content pending)* |

## Navigation Pattern

- **Any page** → Sticky nav: Home · About · Impact Stories · Personal
- **Homepage card** → `impact-stories.html#story-anchor` (scrolls to card)
- **Impact Stories "Read the story →"** → `stories/[story-name].html` (full sub-page)
- **Story sub-page** → Back to Impact Stories (browser back + explicit back link)
- **Story sub-page** → Next / Previous story at bottom
- **Hero "Read the story →"** → `about.html`

## Shared Footer (every page)

- Disclaimer: "All work examples shown are accessible via public domain or are summative communications and do not compromise protected company IP."
- Email: amandacornettharris@gmail.com
- LinkedIn icon → https://www.linkedin.com/in/amandacharris/

## Shared Components

- **Nav** — name left, links right, bronze active state, sticky on scroll
- **Footer** — disclaimer + email + LinkedIn icon
- **Fonts** — Playfair Display (headlines) + DM Sans (body)
- **Palette** — `#FAFAF7` bg · `#1E2A3A` charcoal · `#9A6E3A` bronze · `#1753C5` blue
- **images/** — all photos, referenced by relative path

## File Structure

```
amandacornettharris-site/
├── index.html
├── about.html
├── impact-stories.html
├── personal.html
├── stories/
│   ├── help-salesforce.html
│   ├── command-center.html
│   ├── bnsf-digital-cx.html
│   ├── trackathon.html
│   ├── rail-recovery.html
│   ├── bnsf-dex.html
│   ├── xd-transformation.html
│   ├── account-status.html   ← pending content
│   └── hfrei-reduction.html  ← pending content
└── images/
    └── ← all photos go here
```
