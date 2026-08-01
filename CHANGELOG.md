# Changelog

All toolkit releases. The site reads `version.json`; this file is the human-readable record.

## 1.0.0 — 2026-07-31

- First release of the three skills: `ctc-source-map`, `ctc-harvest`, `ctc-assemble`
- START-HERE setup and weekly guide; city config template
- Companion site: setup section, per-city source registry, harvest and assemble
  prompt generators, event-sheet triage with PICK/DUPE/CUT, browser-side sheet
  checks, Substack send guide, per-city issue log. All state lives in the
  browser (localStorage); no backend, no tracking.

## 1.1.0 - 2026-07-31

- Site redesign for clarity: hero workflow diagram (Claude lane vs you lane), weekly rhythm cards, plainer copy, Cohere-inspired visual system (white canvas, deep green, coral accents, pill buttons, mono labels)
- No em or en dashes anywhere in site copy
- Skills unchanged from 1.0.0

## 1.2.0 - 2026-07-31

- Import a backup: load a previously exported .json file to restore sources, sheets, drafts and the issue log, e.g. after clearing browser data or moving to a new computer
