# Changelog — Amanda Cornett Harris Portfolio Site

---

## 6/17/2026 — Session 3 (Hero Film + Testimonials + Floating Cards)

### index.html (Home)
- **Hero brand film** replaces old hero text + construction banner
- 7-scene animated narrative (~90 seconds): The Problem → The Pattern → The Journey → The Next Transformation → Your AI Story → The Evidence → The Close
- AI transformation positioning: "Helping organizations turn AI potential into business outcomes"
- Pause/play + replay controls, keyboard (Space/Escape), WCAG compliant
- Reduced motion fallback shows static brand summary
- Construction banner removed
- Bottom "Let's Connect" button removed

### about.html (About)
- Career Path timeline card removed
- Education & Certifications card removed
- **Testimonials carousel** added: glass cards on blue gradient, 10s auto-advance, pause on hover, swipe on mobile, blue dot indicators
- 5 placeholder testimonials (quote + name + title + avatar)

### impact-stories.html (Impact Stories)
- **Floating card shadows** applied: 3-layer depth (close/medium/far) + inset glass highlight
- Hover lift increased to 8px with deeper shadow spread
- Header CTA centered below name (was absolutely positioned right)

### personal.html (Personal)
- **Floating card shadows** applied to placeholder card
- Header CTA centered below name

### All Pages
- Header CTA repositioned: centered below name using flex-direction:column (was position:absolute right)
- Header CTA hover: background/border/shadow change only, no vertical movement
- Floating card shadows now the design system standard for all cards

### DESIGN-SYSTEM.md
- Floating card shadow spec documented
- Hero brand film component documented
- Testimonials carousel component documented
- Header CTA centered layout documented

---

## 6/15/2026 — Session 2 (Glass Design System)

### All Pages — Glass Design System v2.0
- Glass design system introduced (Option 2 Plus)
- Glass header chrome: gradient + frosted orb accents
- "Let's Connect" CTA: glass button, border-radius 4px, drop shadow
- Glass nav bar: backdrop-filter blur(20px) saturate(180%)
- Glass footer: rgba(30,42,58,0.92) + backdrop-filter blur(20px)
- Page background standardized to #F4F5F7
- Mobile bottom tab bar on all pages
- Hamburger/overlay nav removed from about + personal
- Tagline removed from all pages

### index.html
- Glass header, nav, CTA, footer applied
- Construction banner converted to glass banner spec
- Meta description updated

### about.html
- Rebuilt with glass bio cards + timeline
- Glass header, nav, CTA, footer applied

### impact-stories.html
- Cards converted to glass card spec
- Glass metrics strip, tag badges, card buttons
- Sticky nav glass treatment

### personal.html
- Glass placeholder card
- Glass header, nav, CTA, footer applied

---

## 6/9/2026 — Session 1

### All Pages
- Header redesigned: centered name, LinkedIn CTA, gradient background
- Desktop nav: horizontal tabs, scroll-aware sticky nav
- Mobile nav: bottom tab bar, 4 icon tabs
- Footer: two disclaimer lines + copyright + email + LinkedIn
- Button system: 5 variants × 3 sizes × 4 states
- Motion design: IntersectionObserver entrance animations
- WCAG 2.0 AA compliance