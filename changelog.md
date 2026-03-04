# Changelog

> **Instructions for Claude Code:** All notable changes to this project are documented in this file. After completing any feature, bug fix, or significant change, append a new entry below following the format shown. Use the most recent date. Group changes under Added, Changed, Fixed, or Removed headers as applicable.

> **Format based on** [Keep a Changelog](https://keepachangelog.com/en/1.1.0/)

---

## [Unreleased]

### Planned
- Upload to Ionos hosting
- Replace gallery placeholders with real before/after photos
- Add Google Analytics tag (optional)

---

## 2026-03-04 — Initial Build

### Added

- **index.html**: Full 15-section home/landing page
  - Sticky top utility bar (hours + phone tel: link)
  - Responsive navbar with logo, nav links, red CTA "Call Now" button
  - Hero section — navy gradient, logo watermark, H1, 2 CTAs
  - About section — company history (est. 1978, Richmond VA), Class A/CIC credentials, stat boxes
  - "Why Clean Your HVAC" — 3 icon cards (Air Quality, Efficiency, Equipment Life)
  - Stats band — navy bg, 4 key numbers, energy savings CTA
  - Services grid (`#services`) — 8 service cards (AHUs, convectors, grilles, bathroom exhaust, dryer exhaust, range hoods, cooling towers, chillers)
  - Process steps — 4-step numbered flow with desktop connector lines
  - Gallery — 6 placeholder slots (3×2 grid) awaiting real photos
  - Problem spotlight — navy bg, mold/air quality risk bullets
  - Industries served — 4 industry cards (Industrial, Commercial, University, Government)
  - Certifications (`#certifications`) — ashrae.png, swam.png, CIC text badge, Class A text badge
  - Service area strip — red bg "Serving Richmond VA and All of Virginia"
  - Final CTA band — "Ready to Breathe Cleaner Air?" with call + contact buttons
  - Footer — 4-column: logo/brand, services list, industries + quick links, contact info
  - Files: `index.html`

- **contact.html**: Full 7-section contact page
  - Shorter hero (~40vh) — navy bg, "Contact Air Clean Corp"
  - 3 contact method cards — Phone (tel: link), Address, Hours
  - Team section — Norris Hicks (804-512-4547) + Ransom Hooks (804-300-7654) with avatar initials
  - Google Maps embed — 4909 W Clay Street, Richmond VA 23230
  - Service area chips — Richmond metro cities + "All of Virginia"
  - CTA strip — navy bg, large call button
  - Shared footer (same as index.html)
  - Files: `contact.html`

- **css/style.css**: Complete custom stylesheet
  - CSS custom properties (--acc-red, --acc-navy, --acc-white, etc.)
  - Typography (Roboto headings, Open Sans body)
  - All section styles: top bar, navbar, hero, about, why cards, stats band, service cards, process steps, gallery placeholders, problem section, industry cards, certifications, service area strip, CTA band, footer
  - Contact-page styles: contact hero, method cards, team cards, avatar circles, map, city chips
  - Responsive breakpoints: mobile (≤767px), tablet (≤991px)
  - Files: `css/style.css`

- **js/main.js**: Custom JavaScript
  - Navbar shadow on scroll (adds `.scrolled` class at 20px scroll depth)
  - Smooth scroll for all `href="#..."` anchor links with navbar offset
  - Mobile navbar auto-close on anchor link click
  - Active nav link highlighting based on scroll position
  - Files: `js/main.js`

- **Project documentation**:
  - `projectspec.md` — filled with project goals, tech stack, milestones, contact details
  - `architecture.md` — system overview, file reference guide, section maps, deployment instructions
  - `changelog.md` — this file

---

## Project Timeline Summary

| Date | Milestone | Status |
|------|-----------|--------|
| 2026-03-04 | Project initialized | ✅ Complete |
| 2026-03-04 | MVP — Static 2-page website | ✅ Complete |
| TBD | V1 — Real photos, SEO, analytics | 🔲 Not Started |
| TBD | Production — Deployed to aircleancorp.com | 🔲 Not Started |

---

## Session Log

### 2026-03-04 — Session 1

**What was worked on:**
Full initial build of the Air Clean Corp static website from scratch.

**What was accomplished:**
- Created all 4 project files: index.html, contact.html, css/style.css, js/main.js
- 15-section home page fully built and styled
- 7-section contact page fully built and styled
- Brand colors (red #C41E3A, navy #1B2A4A) applied consistently throughout
- All 4 image assets integrated (logo, icon, ashrae, swam)
- Responsive design with Bootstrap 5.3 grid
- All tel: links using 804-353-5150 (main), 804-512-4547 (Norris), 804-300-7654 (Ransom)
- Updated all 4 MD docs (projectspec, architecture, changelog, claude.md)

**Where we left off:**
MVP is complete. Site is ready to open in browser for review.

**Next steps:**
1. Open index.html in browser — verify all sections render
2. Open contact.html — verify all sections render
3. Test responsive at multiple widths
4. When ready: upload to Ionos hosting at aircleancorp.com

**Known issues or blockers:**
- Gallery section has 6 placeholder slots — needs real before/after photos from client
- Google Maps embed uses a placeholder src — should be verified/updated with correct embed URL from Google Maps
