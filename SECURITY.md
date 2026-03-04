# Security Policy

## Scope

This repository contains a **fully static website** (HTML, CSS, JavaScript). There is no backend server, no database, no user authentication, no form processing, and no server-side code of any kind.

The attack surface is intentionally minimal by design.

---

## What This Site Does and Does Not Do

| | Status |
|---|---|
| Accepts user input / form submissions | No |
| Stores user data | No |
| Uses cookies or sessions | No |
| Has a backend / API | No |
| Runs server-side code | No |
| Uses a database | No |
| Processes payments | No |
| Handles credentials | No |

---

## Third-Party Dependencies

All external resources are loaded from pinned CDN versions:

| Resource | Source | Version |
|----------|--------|---------|
| Bootstrap CSS + JS | jsDelivr CDN | 5.3.3 (pinned) |
| Bootstrap Icons | jsDelivr CDN | 1.11.3 (pinned) |
| Google Fonts (Roboto, Open Sans) | fonts.googleapis.com | N/A |

Versions are explicitly pinned in the HTML `<link>` and `<script>` tags. Review and update these when new versions are released.

**External links** in the research sources section (EPA, APPA, Harvard, ASHRAE) open in new tabs with `rel="noopener noreferrer"` to prevent tab-napping attacks.

---

## Deployment Security Notes

- This site is deployed via FTP to Ionos shared hosting
- No `.env` files, API keys, or secrets exist in this codebase
- No credentials should ever be committed to this repository
- Keep Ionos FTP credentials private and out of version control

---

## Reporting a Vulnerability

This is a static informational website with no user-facing interactivity. However, if you identify a legitimate security concern (e.g., a compromised CDN dependency, a defaced deployment, or a vulnerable third-party script), please report it by:

1. Opening a **private GitHub security advisory** on this repository
2. Or emailing the site owner directly at the contact information on [aircleancorp.com](https://aircleancorp.com)

Do not open a public issue for security concerns.

---

## Supported Versions

| Version | Supported |
|---------|-----------|
| Current (`main` branch) | Yes |
| Any prior deployment | No — always update to the latest |
