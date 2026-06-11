# Design System — Amanda Cornett Harris

## Brand Personality

**Tagline:** "Transformation in Motion"

The site communicates "here is what happens when I'm in the room." Every pixel feels like forward momentum. Elements arrive — they don't just appear. The site itself is evidence of the superpower: taking complexity and making it feel effortless.

**Emotional arc for visitors:**
1. **Land** → "This person is serious and sophisticated"
2. **Scroll** → "These numbers are real — this is enterprise scale"
3. **Explore** → "She doesn't just talk about transformation, she shows it"
4. **Leave** → "I need to talk to her"

---

## Color Palette

### Primary
| Name | Hex | Usage |
|------|-----|-------|
| Blue | `#1753C5` | Primary brand, CTAs, active states, headlines |
| Blue Hover | `#1E5FD9` | Button hover states |
| Blue Dark | `#0F3D94` | Button pressed states, deep accents |
| Blue Light | `#E8F0FE` | Backgrounds, nav borders |

### Accent
| Name | Hex | Usage |
|------|-----|-------|
| Bronze | `#9A6E3A` | Decorative accents, dividers, focus rings |
| Bronze on Blue | `#E8C89D` | Tagline text on blue backgrounds (4.6:1 contrast) |
| Bronze Hover | `#B07D45` | Bronze button hover |

### Neutrals
| Name | Hex | Usage |
|------|-----|-------|
| Charcoal | `#1E2A3A` | Primary text, dark backgrounds |
| Charcoal Mid | `#3D4F63` | Secondary text, descriptions |
| Footer Text | `#B0BFD0` | Footer links, muted text on dark |
| White | `#FFFFFF` | Page background, card backgrounds |
| Page Gray | `#F4F5F7` | Section backgrounds for card separation |
| Disabled | `#C4CDD6` | Inactive button text |
| Disabled Bg | `#EDF0F3` | Inactive button fill |

### Header Gradient
```css
background: linear-gradient(135deg, #0F2A5E 0%, #1753C5 45%, #2E6DE8 100%);
```

---

## Typography

**Font Family:** `'Inter', -apple-system, system-ui, sans-serif`

| Element | Size | Weight | Color | Spacing |
|---------|------|--------|-------|---------|
| Page name (header) | clamp(24px, 4vw, 36px) | 800 | White | -0.01em |
| Header tagline | 12px | 600 | Bronze on Blue | 0.18em |
| Page title | clamp(28px, 4vw, 40px) | 800 | Charcoal | -0.02em |
| Hero headline | clamp(32px, 5vw, 54px) | 800 | Charcoal | -0.02em |
| Card headline | 20px | 800 | Charcoal | -0.01em |
| Body text | 18px | 400 | Charcoal Mid | normal |
| Card body | 14px | 400 | Charcoal Mid | normal |
| Button text | 11-14px | 700 | Varies | 0.08-0.12em |
| Nav items | 12px | 600/700 | White variants | 0.12em |
| Tag labels | 10-11px | 700 | Blue | 0.14em |
| Metrics value | 18px | 800 | Blue | -0.02em |
| Metrics label | 9px | 600 | Charcoal Mid | 0.08em |
| Footer text | 12-13px | 400 | Footer Text | 0.04em |

---

## Buttons

### Variants

**Primary** — Solid cobalt fill. Main CTA. One per visible section.
**Secondary** — Outlined. Fills on hover. Supporting actions.
**Bronze** — Warm accent. Use sparingly for emotional emphasis.
**Dark** — Charcoal fill. Executive weight on light backgrounds.
**Ghost** — Transparent. Tertiary actions, back links.
**Header CTA** — Frosted glass on blue header. LinkedIn "Let's Connect."

### Sizes

| Size | Font | Padding | Use |
|------|------|---------|-----|
| Small (sm) | 11-12px | 8px 18px | Tags, compact actions |
| Medium (md) | 13px | 14px 36px | Standard actions |
| Large (lg) | 14px | 18px 48px | Hero CTAs |

### States

| State | Behavior |
|-------|----------|
| Default | Base colors, 2px shadow (primary/bronze/dark) |
| Hover | Lifts 2px, shadow deepens, color brightens |
| Active/Press | Returns to baseline, shadow tightens, color darkens |
| Inactive | Gray fill `#EDF0F3`, gray text `#C4CDD6`, `cursor: not-allowed` |
| Focus | 3px bronze outline, 3px offset |

### Specs
- Border radius: `4px`
- Border: `2px solid`
- Font weight: `700`
- Text transform: `uppercase`
- Letter spacing: `0.08–0.12em`
- Transition: `250ms cubic-bezier(0.4, 0, 0.2, 1)`

---

## Impact Story Cards

### Structure
1. **Hero image** (200px height) — gradient fallback + image with `onerror` hide
2. **Tag badge** — frosted glass pill, top-left of hero
3. **Title** — 20px, weight 800
4. **Impact description** — 14px summary
5. **Metrics strip** — 3-column data bar with key stats
6. **CTA** — Secondary button with arrow icon

### Card States
| State | Behavior |
|-------|----------|
| Default | White background, subtle border + shadow, on `#F4F5F7` page |
| Hover | Lifts 6px, shadow deepens dramatically, image zooms 5%, gradient overlay fades in, metrics strip highlights |

### Specs
- Background: `#FFFFFF` on `#F4F5F7` page
- Border: `1px solid rgba(30,42,58,0.04)` + shadow
- Border radius: `8px`
- Grid: `repeat(auto-fill, minmax(340px, 1fr))` with 32px gap
- Image transition: `600ms cubic-bezier(0.4, 0, 0.2, 1)`
- Card transition: `400ms cubic-bezier(0.4, 0, 0.2, 1)`

### Metrics Strip
- 3 columns, bordered container with `border-radius: 6px`
- Value: 18px, weight 800, Blue
- Label: 9px, weight 600, uppercase, Charcoal Mid
- Background highlights to `#F8FAFD` on card hover

---

## Page Chrome

### Header
```
┌──────────────────────────────────────────────────────┐
│  Amanda Cornett Harris          [Let's Connect]  CTA │
│  ENTREPRENEURIAL BUILDER · ENTERPRISE OPERATOR...    │
├──────────────────────────────────────────────────────┤
│      Home    About    Impact Stories    Personal      │
└──────────────────────────────────────────────────────┘
```

- Background: Gradient `135deg` from `#0F2A5E` → `#1753C5` → `#2E6DE8`
- Name: left-aligned, white, weight 800
- Tagline: bronze on blue, uppercase, weight 600
- CTA: Header variant button (frosted glass), size small
- Nav bar: sits below on semi-transparent dark overlay
- Active nav: white text + white bottom border
- Hover nav: white text + faded bottom border

### Page Title
- Bronze bar: 48px × 3px, `border-radius: 2px`
- Title: clamp(28px–40px), weight 800, Charcoal
- Subtitle: 18px, Charcoal Mid, max-width 640px

### Footer
```
┌──────────────────────────────────────────────────────┐
│  All work examples shown are accessible via public   │
│  domain or are summative communications and do not   │
│  compromise protected company IP.                    │
│                                                      │
│  This site is actively under construction in         │
│  collaboration with Claude.                          │
├──────────────────────────────────────────────────────┤
│  © 2026 Amanda Cornett Harris    email | LinkedIn ↗  │
└──────────────────────────────────────────────────────┘
```

- Background: Charcoal `#1E2A3A`
- Disclaimers: 12px, italic, `#7A8A9E`
- Copyright: 13px, `#8A9AB0`
- Links: underlined, `#8A9AB0` → white on hover

---

## Motion Design

### Philosophy
- Nothing instant. Everything eases.
- Elements arrive — fade up, slide in, stagger.
- The site should feel like it's meeting the visitor.

### Entrance Animations
- Elements use `IntersectionObserver` to trigger `.visible` class
- Default: `opacity: 0; transform: translateY(24px)`
- Visible: `opacity: 1; transform: translateY(0)`
- Duration: `600ms ease`
- Stagger: 200ms between sequential elements

### Scroll-Aware Navigation
- Scroll down → nav slides up and disappears
- Scroll up → nav slides back with glass blur backdrop
- Transition: `350ms ease`
- Backdrop: `blur(20px) saturate(180%)`, `rgba(255,255,255,0.85)`

### Hover Transitions
- Buttons: `250ms cubic-bezier(0.4, 0, 0.2, 1)`
- Cards: `400ms cubic-bezier(0.4, 0, 0.2, 1)`
- Card images: `600ms cubic-bezier(0.4, 0, 0.2, 1)`
- Nav/links: `300ms ease`

---

## Accessibility (WCAG 2.0 AA)

- All text meets minimum 4.5:1 contrast ratio
- Bronze accent used only for decorative elements or text verified ≥ 4.5:1
- Skip-to-main-content link on every page
- Focus rings: 3px bronze outline, 3px offset
- `aria-current="page"` on active nav items
- `aria-label` on all links with external targets
- `aria-expanded` on expandable content
- `role="banner"`, `role="main"`, `role="contentinfo"` landmarks
- All images have `alt` text or `role="presentation"`
- Keyboard navigable throughout

---

## File Naming

| Asset | Filename |
|-------|----------|
| Agentforce hero | `images/agentforce-hero.jpg` |
| XD Team hero | `images/xd-team-hero.jpg` |
| Customer CX hero | `images/customer-cx-hero.jpg` |
| Homepage | `index.html` |
| About page | `about.html` |
| Impact Stories page | `impact-stories.html` |
| Personal page | `personal.html` |
