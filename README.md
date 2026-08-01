# CTC Newsletter Toolkit — companion site

Live: **https://joshuakeum9-cell.github.io/ctc-newsletter-workflow/**

A static companion workspace for the Climate Tech Cities newsletter toolkit —
three Claude skills a chapter lead installs in their own Claude account
(`ctc-source-map`, `ctc-harvest`, `ctc-assemble`). **The skills do the work.**
This site holds the lead's config, event sheet, draft, and log between runs,
and generates the prompts they paste into Claude.

## Governing rule

Nothing on the page is fake. Every control either does something real in the
browser with no backend, or honestly hands off to Claude with a copy-paste
prompt.

| Step | What it really does |
|---|---|
| 0. Setup | Downloads (zip + individual files), install steps from START-HERE.md, persistent readiness checklist |
| 1. Source registry | Editable per-city table in localStorage; markdown export; quarterly-staleness warning |
| 2. Harvest | Generates the harvest prompt (city, week window, source list) with a copy button |
| 3. Cut | Import/paste the harvest CSV; KEEP→PICK→DUPE→CUT toggles; live surviving count |
| 4. Assemble | Generates the assemble prompt, optionally carrying the surviving rows as CSV |
| 5. You write | Three autosaving editorial blocks (stays human — the thesis of the toolkit), word count, markdown export |
| 6. Checks | Browser-side linter: duplicates, past dates, block/window mismatches, missing links/dates. Reports, never fixes |
| 7. Send | Numbered Substack paste steps + "mark as sent" which writes the log |
| 8. Log | Per-city issue history in localStorage |

## Contents

- `index.html` — the whole site; no framework, no build step, no analytics
- `downloads/` — the toolkit: skills, START-HERE.md (**source of truth** for the
  process), city-config-template.md, and the zip under a stable filename
- `version.json` — version, date, changelog; the page renders its badge and
  changelog from this file, so shipping a new version = editing this JSON
  (plus `CHANGELOG.md` for the human-readable record)
- `playbook/newsletter-chapter.md` — Chapter 8 draft for the CTC Operational Playbook

## Notes

- All workspace data is browser-local (localStorage). The page warns once and
  offers an export-all backup button.
- Setup and downloads work with JavaScript disabled.
- Stable download URLs never change across versions; the versioned filename is
  applied via the `download` attribute from `version.json`.
