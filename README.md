
# 🤖 Fauna Sprout Robot — Daily Production Status

**Live page:** [https://onholub.github.io/fauna-daily/](https://onholub.github.io/fauna-daily/)

---

## Overview

A single-page interactive production status tracker for the **Fauna Sprout Robot pilot program**. Designed for daily standups, executive reviews, and shift handoffs — everything editable inline, no backend required.

Built as a self-contained `index.html` — runs entirely in the browser with `localStorage` persistence.

---

## Features

### 📝 Fully Editable
- Every text element on the page is editable — titles, headers, dates, footer, resources
- Click any cell in the production table to update Actual / Planned numbers
- Section titles, KPI labels, notes — all inline editable

### 📊 Production Overview
- **Stage × Day matrix** with automatic conditional formatting
  - 🟢 Green = actual ≥ planned (on target)
  - 🔴 Red = actual < planned (behind)
  - ⬇ Today column highlighted with gold border
- **KPI cards** auto-calculate from table data (units completed, on track / behind status)
- Stage names are editable — adapt to any manufacturing flow

### ⚠️ Main Limiters Tracker
- Columns: **Criticality** · **Status** · **Issue** · **Action** · **Owner** · **Opened** · **Due**
- **Criticality badge** — click to toggle P1 ↔ P2
- **Status badge** — click to cycle OPEN → WIP → DONE
- **Opened date** — tracks when the issue was first logged (auto-fills on creation)
- **Due date** — target resolution, editable for carry-over issues
- Individual rows can be reordered (▲▼) or deleted (×)

### 📓 Daily Notes
- Collapsible section with date-stamped entries
- Dates are editable
- Notes can be reordered and deleted
- New notes auto-stamp with today's date

### 💾 Save & History
- **Auto-save** — current state saves to localStorage every 3 seconds
- **Named snapshots** — click Save (or `Ctrl+S`) to create a labeled snapshot
- **History rail** (left sidebar) — slim date-dot timeline, expandable to full list
  - Click any snapshot to view it (read-only with yellow banner)
  - Click "← Back to Current" to return to working version
  - Delete old snapshots from expanded view
  - Up to 50 snapshots stored

### 📤 Export Options
| Button | Output |
|--------|--------|
| ⬇ HTML | Clean static HTML file (no toolbar, no controls) |
| 📷 PNG | 2× resolution screenshot as PNG download |
| ✉ Email | Opens email client with pre-filled subject + plain-text summary |

### 🖨️ Print Ready
- All edit controls, toolbar, history rail hidden automatically
- Clean professional output for printing or PDF export via browser

---

## Quick Start

### Option 1: GitHub Pages (recommended)
1. Fork or clone this repo
2. Enable GitHub Pages (Settings → Pages → Deploy from `main` branch)
3. Visit `https://<your-username>.github.io/fauna-daily/`

### Option 2: Local
1. Download `index.html`
2. Open in any modern browser
3. Start editing — data saves to your browser's localStorage

---

## File Structure

```
fauna-daily/
├── index.html    ← entire app (single file, no dependencies)
└── README.md     ← this file
```

No build step. No dependencies. No framework. Just one HTML file.

---

## Usage — Daily Standup Flow

1. **Before standup** — Update production table with today's numbers
2. **During standup** — Walk through Executive Summary → Production → Limiters
3. **After standup** — Add daily note, update limiter statuses, click **💾 Save**
4. **End of day** — Save snapshot labeled "EOD Oct 8" for the record
5. **Carry-over items** — Limiters with OPEN/WIP status carry to next day automatically

---

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl+S` / `Cmd+S` | Open Save Snapshot dialog |
| `Tab` | Navigate between editable cells |
| `Enter` | Confirm edit in cell |

---

## Browser Support

Tested on Chrome, Firefox, Safari, Edge. Requires JavaScript enabled. Data stored in `localStorage` — clearing browser data will reset the page (use Export HTML to back up).

---

## Legend

**Criticality:**
- **P1** — Safety: operators endangered · Quality: compliance issue · Delivery: line down
- **P2** — Quality: primary function failure · Delivery: delay >6h

**Status:**
- 🔴 **OPEN** — Issue identified, not yet addressed
- 🟡 **WIP** — Work in progress
- 🟢 **DONE** — Resolved

---

## License

Internal use — Fauna Sprout Robot pilot program.
