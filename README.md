# CourtBalance AI

**A scheduling transparency tool for Chapel Hill, NC Parks & Recreation**

![Status](https://img.shields.io/badge/status-MVP%20Demo-blue)
![License](https://img.shields.io/badge/license-MIT-green)

---

## Overview

CourtBalance AI gives Chapel Hill residents and Parks & Rec staff a single, clear view of weekly court schedules across all public tennis and pickleball facilities. It surfaces scheduling conflicts, enables quick staff adjustments, and collects structured community feedback — all in one page.

### The Problem

Residents and staff lack a unified view of which courts are available for tennis vs. pickleball at any given time, leading to scheduling conflicts, crowding frustration, and perceived unfairness in court allocation.

### The Solution

A self-contained web app that:
- Displays all **13 Chapel Hill pilot facilities** with real addresses, court counts, and status info
- Shows a **weekly schedule grid** with color-coded blocks (Open Play, Reserved, Maintenance)
- Lets staff **edit schedules inline** and use an **AI-powered "Suggest Balance"** tool for fair 50/50 allocation
- Accepts **community feedback** and provides a **staff inbox** for review
- Includes an **interactive map** for finding courts by location

---

## Quick Start

1. **Download** or clone this repository.
2. **Open** `courtbalance-ai.html` in any modern browser (Chrome, Firefox, Safari, Edge).
3. That's it — no server, no build step, no dependencies to install.

> **Note:** Internet connection is required for Google Fonts (Inter) and the Leaflet.js map tiles. The app gracefully falls back to system fonts if offline.

---

## Features

### 🎾 Facility Browser
- 13 real Chapel Hill facilities with addresses, court counts, lighting & indoor status
- Filter by sport (Tennis / Pickleball), lighted, and indoor
- Status indicators for closures and reconstruction

### 📅 Weekly Schedule Grid
- 7-day × 14-hour grid (7 AM – 9 PM) with color-coded blocks
- **Green** = Open Play / Drop-in
- **Amber** = Reserved / League / Program
- **Red** = Maintenance / Closed

### 🗺️ Interactive Map
- All facilities plotted on an OpenStreetMap-powered map
- Click markers to view facility details and jump to schedules
- Color-coded pins by sport type

### 👤 Staff View
- Toggle between Public and Staff views (no authentication — demo mode)
- **Inline schedule editing** — click any cell to change block type and sport
- **AI Suggest Balance** — one-click 50/50 tennis/pickleball split for dual-sport facilities with plain-language rationale
- **Feedback Inbox** — review and triage community submissions

### 📋 Community Feedback
- Structured form: facility, sport, category, description, optional email
- Categories: Crowding, Scheduling Fairness, Maintenance, Behavior, Other
- Staff can toggle feedback status (New → Reviewed)

---

## Facilities Covered

| Facility | Sports | Courts | Lighted | Indoor | Status |
|----------|--------|--------|---------|--------|--------|
| Ephesus Park (Tennis) | Tennis | 4 | ✓ | | Open |
| Hargraves Center Park | Tennis | 3 | ✓ | | Open |
| Oakwood Park | Tennis | 1 | | | Open |
| Phillips Park | Tennis | 4 | | | Open |
| Cedar Falls Park | Tennis | 6 | ✓ | | Closed |
| UNC South Campus (Tennis) | Tennis | 2 | | | Open |
| Southern Community Park | Pickleball | 11 | ✓ | | Open |
| Ephesus Park (Pickleball) | Pickleball | 6 | ✓ | | Open |
| Chapel Hill Community Center | Pickleball | TBD | | ✓ | Open |
| UNC South Campus (Pickleball) | Pickleball | 5 | | | Open |
| Seymour Center | Pickleball | TBD | | | Open |
| Hargraves Community Center | Pickleball | TBD | | | Open |
| Chatham Co. NE District Park | Pickleball | TBD | | | Open |

---

## Technical Details

- **Single file:** Everything lives in one self-contained `.html` file
- **No framework:** Vanilla HTML + CSS + JavaScript
- **External CDN only:** Google Fonts (Inter) and Leaflet.js (map)
- **In-memory data:** All state is session-only; changes reset on reload
- **Desktop-first:** Optimized for viewports ≥ 1024px

### Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Primary Blue | `#4B9CD3` | Buttons, accents, tennis badges |
| Dark Navy | `#13294B` | Top bar, headings, text |
| Open Play Green | `#2E8B57` | Open play blocks, pickleball badges |
| Reserved Amber | `#D4A017` | Reserved/league blocks |
| Closed Red | `#C0392B` | Maintenance blocks, closure badges |
| Background | `#F4F6F8` | Page background |

---

## MVP Limitations

This is a demo/prototype. The following are intentionally out of scope:

- **No server-side persistence** — all changes lost on reload
- **No authentication** — staff/public toggle is visual only
- **No mobile layout** — desktop-first for demo purposes
- **No data export** — feedback and schedules are in-memory only
- **Deterministic AI** — "Suggest Balance" uses a simple 50/50 rule, not ML

---

## License

MIT — Free to use, modify, and distribute.

---

*Built for Chapel Hill, NC Parks & Recreation*
