# Air Clean Corp — Website

Static website for **Air Clean Corp** (aircleancorp.com), a professional HVAC cleaning and preventative maintenance company based in Richmond, Virginia. Established 1978. Virginia Class A Licensed.

---

## Pages

| Page | Description |
|------|-------------|
| `index.html` | Home / landing page |
| `contact.html` | Contact information, team, and service area |

## Tech Stack

- **HTML5 / CSS3 / JavaScript (ES6)** — no build step, no framework
- **Bootstrap 5.3** — layout and mobile responsiveness (via CDN)
- **Bootstrap Icons 1.11** — all icons (via CDN)
- **Google Fonts** — Roboto (headings) + Open Sans (body)

No backend. No database. No dependencies to install.

---

## Project Structure

```
aircleancorpsite/
├── index.html          # Home page (16 sections)
├── contact.html        # Contact page (7 sections)
├── css/
│   └── style.css       # All custom styles and brand variables
├── js/
│   └── main.js         # Navbar scroll behavior and smooth scroll
└── Image/
    ├── acc_logo_transparent.png   # Primary logo (navbar, footer, hero)
    ├── accLogo.png                # Alternate logo
    ├── transparent_icon.png       # Favicon
    ├── ashrae.png                 # ASHRAE membership badge
    └── swam.png                   # Virginia SWaM certification badge
```

---

## Running Locally

No server required. Open `index.html` directly in any browser:

```bash
open index.html      # macOS
start index.html     # Windows
xdg-open index.html  # Linux
```

Or double-click `index.html` in Finder / File Explorer.

> **Note:** The Google Maps embed on `contact.html` and CDN resources (Bootstrap, fonts, icons) require an internet connection to render correctly.

---

## Deployment

The site is hosted on **Ionos** at [aircleancorp.com](https://aircleancorp.com). DNS is managed by Microtel Systems Corporation.

**To deploy updates:**
1. FTP or upload via the Ionos file manager
2. Maintain the folder structure — `index.html` must live at the hosting root
3. Upload `css/`, `js/`, and `Image/` subdirectories alongside the HTML files

No build process. Upload files as-is.

---

## Brand

| Token | Value | Usage |
|-------|-------|-------|
| `--acc-red` | `#C41E3A` | CTAs, accents, badges |
| `--acc-navy` | `#1B2A4A` | Backgrounds, headings, navbar |
| `--acc-white` | `#FFFFFF` | Text on dark backgrounds |

Fonts: **Roboto** (headings, 700/800 weight) · **Open Sans** (body, 400/600 weight)

---

## Contact

**Air Clean Corp**  
4909 W Clay Street, Richmond, VA 23230  
804-353-5150 · Mon–Fri 7AM–5PM
