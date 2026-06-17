# Design System — Amanda Cornett Harris
## Version 2.0 — Glass Design System
### Last updated: June 15, 2026

---

## Brand Personality

**Tagline:** "Transformation in Motion"

The site communicates "here is what happens when I'm in the room." Every pixel feels like forward momentum. Elements arrive — they don't just appear. The site itself is evidence of the superpower: taking complexity and making it feel effortless.

**Emotional arc for visitors:**
1. **Land** → "This person is serious and sophisticated"
2. **Scroll** → "These numbers are real — this is enterprise scale"
3. **Explore** → "She doesn't just talk about transformation, she shows it"
4. **Leave** → "I need to talk to her"

---

## Glass Design System — v2.0 Overview

**Option 2 Plus:** Glass chrome (header, nav, CTA, footer) + glass cards and carousels. Page body text stays clean and readable on `#F4F5F7`.

### Rule: Every card and carousel built going forward gets the glass card spec. No exceptions.

---

## Color Palette

### Primary
| Name       | Hex       | Usage                                         |
|------------|-----------|-----------------------------------------------|
| Blue       | `#1753C5` | Primary brand, CTAs, active states, headlines |
| Blue Hover | `#1E5FD9` | Button hover states                           |
| Blue Dark  | `#0F3D94` | Button pressed states, deep accents           |
| Blue Light | `#E8F0FE` | Tint backgrounds, mobile nav active bg        |

### Accent
| Name           | Hex       | Usage                                              |
|----------------|-----------|----------------------------------------------------|
| Bronze         | `#9A6E3A` | Decorative accents, dividers, eyebrows, focus rings|
| Bronze on Blue | `#E8C89D` | Text on blue backgrounds (4.6:1 contrast)          |
| Bronze Hover   | `#B07D45` | Bronze button hover                                |

### Neutrals
| Name         | Hex       | Usage                                    |
|--------------|-----------|------------------------------------------|
| Charcoal     | `#1E2A3A` | Primary text, footer background          |
| Charcoal Mid | `#3D4F63` | Secondary text, descriptions, card body  |
| White        | `#FFFFFF` | Card backgrounds, mobile nav             |
| Page Gray    | `#F4F5F7` | Page background on all pages             |
| Gray Icon    | `#8A95A5` | Mobile nav icons (inactive)              |
| Gray Icon Tx | `#6B7685` | Mobile nav labels (inactive)             |
| Footer Muted | `#7A8A9E` | Footer disclaimer text                   |
| Footer Text  | `#8A9AB0` | Footer copyright + links                 |
| Footer Sep   | `#3D506E` | Footer link separator                    |
| Disabled     | `#C4CDD6` | Inactive button text                     |
| Disabled Bg  | `#EDF0F3` | Inactive button fill                     |

### Header Gradient
```css
background: linear-gradient(135deg, #0F2A5E 0%, #1753C5 45%, #2E6DE8 100%);
```

---

## Glass Component Specifications

### Glass Card (cards + carousels)
Every card and carousel on the site uses this exact spec. Cards float above the page with layered shadows that create real depth perception.

```css
background: rgba(255,255,255,0.55);
backdrop-filter: blur(20px) saturate(140%);
-webkit-backdrop-filter: blur(20px) saturate(140%);
border: 1px solid rgba(255,255,255,0.75);
border-radius: 10px;
box-shadow:
  0 1px 2px rgba(30,42,58,0.04),
  0 4px 12px rgba(30,42,58,0.06),
  0 12px 36px rgba(30,42,58,0.1),
  inset 0 1px 0 rgba(255,255,255,0.85);
transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
```

**Hover state:**
```css
box-shadow:
  0 2px 4px rgba(30,42,58,0.04),
  0 8px 24px rgba(30,42,58,0.08),
  0 24px 64px rgba(30,42,58,0.16),
  inset 0 1px 0 rgba(255,255,255,0.9);
transform: translateY(-8px);
```

### Glass Header CTA Button ("Let's Connect")
Centered below name using `flex-direction: column` with `gap: 14px`. No absolute positioning.

```css
display: inline-flex;
align-items: center;
gap: 7px;
font-size: 12px;
font-weight: 600;
color: rgba(255,255,255,0.9);
background: rgba(255,255,255,0.12);
backdrop-filter: blur(16px) saturate(200%);
-webkit-backdrop-filter: blur(16px) saturate(200%);
border: 1px solid rgba(255,255,255,0.25);
border-radius: 4px;
padding: 8px 20px;
letter-spacing: 0.3px;
text-transform: uppercase;
box-shadow: inset 0 1px 0 rgba(255,255,255,0.2), 0 2px 8px rgba(0,0,0,0.2);
```

**Hover state (no vertical movement):**
```css
background: rgba(255,255,255,0.2);
border-color: rgba(255,255,255,0.4);
box-shadow: inset 0 1px 0 rgba(255,255,255,0.25), 0 4px 16px rgba(0,0,0,0.25);
```

### Glass Nav Bar
```css
background: rgba(255,255,255,0.08);
backdrop-filter: blur(20px) saturate(180%);
-webkit-backdrop-filter: blur(20px) saturate(180%);
border-top: 1px solid rgba(255,255,255,0.13);
```

**Active tab:**
```css
color: #fff;
font-weight: 700;
border-bottom: 2.5px solid #fff;
```

### Glass Sticky Nav (impact-stories.html only)
```css
background: rgba(15,42,94,0.88);
backdrop-filter: blur(24px) saturate(180%);
-webkit-backdrop-filter: blur(24px) saturate(180%);
border-bottom: 1px solid rgba(255,255,255,0.1);
box-shadow: 0 4px 24px rgba(0,0,0,0.2);
```

### Glass Construction Banner / Promo Banner
```css
background: linear-gradient(135deg, rgba(15,42,94,0.88) 0%, rgba(23,83,197,0.88) 45%, rgba(46,109,232,0.88) 100%);
backdrop-filter: blur(24px) saturate(160%);
-webkit-backdrop-filter: blur(24px) saturate(160%);
border: 1px solid rgba(255,255,255,0.2);
border-radius: 10px;
box-shadow: inset 0 1px 0 rgba(255,255,255,0.15), 0 8px 32px rgba(23,83,197,0.2);
```
Top shimmer line:
```css
::before {
  content: '';
  position: absolute; top: 0; left: 0; right: 0; height: 1px;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
}
```

### Glass Metrics Strip (inside cards)
```css
background: rgba(23,83,197,0.05);
backdrop-filter: blur(8px);
-webkit-backdrop-filter: blur(8px);
border: 1px solid rgba(23,83,197,0.12);
border-radius: 6px;
```
Column separator: `border-right: 1px solid rgba(23,83,197,0.1)`

**Value:** `font-size: 17px; font-weight: 800; color: #1753C5`
**Label:** `font-size: 9px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.07em; color: #3D4F63`

### Glass Card CTA Button (inside cards)
```css
background: rgba(23,83,197,0.07);
backdrop-filter: blur(8px);
-webkit-backdrop-filter: blur(8px);
border: 1.5px solid rgba(23,83,197,0.2);
border-radius: 4px;
padding: 11px 24px;
font-size: 12px;
font-weight: 700;
color: #1753C5;
text-transform: uppercase;
letter-spacing: 0.08em;
```

**Hover:**
```css
color: #fff;
background: #1753C5;
border-color: #1753C5;
box-shadow: 0 6px 20px rgba(23,83,197,0.2);
transform: translateY(-2px);
```

### Glass Tag Badge (inside card hero images)
```css
background: rgba(255,255,255,0.92);
backdrop-filter: blur(8px);
-webkit-backdrop-filter: blur(8px);
border-radius: 4px;
padding: 4px 10px;
font-size: 10px;
font-weight: 700;
color: #1753C5;
letter-spacing: 0.12em;
text-transform: uppercase;
```

### Glass Footer
```css
background: rgba(30,42,58,0.92);
backdrop-filter: blur(20px);
-webkit-backdrop-filter: blur(20px);
border-top: 1px solid rgba(255,255,255,0.07);
padding: 28px 40px;
```

---

## Typography

**Font Family:** `'Inter', -apple-system, system-ui, sans-serif`

| Element              | Size                   | Weight | Color          | Spacing  |
|----------------------|------------------------|--------|----------------|----------|
| Page name (header)   | clamp(24px, 4vw, 36px) | 800    | White          | -0.01em  |
| Hero headline        | clamp(30px, 5vw, 52px) | 800    | Charcoal       | -0.02em  |
| Page title           | clamp(26px, 4vw, 38px) | 800    | Charcoal       | -0.02em  |
| Card headline        | 19px (26px expanded)   | 800    | Charcoal       | -0.01em  |
| Section head         | 18–21px                | 800    | Charcoal       | -0.01em  |
| Body text            | 17–18px                | 400    | Charcoal Mid   | normal   |
| Card body            | 14px                   | 400    | Charcoal Mid   | normal   |
| Card section body    | 15px                   | 400    | Charcoal Mid   | normal   |
| Nav items            | 12px                   | 600/700| White variants | 0.1em    |
| Tag labels / eyebrow | 10–11px                | 700    | Bronze / Blue  | 0.1em+   |
| Metrics value        | 17px                   | 800    | Blue           | -0.02em  |
| Metrics label        | 9px                    | 600    | Charcoal Mid   | 0.07em   |
| Footer disclaimer    | 11px                   | 400    | #7A8A9E        | normal   |
| Footer copy / links  | 12px                   | 400    | #8A9AB0        | 0.04em   |

---

## Buttons

### Variants
- **Primary** — Solid blue fill. Main page CTA. One per visible section.
- **Secondary** — Outlined blue. Supporting actions. Fills on hover.
- **Bronze** — Warm accent. Use sparingly.
- **Dark** — Charcoal fill. Executive weight on light backgrounds.
- **Ghost** — Transparent. Tertiary actions.
- **Header CTA** — Glass spec above. LinkedIn "Let's Connect." Fixed top-right in header.
- **Glass Card Button** — Glass spec above. Inside impact cards and carousels.

### Sizes
| Size   | Font  | Padding   | Use                   |
|--------|-------|-----------|-----------------------|
| Small  | 11px  | 8px 18px  | Tags, compact actions |
| Medium | 13px  | 14px 36px | Standard actions      |
| Large  | 14px  | 18px 48px | Hero CTAs             |

### Shared Specs
- Border radius: `4px`
- Font weight: `700`
- Text transform: `uppercase`
- Letter spacing: `0.08–0.12em`
- Transition: `250ms cubic-bezier(0.4, 0, 0.2, 1)`

### States
| State    | Behavior                                                     |
|----------|--------------------------------------------------------------|
| Default  | Base colors, shadow                                          |
| Hover    | Lifts 2px, shadow deepens, color brightens                   |
| Active   | Returns to baseline, shadow tightens, color darkens          |
| Inactive | `#EDF0F3` fill, `#C4CDD6` text, `cursor: not-allowed`        |
| Focus    | `3px solid var(--bronze)` outline, `3px` offset              |

---

## Page Chrome (identical on every page)

### Header Structure
```
┌───────────────────────────────────────────────────────────────┐
│  (gradient + frosted orb accents)                             │
│                   Amanda Cornett Harris      [Let's Connect]  │
├───────────────────────────────────────────────────────────────┤
│   (glass nav bar)  Home  About  Impact Stories  Personal      │
└───────────────────────────────────────────────────────────────┘
```
- Name: centered, `clamp(24px–36px)`, weight 800, white
- No tagline
- "Let's Connect" pill: absolutely positioned right, glass spec above
- Nav bar: glass spec above, active = white + 2.5px white underline

### Header Orb Accents (identical on all pages)
```css
/* Light orb top-left */
::before { top: -80px; left: -80px; width: 360px; height: 360px;
  background: radial-gradient(circle, rgba(255,255,255,0.06) 0%, transparent 70%); }
/* Bronze orb bottom-right */
::after { bottom: -60px; right: -60px; width: 280px; height: 280px;
  background: radial-gradient(circle, rgba(232,200,157,0.07) 0%, transparent 70%); }
```

### Bronze Accent Bar (below page title)
```css
width: 44–52px; height: 3px; background: #9A6E3A; border-radius: 2px;
```

### Footer Structure (identical on all pages)
```
┌────────────────────────────────────────────────────────────┐
│  All work examples shown are accessible via public domain  │
│  or are summative communications and do not compromise     │
│  protected company IP.                                     │
│                                                            │
│  This site is actively under construction in               │
│  collaboration with Claude.                                │
├────────────────────────────────────────────────────────────┤
│  © 2026 Amanda Cornett Harris    email | LinkedIn ↗        │
└────────────────────────────────────────────────────────────┘
```
Uses glass footer spec. Both disclaimer lines on every page.

### Mobile Bottom Nav (identical on all pages)
```css
/* Bar */
background: #FFFFFF;
border-top: 1px solid #E2E6EB;
box-shadow: 0 -2px 16px rgba(0,0,0,0.06);
padding: 6px 0 calc(6px + env(safe-area-inset-bottom));

/* Inactive icon */
stroke: #8A95A5;

/* Active icon */
stroke: #1753C5;

/* Active label */
color: #1753C5; font-weight: 700;
```

Tabs: Home (house) · About (person) · Impact (lightning bolt) · Personal (heart)

---

---

## Hero Brand Film (index.html)

7-scene animated narrative (~90 seconds) that auto-plays on page load.

### Scenes
1. **The Problem** — Line fracture, chaos words, glass card with failures
2. **The Pattern** — Blue light, connecting lines, "Few connect all three"
3. **The Journey** — Railroad → Supply Chain → Industrial Operations → Enterprise Software
4. **The Next Transformation** — AI as organizational transformation, not technology
5. **Your AI Story** — Agentforce, Customer 0, Agentic Service, Command Center, etc.
6. **The Evidence** — Metrics animate in (2.2M+, 82%, $100M+, 584K+, 2.8B+)
7. **The Close** — Name, pillars, values, impact line

### Controls
- Pause/play button (bottom-right)
- Replay button (bottom-right)
- Keyboard: Space = pause/play, Escape = replay
- Auto-pauses on prefers-reduced-motion; shows static fallback

### Film Container
```css
background: linear-gradient(135deg, #0F2A5E 0%, #1753C5 45%, #2E6DE8 100%);
min-height: 70vh;
/* Same frosted orb accents as header */
```

### Scene Transitions
```css
transition: opacity 1s ease;
```

### Impact Line (Scene 7 final)
```css
font-size: clamp(22px, 3.5vw, 32px);
font-weight: 800;
color: #fff;
letter-spacing: -0.02em;
transition: opacity 1s ease;
```

---

## Testimonials Carousel (about.html)

Glass cards on blue gradient wrapper. 10-second auto-advance.

### Section Wrapper
Uses the same Glass Banner spec as construction banner:
```css
background: linear-gradient(135deg, rgba(15,42,94,0.88) 0%, rgba(23,83,197,0.88) 45%, rgba(46,109,232,0.88) 100%);
backdrop-filter: blur(24px) saturate(160%);
border: 1px solid rgba(255,255,255,0.2);
border-radius: 10px;
```

### Cards Inside Carousel (dark bg variant)
```css
background: rgba(255,255,255,0.1);
backdrop-filter: blur(20px) saturate(140%);
border: 1px solid rgba(255,255,255,0.2);
border-radius: 10px;
box-shadow: 0 4px 24px rgba(0,0,0,0.15), inset 0 1px 0 rgba(255,255,255,0.15);
```

### Dot Indicators
- Inactive: `background: rgba(255,255,255,0.3); width: 8px; height: 8px; border-radius: 50%`
- Active: `background: #fff; transform: scale(1.3)`

### Arrow Buttons
Glass spec matching header CTA, white chevrons, 36px circles.

### Quote Typography
- Quote mark: 64px Georgia, white at 20% opacity
- Quote text: 17px, weight 400, italic, white at 92% opacity
- Name: 15px, weight 700, white
- Title: 13px, white at 70% opacity

### Behavior
- 10-second auto-advance
- Pauses on hover
- Touch/swipe on mobile (40px threshold)
- Dots are clickable, arrows advance manually

### Adding/Removing Testimonials
Copy or delete a `<div class="t-card">...</div>` block. Update `aria-label` counts. Dots regenerate automatically.

### Adding Photos
Replace initials avatar with: `<img class="t-avatar" src="images/name.jpg" alt="Name" style="object-fit:cover"/>`

---

## Impact Story Cards

### Structure
1. **Hero area** (196px height) — gradient background + image with `onerror` hide
2. **Glass tag badge** — top-left of hero, glass spec above
3. **Card headline** — 19px, weight 800, charcoal
4. **Summary** — 14px, charcoal mid
5. **Glass metrics strip** — 3-column, glass spec above
6. **Glass card CTA button** — "Read Story →", glass spec above
7. **Expanded sections** — hidden, revealed on "Read Story" click

### Card Hero Gradients
| Story             | Gradient                              |
|-------------------|---------------------------------------|
| Agentforce / AI   | `#4338CA → #7C3AED` (purple)          |
| BNSF XD Team      | `#0D6B3E → #22C55E` (green)           |
| BNSF Digital CX   | `#1E3A5F → #2E6DE8` (blue)            |

### Card Grid
```css
grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
gap: 28px;
```

Expanded card: `grid-column: 1 / -1`

---

## About Page Cards

Bio sections use the glass card spec with this internal structure:
```css
.about-card { padding: 28px 32px; margin-bottom: 20px; }
.eyebrow { font-size: 11px; font-weight: 700; letter-spacing: 1px;
           text-transform: uppercase; color: #9A6E3A; margin-bottom: 8px; }
```

Timeline dots:
```css
width: 10px; height: 10px; border-radius: 50%; background: #1753C5;
box-shadow: 0 0 0 3px rgba(23,83,197,0.15);
```

---

## Motion Design

### Philosophy
- Nothing instant. Everything eases.
- Elements arrive — they don't just appear.
- The site itself is evidence of the superpower.

### Entrance Animations
```css
/* Default */
.anim { opacity: 0; transform: translateY(24px);
        transition: opacity 0.6s ease, transform 0.6s ease; }
.anim.visible { opacity: 1; transform: translateY(0); }

/* Bronze line scale */
.anim-scale { opacity: 0; transform: scaleX(0); transform-origin: left;
              transition: opacity 0.5s ease, transform 0.5s ease; }
.anim-scale.visible { opacity: 1; transform: scaleX(1); }
```

Triggered via `IntersectionObserver` + 80ms `setTimeout` fallback for above-fold elements.
Stagger: 150–200ms between sequential elements via `transition-delay`.

### Hover Transitions
| Element     | Duration | Easing                          |
|-------------|----------|---------------------------------|
| Buttons     | 250ms    | `cubic-bezier(0.4, 0, 0.2, 1)` |
| Cards       | 350ms    | `cubic-bezier(0.4, 0, 0.2, 1)` |
| Card images | 600ms    | `cubic-bezier(0.4, 0, 0.2, 1)` |
| Nav links   | 250ms    | `ease`                          |

### Scroll-Aware Sticky Nav (impact-stories.html)
- Scroll down past header → nav hides (`translateY(-100%)`)
- Scroll up → nav slides back (`translateY(0)`)
- Transition: `350ms ease`
- Sticky style uses glass sticky nav spec above

---

## Accessibility (WCAG 2.0 AA)

- All text meets minimum 4.5:1 contrast ratio
- Skip-to-main-content link on every page
- Focus rings: `3px solid var(--bronze)`, `3px offset` (bronze-on-blue in header)
- `aria-current="page"` on active nav items (desktop + mobile)
- `aria-label` on all icon-only links and external links
- `aria-expanded` on expandable card buttons
- `role="banner"`, `role="main"`, `role="contentinfo"` on every page
- All images have `alt` text or `onerror` fallback

---

## Page Backgrounds

| Page           | Background  |
|----------------|-------------|
| All pages      | `#F4F5F7`   |

No page uses `#FFFFFF` as the page background. White is reserved for card surfaces only.

---

## File Structure

```
amandacornettharris-site/
├── index.html             (Home)
├── about.html             (About — glass bio cards + timeline)
├── impact-stories.html    (Impact Stories — glass cards + sticky nav)
├── personal.html          (Personal — glass placeholder card)
├── images/
│   ├── agentforce-hero.jpg
│   ├── xd-team-hero.jpg
│   └── customer-cx-hero.jpg
├── DESIGN-SYSTEM.md       (this file)
├── CHANGELOG.md
└── README.md
```

---

## Changelog

### v2.1 — June 17, 2026
- Hero brand film added to homepage (7 scenes, ~90 seconds)
- Testimonials carousel added to about page (glass cards on blue gradient)
- Floating card shadows: 3-layer depth replaces single shadow
- Header CTA centered below name (was absolutely positioned right)
- Header CTA hover: no vertical movement
- Career Path and Credentials cards removed from about
- Construction banner and bottom CTA removed from home
- Scene 7 final line: "Helping organizations turn AI potential into business outcomes" in impact font

### v2.0 — June 15, 2026
- Introduced glass design system (Option 2 Plus)
- Glass chrome: header, CTA button, nav bar, footer on all pages
- Glass cards: all impact story cards, about bio cards, personal placeholder
- Glass metrics strip inside cards
- Glass card CTA buttons
- Glass construction banner on Home
- About page rebuilt with glass bio cards + career timeline
- Removed tagline from all pages
- Standardized page background to `#F4F5F7` everywhere
- Standardized footer (both disclaimer lines on all pages, consistent padding)
- Removed hamburger/overlay nav from about.html and personal.html
- Added bottom tab bar mobile nav to all pages
- Updated headline: "Customer Value · AI Transformation · Product & Design Strategy"

### v1.0 — June 2026
- Initial design system
- Flat white cards
- Gradient header (no glass)
- Bottom tab bar on home + impact only