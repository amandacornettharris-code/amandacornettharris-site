# Changelog — Amanda Cornett Harris Portfolio Site

## 6/9/2026 — Session 1

### All Pages
- **Header redesigned**: Centered name, centered "Let's Connect" LinkedIn CTA (tier 3/small), gradient background (135deg: #0F2A5E → #1753C5 → #2E6DE8). Tagline removed.
- **Desktop nav**: Horizontal tabs in header bar. Scroll-aware sticky nav with glass blur on scroll. Active tab = white text + white underline. Hover = brightens + faded underline.
- **Mobile nav**: Persistent bottom tab bar replaces hamburger/drawer. 4 icon tabs (Home, About, Impact, Personal) in grayscale. Active tab in cobalt blue. Respects safe-area-inset-bottom.
- **Footer updated**: Two disclaimer lines added: (1) IP protection statement, (2) "Under construction in collaboration with Claude." Copyright + email + LinkedIn links below.
- **Button system created**: 5 variants (Primary, Secondary, Bronze, Dark, Ghost) × 3 sizes (sm, md, lg) × 4 states (default, hover, active, inactive). All buttons have 4px border radius, 2px border, 700 weight, uppercase, 250ms cubic-bezier transitions. Hover lifts 2px + shadow deepens. Active presses down. Focus = 3px bronze outline.
- **Motion design**: IntersectionObserver entrance animations on all content. Staggered fade-up timing. 600ms ease transitions.
- **WCAG 2.0 AA compliance**: All contrast ratios verified. Skip-to-content link. Focus rings. ARIA labels. Semantic landmarks.

---

### index.html (Home)
**Status:** ✅ Deployed

**Content:**
- Hero headline: "I specialize in turning bold ideas into operating realities."
- Three supporting paragraphs (Fortune 500 experience, cross-functional background, AI/transformation)
- Under construction banner (gradient card, bronze text): "This site is under construction in partnership with Claude. Please explore existing content and check back daily for updates. Updated 6/9/26"
- "Let's Connect" CTA linking to LinkedIn

**Changes this session:**
- [x] Gradient header with centered name
- [x] Tagline removed from header
- [x] "Let's Connect" CTA added to header (tier 3/small, frosted glass style)
- [x] Under construction banner text changed to bronze (#E8C89D)
- [x] Desktop scroll-aware sticky nav with glass blur
- [x] Mobile bottom tab bar (no hamburger)
- [x] New footer with disclaimers
- [x] Entrance animations on all content

---

### impact-stories.html (Impact Stories)
**Status:** ✅ Deployed

**Content:**
- Page title: "Impact Stories"
- Subtitle: "Real outcomes from real work — building businesses, transforming organizations, and connecting innovation to adoption."
- 3 impact story cards with expand/collapse

**Card 1 — Salesforce: 5 Key Mindset Shifts for Building Agentforce Experiences**
- Metrics: 82% Self-Service Resolution | 2.2M+ AI Interactions | 5 Days Concept to Launch
- 6 expandable sections (The Challenge, 5 Mindset Shifts)
- Hero: purple gradient (replace with images/agentforce-hero.jpg)

**Card 2 — BNSF: Transforming Experience Design**
- Metrics: 320+ Engagements | 67 NPS | ~$100M Patent Value
- 5 expandable sections (Origins, Operating Model, Impact, Enterprise, 2021 Focus)
- Hero: green gradient (replace with images/xd-team-hero.jpg)

**Card 3 — BNSF: Creating BNSF's Digital Customer Experience**
- Metrics: 94+ Apps Unified | 5-Year Funded Roadmap | $23B+ Revenue Supported
- 5 expandable sections (My Role, App Overload, Radical Alignment, Outcome, Learnings)
- Hero: blue gradient (replace with images/customer-cx-hero.jpg)

**Changes this session:**
- [x] New page chrome (gradient header, centered name, bottom nav)
- [x] Cards redesigned: 8px border-radius, metrics strip, tag badge, hover lift (6px), image zoom (5%)
- [x] Expand/collapse with smooth max-height animation
- [x] "Read Story →" secondary button with arrow icon
- [x] Cards on #F4F5F7 background for visual separation
- [x] New footer with disclaimers

---

### about.html (About)
**Status:** ✅ Deployed (old header pattern — needs update)

**Content:**
- Page title: "About Amanda"
- Executive summary (3 paragraphs from resume)
- Career path: Salesforce (2021–Present), BNSF Railway (2013–2021), US Lime & Minerals (2007–2011)
- Education: Texas A&M, BS Agricultural Development
- Certifications: Salesforce UX Designer (2022), CUA (2018)
- "Full Profile on LinkedIn" CTA

**Changes this session:**
- [x] Career items with blue company name highlights
- [x] Section headers at 22px weight 800
- [x] Entrance animations on all content
- [x] New footer with disclaimers

**TODO:**
- [ ] Update header to centered layout (remove tagline) — currently uses old solid-blue left-aligned header + hamburger menu
- [ ] Replace hamburger with bottom tab bar
- [ ] Add professional photo

---

### personal.html (Personal)
**Status:** 🚧 Placeholder (old header pattern — needs update)

**Content:**
- Page title: "Personal"
- Subtitle: "Accomplished leader. Real person."
- Icon graphic
- "This section is coming soon" message
- "Horses, community, faith, family, and the outdoors."

**Changes this session:**
- [x] Centered layout for body content
- [x] Entrance animations
- [x] New footer with disclaimers

**TODO:**
- [ ] Update header to centered layout (remove tagline) — currently uses old solid-blue left-aligned header + hamburger menu
- [ ] Replace hamburger with bottom tab bar
- [ ] Add personal content and photography
- [ ] Add community/faith/horses/outdoors sections

---

## Pending Items (Next Session)

### Design
- [ ] Apply centered header + bottom nav to about.html and personal.html
- [ ] Refine scroll-aware nav transitions
- [ ] Add testimonial carousel to homepage
- [ ] Design impact stats section for homepage

### Content
- [ ] Hero images for impact story cards (screenshots from PDFs)
- [ ] Professional headshot for homepage/about
- [ ] Personal page content (horses, community, faith, family, outdoors)
- [ ] Testimonial quotes with names, titles, photos

### Technical
- [ ] Admin panel for content management
- [ ] CMS for adding/editing/deleting impact stories
- [ ] Page add/delete capability
- [ ] Resume/PDF upload and link management

### Deployment
- [x] Connect GitHub repo to Netlify auto-deploy
- [ ] Set up custom domain (amandacornettharris.ai)
- [ ] Add hero images to /images/ folder
