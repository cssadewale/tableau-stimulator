# Changelog

All notable changes to DataViz Studio are documented in this file.
Format: [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)

---

## [v7.0.0] — 2025

### Added
- **Smart Narrative Engine** — 100% algorithmic chart summary. No AI API. Covers total, mean, top/bottom performers, variability, trend direction, top 3 categories.
- **Undo / Redo** — 50-step shelf action history. Alt+Z / Alt+Y keyboard shortcuts.
- **Compare Mode** — New tab with side-by-side dual chart view. Independent field, chart type, and aggregation per chart. Export both as PNG simultaneously.
- **Report Builder** — New tab. Assembles professional HTML reports from selectable components (chart, insights, stats, pivot). Inline title editing. Export as HTML or print to PDF.
- **Goal / Target Line** — Quick right-panel input. Renders a bold amber dashed line on the chart at the specified value labelled "Target: [value]".
- **Top N Filter** — Show only top or bottom N categories by aggregated value. Works on bar, line, area, and colour-encoded charts.
- **Data Binning** — Groups a numeric field into equal-width range categories. Creates a new dimension field draggable to COLS shelf.
- **Search & Replace** — Find and replace values across any field. Case-insensitive. Instant chart update.
- **Custom Series Colors** — Per-series color picker in the right panel overrides the active palette for individual measures.
- **Inline Cell Editing** — Double-click any Data Preview cell to edit its value directly. Enter to save, Escape to cancel.
- **Keyboard Shortcuts System** — Full Alt+key shortcut system. Accessible via the keyboard icon in the topbar or pressing Escape.
- **Two new chart types in Compare Mode** — Pie and Donut available in compare chart type selector.
- **v7 section in built-in Help** — All 11 new features documented in the searchable help panel.

### Fixed
- Apostrophe syntax error in Help content strings that caused entire JavaScript to fail loading.

### Changed
- Tab bar expanded from 5 to 7 tabs (added Compare, Report).
- Topbar expanded with Narrative, Undo, Redo, and Shortcuts buttons.
- clearAll() now also resets goal line and Top N filter state.
- renderPreviewTable() now calls makePreviewEditable() after build.
- addToShelf() and removeFromShelf() now call snapshotHistory() for undo support.

---

## [v6.0.0] — 2025

### Added
- **Statistics Tab** — Descriptive statistics (count, mean, median, std dev, variance, min, max, Q1, Q3, skewness), outlier detection (IQR method), Pearson correlation matrix, CSV export.
- **Data Cleaner Tab** — Scan for missing values, duplicates, type inconsistencies. One-click: Fill Missing, Remove Duplicates, Trim Whitespace, Standardise Casing.
- **What-If Simulator** — Right panel multiplier/offset tool. Creates a new calculated field on demand.
- **Formula Bar** — Persistent bar for instant calculated field creation using [FieldName] syntax.
- **Auto Chart (✨)** — Analyses field types and automatically selects the best chart, populates shelves, and renders.
- **Chart Templates (📋)** — 12 pre-built configurations (Sales Ranking, Trend Over Time, Distribution, Funnel, Waterfall, Gauge, etc.).
- **Waterfall Chart** — Incremental positive/negative changes. Green = positive, Red = negative.
- **Funnel Chart** — Sequential reduction chart sorted largest to smallest.
- **Gauge Chart** — Single metric speedometer with three colour zones.
- **STDEV Aggregation** — Standard deviation added to aggregation dropdown.
- **Outlier Highlighting** — IQR-based outlier markers (red diamonds) on chart canvas.
- **Data Sampling** — Limit rows used for rendering (All / 500 / 1K / 5K).
- **Two new palettes** — Candy (vibrant pastels) and Earth (natural tones). Total: 10 palettes.
- **Built-in Help System** — 340px slide-in panel with 10 sections, 80+ help items, searchable in real time.

---

## [v5.0.0] — 2025

### Added
- **Multi-Sheet Workbook** — Unlimited named sheets with independent shelf/filter/chart configurations.
- **Pivot Table Tab** — Cross-tabulation of any Row x Column x Value. Row totals, column totals, grand total. Heatmap colouring. CSV export.
- **KPI Cards** — Big-number metric cards with optional sparkline and delta badge (vs mean or vs previous value).
- **Dashboard Drill-Down** — Click any chart panel element to filter all other panels and KPI cards simultaneously.
- **Conditional Formatting** — Numeric cells in Data Preview coloured red (top 25%), amber (mid), green (low 40%).

---

## [v4.0.0] — 2025

### Added
- **Multi-Dataset Support (DS1 + DS2)** — Load two CSV files simultaneously and switch between them.
- **Dataset Join** — Inner, Left, and Full Outer Join on shared key fields. Preview row count before applying.
- **Chart Annotations** — Click any data point in Annotation Mode to pin a text note. Gold pin markers on chart canvas.
- **Light / Print Theme** — Clean white theme for print-ready screenshots and client presentations.
- **Global Dashboard Filter** — One field=value filter applied to all dashboard panels and KPI cards simultaneously.
- **CSV Export** — Download currently filtered dataset as a CSV file.
- **Zoom & Pan** — Scroll-to-zoom and drag slider below the chart canvas.
- **Field Profiling Panel** — Per-field statistics at the bottom of the Data Pane. Auto-updates on field selection.

---

## [v3.0.0] — 2025

### Added
- **Chart Title & Axis Label Editing** — Title bar above canvas with chart title input and X/Y axis label inputs.
- **Range Slider Filters** — Numeric fields on the filter shelf get dual range sliders.
- **Trend Lines** — Linear regression overlay on any series.
- **Reference Lines** — Add horizontal guide lines at specific Y values with custom labels and colours. Auto options: Mean, Median, Max, Min.
- **Sort Controls** — Sort X-axis categories by ascending/descending value or A-Z/Z-A alphabetically.
- **Box Plot** — Five-number summary with IQR-based whiskers and outlier markers.
- **Workspace Save / Load** — Serialise full session to JSON and restore it.
- **Dashboard PNG Export** — Each panel exported as individual high-resolution PNG.

---

## [v2.0.0] — 2025

### Added
- **Multi-Series Charts** — Multiple ROWS fields create multi-series charts with individual legends.
- **Dual Y-Axis** — When two measures are on ROWS, each gets its own Y-axis scale.
- **Color Encoding Mark** — Drop a categorical field onto Color By to split chart by colour.
- **Data Labels** — Toggle numeric value labels on every data point.
- **Heatmap Chart** — Colour-intensity grid for two-dimensional category analysis.
- **Radar / Spider Chart** — Polygon chart for multi-attribute comparisons.
- **Dashboard Tab** — Independent chart panels with configurable title, field, chart type, and aggregation.
- **Calculated Fields (f)** — Create new measures using [FieldName] formula syntax.
- **Summary Stats Bar** — SUM, AVG, MAX, MIN computed live below the chart.
- **Tooltip Configuration** — Style (Default/Detailed/Minimal) and Trigger (Axis/Item) controls.

---

## [v1.0.0] — 2025

### Added
- Initial release — complete Phase 1 shell.
- CSV / TSV upload with drag-and-drop.
- Automatic field type detection (Numeric, Categorical, Date).
- Dimensions / Measures separation in the field list.
- COLS (X-axis) and ROWS (Y-axis) drag-and-drop shelves.
- 7 chart types: Bar, Horizontal Bar, Line, Area, Scatter, Pie, Donut.
- Aggregation: SUM, AVG, COUNT, MAX, MIN, MEDIAN.
- Filter shelf with checkbox filters.
- Color By, Size By, and Label marks.
- 6 colour palettes.
- Data preview table strip.
- Export chart as PNG.
- Dark theme UI.
