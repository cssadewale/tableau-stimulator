# Contributing to DataViz Studio

Thank you for your interest in contributing. This guide covers everything you need.

---

## Table of Contents

1. [How to Contribute](#how-to-contribute)
2. [Development Setup](#development-setup)
3. [Architecture Overview](#architecture-overview)
4. [Coding Standards](#coding-standards)
5. [Adding New Chart Types](#adding-new-chart-types)
6. [Adding New Features](#adding-new-features)
7. [Submitting a Pull Request](#submitting-a-pull-request)
8. [Reporting Bugs](#reporting-bugs)

---

## How to Contribute

| Type | Description |
|---|---|
| Bug Fix | Fix a reported issue |
| New Feature | Add a new capability |
| Documentation | Improve README, CHANGELOG, or inline help text |
| UI Improvement | Improve layout, accessibility, or visual design |
| Performance | Optimise rendering for large datasets |

---

## Development Setup

DataViz Studio has **no build step, no package manager, and no dependencies to install**.

```bash
# 1. Fork the repository on GitHub

# 2. Clone your fork
git clone https://github.com/YOUR-USERNAME/dataviz-studio.git
cd dataviz-studio

# 3. Open in browser
open index.html        # macOS / Linux
start index.html       # Windows
# Or use VS Code + Live Server extension for auto-reload
```

**Recommended tools:**
- VS Code with the Live Server extension
- Chrome DevTools (F12) for debugging
- Firefox DevTools for cross-browser verification

---

## Architecture Overview

The entire application is a single HTML file with three sections:

```
index.html
├── <style>     All CSS — variables, layout, components, animations
├── <body>      All HTML — panels, shelves, tabs, modals, overlays
└── <script>    All JavaScript — state, logic, rendering, exports
```

### JavaScript Organisation

The JS is organised into clearly commented sections (search for the section header to jump to it):

```
STATE              — G{}, DS{}, sheets[], SHEET_DEFAULTS()
PALETTES           — 10 colour palette arrays
TEMPLATES          — 12 chart template configurations
HELP_CONTENT       — Built-in documentation data array

FILE/DATASET       — CSV loading, field type detection, DS switching
MULTI-SHEET        — Sheet creation, switching, save/load state
THEME              — Light/dark mode toggle
FIELD LIST         — Left pane rendering, field profiling
DRAG & DROP        — Shelf drag-and-drop system
FILTERS            — Range sliders, checkbox filters
CALC FIELDS        — Formula parsing and evaluation
JOIN               — Dataset joining logic
AGGREGATION        — All aggregation and helper functions
CHART RENDERING    — buildOption() and renderChart()
STATISTICS         — Descriptive stats, outliers, correlation
DATA CLEANER       — Missing, duplicates, trim, case, binning, S&R
WHAT-IF            — Multiplier scenario simulation
SMART NARRATIVE    — Algorithmic chart summary generator
UNDO/REDO          — Action history system
COMPARE MODE       — Dual side-by-side chart view
REPORT BUILDER     — HTML report assembly and export
GOAL LINE          — Target reference line
TOP N FILTER       — Top/bottom N category filter
BINNING            — Numeric field binning into ranges
SEARCH/REPLACE     — Field value find and replace
CUSTOM COLORS      — Per-series color override
CELL EDITING       — Inline preview table editing
KEYBOARD           — Shortcut event listener system
PIVOT TABLE        — Cross-tabulation
DASHBOARD          — Panels, KPI cards, drill-down, global filter
EXPORT             — PNG, CSV, HTML, JSON
SAVE/LOAD          — Workspace serialisation
HELP SYSTEM        — Documentation panel
TEMPLATES          — Chart template picker
AUTO CHART         — Automatic chart type selection
FORMULA BAR        — Quick calculated field input
TABS & MISC        — Navigation, preview, status, utilities
INIT               — Startup calls
```

### Core State Objects

| Object | Description |
|---|---|
| `G` | Global shared state — palette, theme, joined data, calc fields, dashboard panels, KPI cards |
| `DS` | Two dataset slots: `DS[1]` and `DS[2]`, each with `{data, headers, fieldTypes, filename}` |
| `sheets` | Array of sheet objects, each with independent shelf, filter, chart, and annotation state |
| `sh()` | Helper returning the active sheet: `sheets[activeSheetIdx]` |

---

## Coding Standards

### Rules That Must Not Be Broken

1. **No external dependencies** beyond ECharts, PapaParse, and Google Fonts (already loaded).
2. **No build step** — code must work as raw JS in any modern browser.
3. **No AI API calls** — all intelligence must be algorithmic and local.
4. **Single file** — all code stays in `index.html`.
5. **Mobile-first** — test on small screens. Primary target: Android tablet.
6. **Every interactive element must have a `title` attribute** explaining what it does.
7. **Every new feature must be documented** in the `HELP_CONTENT` array.

### JavaScript Style

```javascript
// Use const/let, never var
const data = getFilteredData();
let count = 0;

// Arrow functions for callbacks
data.forEach(row => { /* ... */ });

// Template literals for strings
const label = `${field}: ${fmt(value)}`;

// Guard against missing DOM elements
const el = document.getElementById("my-element");
if (!el) return;

// Early returns to reduce nesting
function processData(data) {
  if (!data || !data.length) { toast("error", "No data"); return; }
  // main logic here
}

// No unescaped apostrophes in single-quoted strings
// WRONG:  {desc: "field's values"}  inside a single-quoted JS string
// RIGHT:  {desc: "field's values"} or use double quotes for the outer string
```

### Tooltip Requirement

Every button, input, select, and interactive element must have a `title` attribute:

```html
<!-- Required format -->
<button onclick="applyTopN()"
  title="Top N Filter — shows only the N highest (or lowest) categories
         by aggregated value. Enter a number, choose Top or Bottom,
         then click Apply. Click Clear to restore all categories.">
  Apply
</button>
```

### Help Content Requirement

Every new feature must be documented in `HELP_CONTENT`:

```javascript
{
  title: "Your Feature Name",
  desc: "Clear explanation in plain English. What it does. When to use it.
         How to use it. Write as if explaining to a non-technical user."
}
```

---

## Adding New Chart Types

**Step 1.** Add the option to the chart type `<select>` in HTML:

```html
<option value="treemap">🌳 Treemap</option>
```

**Step 2.** Add a handler in `buildOption()` in JavaScript:

```javascript
// TREEMAP
if (chartType === "treemap") {
  if (!xF || !yFs.length) return null;
  const ad = aggregateBy(data, xF, yFs[0], agg);
  return {
    backgroundColor: bg(),
    color: palette,
    title: titleOpt,
    tooltip: { ...btt, formatter: "{b}: {c}" },
    series: [{
      type: "treemap",
      data: ad.map(d => ({ name: d.x, value: d.y }))
    }]
  };
}
```

**Step 3.** Add to Compare Mode and Dashboard panel selects.

**Step 4.** Add a template in `TEMPLATES` if appropriate.

**Step 5.** Document in `HELP_CONTENT` under the "Chart Types" section.

---

## Adding New Features

Follow this pattern for right-panel features:

**Step 1.** Add CSS:
```css
/* ── MY FEATURE ── */
.myfeature-input { background: var(--bg-card); border: 1px solid var(--border); ... }
```

**Step 2.** Add HTML in `#right-pane`:
```html
<div class="rp-section">
  <div class="rp-title" title="My Feature — what it does">My Feature</div>
  <!-- controls here -->
</div>
```

**Step 3.** Add JavaScript, clearly commented:
```javascript
// ── MY FEATURE ─────────────────────────────────────────
function myFeatureFunction() {
  // implementation
}
```

**Step 4.** If it needs field selectors, populate in `renderFieldList()`:
```javascript
bindDrag(); populateAtdSelects(); ... populateMyFeature();
```

**Step 5.** If it affects chart rendering, integrate into `buildOption()` or `buildMarkLines()`.

**Step 6.** If it affects chart state, add to `SHEET_DEFAULTS()` and `clearAll()`.

**Step 7.** Add keyboard shortcut if appropriate.

---

## Submitting a Pull Request

**Step 1.** Create a descriptive branch:
```bash
git checkout -b feat/treemap-chart
git checkout -b fix/pivot-export-encoding
git checkout -b docs/update-keyboard-shortcuts
```

**Step 2.** Make changes to `index.html` (and docs as needed).

**Step 3.** Test thoroughly:
- Chrome desktop
- Firefox desktop
- Chrome Android (or DevTools mobile emulation)
- CSV file with 500+ rows
- CSV file with missing values
- Workspace save → reload → workspace load

**Step 4.** Update `CHANGELOG.md` — add your change under `## [Unreleased]`.

**Step 5.** Commit with a clear message:
```bash
git commit -m "feat: add treemap chart type with TopN and color-by support"

# Prefixes:
# feat:     new feature
# fix:      bug fix
# docs:     documentation only
# style:    CSS/visual only
# perf:     performance improvement
# refactor: restructuring without functional change
```

**Step 6.** Push and open a Pull Request with a clear title, description, screenshots (if visual), and browsers tested.

---

## Reporting Bugs

Open a [GitHub Issue](../../issues/new?template=bug_report.md) and include:
- Browser name and version
- Device and operating system
- Exact steps to reproduce
- Expected vs actual behaviour
- A sample CSV file (if data-related)
- Console error messages (F12 → Console tab)

---

## Questions?

- 📧 buildingmyictcareer@gmail.com
- 🔗 [LinkedIn](https://linkedin.com/in/adewalesamsonadeagbo)
- 🐙 [GitHub](https://github.com/cssadewale)

Thank you for contributing to DataViz Studio.
