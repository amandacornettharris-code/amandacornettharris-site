# Changelog — Amanda Cornett Harris Portfolio Site

---

## 6/15/2026 — Session 2 (Glass Design System)

### All Pages — Glass Design System v2.0

- **Glass design system introduced (Option 2 Plus):** Glass chrome on all pages + glass cards/carousels as the universal card pattern going forward. Every card and carousel added to the site must use the glass card spec documented in DESIGN-SYSTEM.md.
- **Glass header chrome:** Gradient header with frosted radial orb accents (white top-left, bronze bottom-right). Identical on all 4 pages.
- **"Let's Connect" CTA button:** Updated from pill (border-radius: 20px) to square-cornered glass button (border-radius: 4px) with frosted glass fill, white outline, and drop shadow. LinkedIn icon included. Absolutely positioned top-right in header on all pages.
- **Glass nav bar:** `backdrop-filter: blur(20px) saturate(180%)` on the nav strip. Active tab = white text + 2.5px white underline. No tagline on any page.
- **Glass footer:** All pages now use `rgba(30,42,58,0.92)` + `backdrop-filter: blur(20px)` footer. Both disclaimer lines present on all pages. Consistent `28px 40px` padding.
- **Page background:** Standardized to `#F4F5F7` on all 4 pages (was `#FFFFFF` on about and personal).
- **Mobile bottom tab bar:** All 4 pages now have identical bottom tab bar nav. Hamburger/overlay nav fully removed from about.html and personal.html.
- **Tagline:** Removed from all pages.
- **Entrance animations:** `IntersectionObserver` + 80ms setTimeout fallback. All pages.
- **WCAG 2.0 AA:** Skip links, ARIA labels, focus rings, landmarks maintained.
- **Design system reference:** Every HTML file includes a design system comment block at the top of the `<style>` section referencing DESIGN-SYSTEM.md v2.0 and the component being used.

---

### index.html (Home)

**Status:** ✅ Ready to deploy

**Changes:**
- Glass header, nav, CTA button, footer applied
- Construction banner converted to glass banner spec (gradient + backdrop-filter overlay)
- Meta description updated: "Customer Value, AI Transformation & Product and Design Strategy Executive"
- Construction banner date updated to 6/15/26
- Page background: `#F4F5F7`
- All entrance animations retained

---

### about.html (About)

**Status:** ✅ Ready to deploy

**Changes:**
- Glass header, nav, CTA button, footer applied
- Hamburger/overlay nav removed
- Bottom tab bar added
- Content restructured into 3 glass bio cards (Summary, Career Path, Education & Certifications)
- Career path now uses a timeline component (dot + role + company + dates)
- Bronze eyebrow labels on each card section
- Page background: `#F4F5F7`

---

### impact-stories.html (Impact Stories)

**Status:** ✅ Ready to deploy

**Changes:**
- Glass header, nav, CTA button, footer applied
- Impact story cards converted to glass card spec:
  - `background: rgba(255,255,255,0.55)` + `backdrop-filter: blur(20px) saturate(140%)`
  - `border: 1px solid rgba(255,255,255,0.75)`
  - `box-shadow: 0 4px 24px rgba(30,42,58,0.08), inset 0 1px 0 rgba(255,255,255,0.85)`
  - Hover: `translateY(-5px)` + deeper shadow
- Tag badges converted to glass spec (frosted white background)
- Metrics strip converted to glass spec (blue-tinted blur panel)
- "Read Story" button converted to glass card button spec
- Sticky nav retains glass blur treatment on scroll

---

### personal.html (Personal)

**Status:** 🚧 Placeholder — Ready to deploy

**Changes:**
- Glass header, nav, CTA button, footer applied
- Hamburger/overlay nav removed
- Bottom tab bar added
- Placeholder card converted to glass card spec
- Page background: `#F4F5F7`

---

### DESIGN-SYSTEM.md

**Status:** ✅ Updated to v2.0

**Changes:**
- Full glass component spec added for all 8 glass components:
  1. Glass Card (universal card/carousel spec)
  2. Glass Header CTA Button
  3. Glass Nav Bar
  4. Glass Sticky Nav
  5. Glass Construction/Promo Banner
  6. Glass Metrics Strip
  7. Glass Card CTA Button
  8. Glass Tag Badge
  9. Glass Footer
- Typography table updated with new sizes
- About page bio card and timeline specs added
- Motion design specs updated
- Page backgrounds section added
- Changelog section added to document

---

### CHANGELOG.md

**Status:** ✅ Updated (this file)

**Changes:**
- Session 2 entry added covering all 6/15 changes
- Pending items updated

---

### README.md

**Status:** ✅ Updated

**Changes:**
- Design system version updated to v2.0
- Page status table updated
- Glass design system noted in Tech Stack

---

## Pending Items (Next Session)

### Design
- [ ] Testimonial carousel (glass carousel spec — see DESIGN-SYSTEM.md)
- [ ] Impact stats / metric strip section on homepage
- [ ] Professional headshot (homepage + about)
- [ ] Personal page content (horses, community, faith, family, outdoors)
- [ ] Scroll animations and motion refinements

### Content
- [ ] Hero images for impact story cards (`images/agentforce-hero.jpg`, `images/xd-team-hero.jpg`, `images/customer-cx-hero.jpg`)
- [ ] Testimonial quotes with names, titles, photos
- [ ] Personal page photography

### Technical
- [ ] Admin panel / CMS for content management
- [ ] Page add/delete capability

---

## 6/9/2026 — Session 1

### All Pages

- **Header redesigned**: Centered name, "Let's Connect" LinkedIn CTA, gradient background. Tagline removed.
- **Desktop nav**: Horizontal tabs. Scroll-aware sticky nav. Active tab = white text + underline.
- **Mobile nav**: Bottom tab bar replaces hamburger. 4 icon tabs. Active in cobalt blue.
- **Footer**: Two disclaimer lines + copyright + email + LinkedIn.
- **Button system**: 5 variants × 3 sizes × 4 states. 4px radius, 250ms cubic-bezier transitions.
- **Motion design**: IntersectionObserver entrance animations, staggered timing.
- **WCAG 2.0 AA**: Contrast verified, skip links, focus rings, ARIA labels, landmarks.

### index.html
- Hero headline, three body paragraphs, construction banner, Let's Connect CTA.

### impact-stories.html
- 3 impact story cards with expand/collapse, metrics strips, tag badges, hero gradients.

### about.html
- Executive summary, career path, education, certifications.

### personal.html
- Placeholder: "Coming soon — horses, community, faith, family, outdoors."