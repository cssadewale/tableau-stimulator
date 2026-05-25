# Contributing to Tableau Stimulator Enterprise

Thank you for your interest in contributing. This guide covers everything you need.

## Creator / Owner
**Adewale Samson Adeagbo** — Data Scientist, STEM Educator, AI-Augmented Solutions Developer, Lagos, Nigeria
- Portfolio: https://cssadewale.pages.dev | HMG Concepts: https://hmgconcepts.pages.dev | HMG Academy: https://hmgacademy.pages.dev
- GitHub: https://github.com/cssadewale | LinkedIn: https://linkedin.com/in/adewalesamsonadeagbo
- Email: hmgconcepts@gmail.com | WhatsApp: +234 810 086 6322

---

## How to Contribute

| Type | Description |
|---|---|
| Bug Fix | Fix a reported issue |
| New Feature | Add a new capability |
| Documentation | Improve README, guides, or help text |
| UI Improvement | Improve layout, accessibility, or visuals |
| Performance | Optimise rendering for large datasets |

## Development Setup

**No build step. No package manager. No dependencies to install.**

```bash
git clone https://github.com/YOUR-USERNAME/tableau-stimulator.git
cd tableau-stimulator
open index.html    # macOS/Linux
# start index.html   # Windows
```

## Architecture

Single HTML file with three sections:
- `<style>` — All CSS
- `<body>` — All HTML
- `<script>` — All JavaScript (original + enterprise extension at bottom)

Enterprise features are appended at the end of the script section, using monkey-patching to extend existing functions without modifying them.

## Rules That Must Not Be Broken

1. **No external dependencies** beyond ECharts, PapaParse, and Google Fonts
2. **No build step** — must work as raw JS in any browser
3. **No AI API calls** — all intelligence must be algorithmic
4. **Single file** — all code stays in `index.html`
5. **Every interactive element must have a `title` attribute**
6. **Every new feature must be documented** in `HELP_CONTENT`
7. **No removal of existing features** — only additions and enhancements
8. **Creator attribution must not be altered** — Adewale Samson Adeagbo

## Adding Enterprise Chart Types

1. Add option to chart type `<select>` in the Enterprise Charts section
2. Add rendering handler in `renderChartEnterprise()` function
3. Add to Help content in the Enterprise Features section
4. Test with the sample dataset and at least one custom CSV

## Submitting a Pull Request

1. Fork the repository
2. Create a descriptive branch: `feat/new-chart-type`
3. Make changes to `index.html`
4. Test on Chrome desktop + Chrome Android
5. Update `CHANGELOG.md`
6. Submit PR with clear description

## Questions?
- 📧 hmgconcepts@gmail.com
- 🔗 [LinkedIn](https://linkedin.com/in/adewalesamsonadeagbo)
- 🐙 [GitHub](https://github.com/cssadewale)
