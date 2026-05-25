# Security Policy — Tableau Stimulator Enterprise

## Overview

Tableau Stimulator Enterprise is a **client-side only** application. All data processing happens entirely within the user's browser. No data is transmitted to any server, stored in any database, or shared with any third party.

## Data Privacy

- **Your data never leaves your browser.** All CSV files are processed in browser memory only.
- **No cookies.** The application does not set any cookies.
- **No tracking.** No analytics, no telemetry, no usage tracking.
- **No accounts.** No login, no registration, no user data collected.
- **No AI API.** No data is sent to any AI service for processing.
- **Workspace files** are downloaded to your local device only.

## Supported Versions

| Version | Support Status |
|---|---|
| v9.x Enterprise | Active — all fixes applied |
| v8.x | Security fixes only |
| v7.x and below | Not supported |

## Reporting a Vulnerability

**Do not open a public GitHub Issue for security vulnerabilities.**

Contact the author directly:
- Email: hmgconcepts@gmail.com
- LinkedIn: https://linkedin.com/in/adewalesamsonadeagbo

### Response Timeline
- Acknowledgement: Within 48 hours
- Assessment: Within 7 days
- Fix (if confirmed): Within 30 days for critical issues

## Known Limitations

- **Formula evaluation** uses `new Function()` — only use with trusted CSV data
- **Inline editing** modifies browser memory only — no changes to original files
- **Not designed for PII** in production — anonymise sensitive data before uploading

## Creator / Owner
**Adewale Samson Adeagbo** — Data Scientist, STEM Educator, Lagos, Nigeria
- Portfolio: https://cssadewale.pages.dev | HMG Concepts: https://hmgconcepts.pages.dev | HMG Academy: https://hmgacademy.pages.dev
- GitHub: https://github.com/cssadewale | Email: hmgconcepts@gmail.com | WhatsApp: +234 810 086 6322
