# Architecture



## System Overview

**Project:** Air Clean Corp Website
**Type:** Static Website
**Architecture Style:** Pure static HTML/CSS/JS — no server, no build step

**One-paragraph summary:**
A 2-page static website for Air Clean Corp (aircleancorp.com). The site uses Bootstrap 5.3 via CDN, Bootstrap Icons, and Google Fonts. All styling lives in `css/style.css` and behavior in `js/main.js`. There is no backend, no form processing, and no database. The site is designed to be deployed by uploading the entire project folder to Ionos hosting.

---

## Data Flow

```
User opens browser → loads index.html or contact.html
→ Browser fetches CDN resources (Bootstrap, Icons, Fonts)
→ Browser fetches local css/style.css and js/main.js
→ Page renders → User clicks tel: link → phone call initiated
→ User clicks nav link → smooth scroll or page navigation
```

---

## Component Architecture

### Pages

| File | Purpose | Notes |
|------|---------|-------|
| `index.html` | Home / landing page | 15 sections |
| `contact.html` | Contact page | 7 sections, shares nav/footer with index |

### Assets

| File | Purpose |
|------|---------|
| `css/style.css` | All custom styles — brand colors, typography, layout, responsive |
| `js/main.js` | Navbar scroll shadow, smooth scroll, active link highlighting |
| `Image/acc_logo_transparent.png` | Primary logo — used in navbar, footer, hero watermark |
| `Image/transparent_icon.png` | Browser favicon |
| `Image/ashrae.png` | ASHRAE membership badge (certifications section) |
| `Image/swam.png` | SWaM certification badge (certifications section) |
| `Image/accLogo.png` | Alternate logo (available but not currently used) |

### External CDN Dependencies

| Resource | URL | Purpose |
|----------|-----|---------|
| Bootstrap 5.3 CSS | jsdelivr.net | UI framework |
| Bootstrap 5.3 JS | jsdelivr.net | Collapse, mobile nav |
| Bootstrap Icons 1.11 | jsdelivr.net | All icon usage |
| Google Fonts | fonts.googleapis.com | Roboto (headings) + Open Sans (body) |

---

## Directory Structure

```
AirCleanCorp/
├── index.html                  # Home page (15 sections)
├── contact.html                # Contact page (7 sections)
├── css/
│   └── style.css               # Custom branding & responsive styles
├── js/
│   └── main.js                 # Navbar scroll, smooth scroll, active links
├── Image/
│   ├── acc_logo_transparent.png # Primary transparent logo
│   ├── accLogo.png             # Alternate logo
│   ├── transparent_icon.png    # Favicon
│   ├── ashrae.png              # ASHRAE badge
│   └── swam.png                # SWaM certification badge
├── projectspec.md              # Product requirements and milestones
├── architecture.md             # This file
└── changelog.md                # Version history
```

---

## File Reference Guide

| File Path | What It Does | How to Run |
|-----------|-------------|------------|
| `index.html` | Home/landing page with hero, about, services, certifications, CTA | Open in browser |
| `contact.html` | Contact page with team, map, service area | Open in browser |
| `css/style.css` | All custom CSS — brand vars, section styles, responsive breakpoints | Loaded by HTML pages |
| `js/main.js` | Navbar scroll shadow, smooth scroll, active nav highlighting | Loaded by HTML pages |
| `Image/acc_logo_transparent.png` | Transparent PNG logo — navbar (200px), footer (160px), hero watermark | Referenced in HTML |
| `Image/transparent_icon.png` | Square icon for browser favicon | Referenced in `<link rel="icon">` |
| `Image/ashrae.png` | ASHRAE membership logo | Certifications section in index.html |
| `Image/swam.png` | Virginia SWaM certification logo | Certifications section in index.html |
| `architecture.md` | System design and file map (this file) | Reference |


---

## Deployment

**Platform:** Ionos (shared hosting)
**DNS:** Managed by Microtel Systems Corporation
**Domain:** aircleancorp.com



**No build step required** — upload files exactly as they are in this folder.

---

## index.html — Section Map

| # | Section | ID | Notes |
|---|---------|-----|-------|
| 1 | Top utility bar | — | Navy bg, phone + hours |
| 2 | Navbar | — | sticky-top, logo left, nav right |
| 3 | Hero | — | Navy gradient, watermark logo |
| 4 | About / Credibility | — | History, Class A, CIC, 45+ years |
| 5 | Why Clean Your HVAC | — | 3 icon cards |
| 6 | Stats band | — | Navy bg, key numbers |
| 7 | Services grid | `#services` | 8 service cards |
| 8 | Process steps | — | 4-step numbered process |
| 9 | Gallery | — | 6 placeholder slots |
| 10 | Problem spotlight | — | Navy bg, mold/air quality risks |
| 11 | Industries served | — | 4 industry cards |
| 12 | Certifications | `#certifications` | ASHRAE, SWaM, CIC, Class A |
| 13 | Service area strip | — | Red bg strip |
| 14 | Final CTA | — | Navy bg, call + contact buttons |
| 15 | Footer | — | 4-col: brand, services, industries, contact |

## contact.html — Section Map

| # | Section | Notes |
|---|---------|-------|
| 1 | Contact hero | ~40vh, navy bg |
| 2 | Contact method cards | Phone, address, hours |
| 3 | Team supervisors | Norris Hicks + Ransom Hooks |
| 4 | Google Maps embed | 4909 W Clay St |
| 5 | Service area chips | Richmond metro + all VA |
| 6 | CTA strip | Navy bg, call button |
| 7 | Footer | Same as index.html |

---

## Technical Decisions Log

| Date | Decision | Reasoning |
|------|----------|-----------|
| 2026-03-04 | Pure static, no backend | Client has no need for forms/reviews; simplest deploy to Ionos |
| 2026-03-04 | Bootstrap 5.3 via CDN | No build tools needed; fast setup; well-maintained |
| 2026-03-04 | tel: links only for contact | No form backend needed; direct calls are better for this client type |
| 2026-03-04 | Gallery as placeholders | Client has no photos yet; placeholders are better than removing the section |
