# Information Architecture — Amanda Cornett Harris Portfolio

## Navigation Structure

Four pages in primary nav. Impact Stories links to 9 story sub-pages (not in nav).

```
┌────────────────────────────────────────────────────┐
│                  Primary Nav (4)                   │
├──────────┬──────────┬────────────────┬─────────────┤
│   Home   │  About   │ Impact Stories │  Personal   │
└──────────┴──────────┴───────┬────────┴─────────────┘
                              │
                    Story sub-pages (9)
                              │
             ┌────────────────┼────────────────┐
             │                │                │
        Featured (3)    Additional (6)    (see below)
```

---

## Page-by-Page Content Hierarchy

| Page | Above the fold | Below the fold | Primary job |
|---|---|---|---|
| **Home** | Editorial hero: headline + metrics stacked right | Benioff pull quote, 3 featured work cards | 30-second commercial — "This person operates at enterprise scale" |
| **About** | Bio summary | Visual career timeline, How I Work section, team photos | Trust the resume claims |
| **Impact Stories** | 3 featured story cards (alternating layout) | 6-card grid (second tier stories) | Deep proof of delivery |
| **Personal** | 5 photo sections | Horses, Community, Faith, Family, Outdoors | Culture / EQ calibration |

---

## Story Sub-Pages

All 9 live at `stories/[name].html`. Accessed from Impact Stories cards via "Read the story →" link. Not in primary nav.

### Featured (linked from Impact Stories top section)
| Story | File | Company |
|---|---|---|
| Help.Salesforce.com | `stories/help-salesforce.html` | Salesforce |
| Command Center | `stories/command-center.html` | Salesforce |
| Creating BNSF's Digital Customer Experience | `stories/bnsf-digital-cx.html` | BNSF |

### Additional (linked from Impact Stories grid)
| Story | File | Company |
|---|---|---|
| Trackathon | `stories/trackathon.html` | BNSF |
| Rail Recovery Turnaround | `stories/rail-recovery.html` | BNSF |
| BNSF DEX Transformation | `stories/bnsf-dex.html` | BNSF |
| Transforming Experience Design | `stories/xd-transformation.html` | BNSF |
| Account Status | `stories/account-status.html` | TBD |
| HFREI Reduction | `stories/hfrei-reduction.html` | BNSF |

---

## User Journey Mapping

- **SVP / executive scan (60 sec):** Home → skims metrics + pull quote → leaves with "this person is real"
- **Recruiter deep-dive:** Home → About → Impact Stories → 1-2 story sub-pages
- **Hiring manager:** Home → About → Impact Stories → all stories → Personal

---

## Navigation Pattern

- **Any page:** Sticky nav — Amanda Cornett Harris (name, left) + Home · About · Impact Stories · Personal (links, right)
- **Homepage card:** → `impact-stories.html` (with optional anchor to card)
- **Impact Stories card "Read the story →":** → `stories/[name].html`
- **Story sub-page back link:** → `../impact-stories.html`
- **Story sub-page prev/next:** sequential navigation through all 9 stories

---

## Implementation Notes

1. **No mobile hamburger menu** — nav links visible in header at all sizes
2. **No Vault page, no Admin page** — removed from architecture
3. **Footer identical on all pages:** disclaimer + "Connect" label + email + LinkedIn SVG icon
4. **Dates removed from all story cards** — per Amanda's request
5. **All story sub-pages use relative paths:** `../index.html`, `../impact-stories.html`, `../images/`, `../docs/`
