# Tableau Stimulator Enterprise — Complete System Feature Guide

## 👤 Creator / Owner
**Adewale Samson Adeagbo** — Data Scientist · STEM Educator · AI-Augmented Solutions Developer · Founder, HMG Concepts · Lagos, Nigeria
- Portfolio: https://cssadewale.pages.dev | HMG Concepts: https://hmgconcepts.pages.dev | HMG Academy: https://hmgacademy.pages.dev
- GitHub: https://github.com/cssadewale | LinkedIn: https://linkedin.com/in/adewalesamsonadeagbo
- Email: hmgconcepts@gmail.com | WhatsApp: +234 810 086 6322

---

This guide explains every feature in the Enterprise Edition. It preserves all original features and adds 16 enterprise capabilities. No paid service, backend, database, or AI API is required.

## 1. Tableau-Style Workspace (Original)
- **Worksheet:** Main analysis canvas with drag-and-drop shelves, chart type selector, aggregation, sorting, labels, trend, forecast and filters
- **Shelves:** COLS (X/category), ROWS (Y/measures). Multiple ROWS = multi-series
- **Marks:** Color By, Size By, Label — mark encodings that change visual appearance
- **Workbook Sheets:** Unlimited sheets with independent state

## 2. Charting — 23 Chart Types
### Original (15): Bar, Horizontal Bar, Stacked Bar, Line, Area, Stacked Area, Scatter, Pie, Donut, Radar, Heatmap, Box Plot, Waterfall, Funnel, Gauge
### Enterprise (8): Treemap, Sunburst, Sankey, Parallel Coordinates, Bubble, Nightingale Rose, Histogram, Bullet
- **Forecast (🔮):** 5-step linear projection — no AI API
- **Moving Average (Ⓜ):** 3-point rolling average

## 3. Show Me / Template Picker (Original)
12 templates: Sales Ranking, Trend, Part of Whole, Distribution, Correlation, Contribution, Funnel, Cumulative Flow, Waterfall, KPI Gauge, Heat Analysis, Horizontal Ranking

## 4. Calculated Fields (Original)
Formula bar with `[FieldName]` syntax: `[Revenue] - [Cost]`, `[Sales] / [Target] * 100`

## 5. Filters, Top N, Reference/Goal Lines (Original)
Range and checkbox filters, Top/Bottom N, fixed reference lines, auto mean/median/max/min, goal/target line

## 6. Data Preparation (Original)
Scan, Fill Missing, Remove Duplicates, Trim Spaces, Standardise Casing, Search & Replace, Data Binning, Inline Editing

## 7. Statistics (Original)
Descriptive stats, IQR outliers, Pearson correlation matrix, CSV export

## 8. Pivot Table (Original)
Cross-tabulation with totals, heatmap, CSV export

## 9. Dashboard (Enhanced in Enterprise)
Chart panels, KPI cards, sparklines, drill-down, global filters, 1/2/3/**4-column** layouts, presentation mode, PNG export

## 10. Report Builder (Original)
Selectable components (chart, insights, stats, pivot), HTML/PDF export

## 11. Smart Narrative (Original)
Rule-based algorithmic summary — no AI API

## 12. Save/Load Workspace (Original)
Full JSON serialization and restoration

## 13. Compare Mode (Original)
Side-by-side dual chart view with independent configuration

## 14. Ask Data (Original)
Local rule-based natural language queries: "top sales by region"

## 15. Data Dictionary (Original)
Field metadata: type, role, missing count, distinct count, examples. CSV export

---

## ENTERPRISE FEATURES (v9.0)

## 16. Treemap Chart
Hierarchical area visualization. Each rectangle's area = aggregated value. COLS=dimension, ROWS=measure. Best for 10+ categories showing composition.

## 17. Sunburst Chart
Multi-level radial hierarchy. COLS=parent, ROWS=measure, Color By=child. Inner ring = parents, outer = children. Click to drill.

## 18. Sankey Flow Diagram
Flow visualization. COLS=Source, Color By=Target, ROWS=Value. Line thickness = flow volume. Customer journeys, budget flows.

## 19. Parallel Coordinates
Multi-dimensional comparison. Each numeric field = vertical axis, each row = connecting line. Auto-detects all numeric fields (up to 8).

## 20. Bubble Chart
Scatter + size encoding. COLS=X, ROWS=Y, Size By=bubble diameter. Three-variable comparison.

## 21. Nightingale Rose
Polar area chart. Sector radius = magnitude. Better than pie for absolute magnitude comparison. Cyclical data.

## 22. Histogram
Auto-binned frequency distribution. 15 bins. ROWS=numeric field. Shows count per bin. Data shape, skewness, outlier detection.

## 23. Bullet Chart
Actual vs target with quality bands. COLS=dimension, ROWS=measure, Goal Line=target. Compact KPI format.

## 24. Data Stories / Storyboard
Capture charts as numbered story points with editable titles and captions. Navigate between points. Export as standalone HTML presentation. Replicates Tableau Story.

## 25. Explain Data
Algorithmic analysis generating 8 structured insights: overview, dominant category, lowest performer, trend direction, variability, distribution shape, concentration, recommendations. No AI API.

## 26. Linear Regression
OLS regression: R², slope, intercept, standard error, Pearson r, regression equation, interpretation. Select X and Y numeric fields.

## 27. K-Means Clustering
Unsupervised grouping into K clusters. Select 2 numeric fields, choose K (2-8). Results: centroids, sizes, percentages. Adds _Cluster field to data for visualization.

## 28. Enterprise Export Center
9 formats: PNG, SVG, CSV, HTML report, workbook JSON, print/PDF, pivot CSV, stats CSV, dictionary CSV. All local.

## 29. Row-Level Security Simulation
Restrict visible rows by field=value rule. Original data preserved. Toggle on/off. Governance training.

## 30. 4-Column Dashboard Layout
Enterprise-grade dense KPI grid with 4-column option.

## 31. SVG Vector Export
Scalable vector graphics for print-quality publications.

## 32. Enterprise UI Components
- **Splash Screen:** Branded loading screen with creator details
- **Enterprise Status Bar:** Version, links to HMG Concepts, HMG Academy, Portfolio
- **Enterprise Footer:** Creator attribution with links
- **About Modal Enhancement:** Enterprise features summary appended

---

## Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| Alt+R | Render chart |
| Alt+C | Clear shelves |
| Alt+Z | Undo |
| Alt+Y | Redo |
| Alt+S | Save workspace |
| Alt+E | Export PNG |
| Alt+P | Toggle data preview |
| Alt+N | Generate narrative |
| Alt+H | Toggle help |
| Alt+A | Auto Chart |
| Alt+F | Focus formula bar |
| Alt+W | Worksheet tab |
| Alt+D | Dashboard tab |
| Alt+T | Statistics tab |
| Alt+1-4 | Switch sheets |
| Escape | Close overlays |
