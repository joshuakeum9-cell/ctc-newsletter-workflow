# CTC Newsletter Toolkit — companion site

Live: **https://joshuakeum9-cell.github.io/ctc-chapter-launch-workflow/**

A static companion page for the CTC Newsletter Toolkit: three Claude skills
(`ctc-source-map`, `ctc-harvest`, `ctc-assemble`) that help a volunteer city lead
produce a weekly climate events newsletter.

The page does three things and nothing else: it hands out the toolkit, explains
the setup, and explains the weekly workflow with a copy-ready prompt for each
step. **The skills do the work, inside the lead's own Claude account.** This page
has no backend, no account connection, and stores nothing.

## Structure

| Section | What it holds |
|---|---|
| Hero and diagram | The one-line thesis, and a workflow diagram showing which steps are Claude's and which are the lead's |
| Weekly rhythm | Four day cards with honest time estimates, linking to their sections |
| **Set up once** (always open) | Downloads, install steps, install verification prompt, city config, Claude project, and the source registry prompt |
| Your city | A single field that fills every prompt on the page. Not saved |
| **Thursday · Collect** | Harvest prompt |
| **Friday · Cut** | Triage guidance. No prompt: this is judgment, done in the spreadsheet |
| **Monday · Write** | Assemble prompt, then what the three bracketed gaps need |
| **Tuesday · Send** | Pre-send checks and Substack paste steps |
| When something breaks | Troubleshooting, collapsed |

## What this page deliberately does not do

- **No saved state.** No workspace, no source registry table, no issue log, no
  backup export or import. Earlier versions had these; they are gone, and the
  page clears anything they left in the browser.
- **No writing scaffolds.** `ctc-assemble` already emits the opening note, picks,
  and opportunities scaffolds with their gaps marked, in the document it hands
  back. Duplicating them here meant maintaining the same content twice.
- **No fake execution.** The page cannot run a skill or reach a Claude account.
  Every action is either a copy-ready prompt or a plain instruction.

## Contents

- `index.html` — the whole site; no framework, no build step, no analytics, no cookies
- `downloads/` — the toolkit: three skills, START-HERE.md (offline reference),
  city-config-template.md, and the zip under a stable filename
- `version.json` — version, date, changelog. The page renders its badge and
  changelog from this file, so shipping a new version is editing one JSON file
  (plus `CHANGELOG.md` for the human-readable record)
- `playbook/newsletter-chapter.md` — Chapter 8 draft for the CTC Operational Playbook
- `TODO.md` — open items: trimming START-HERE.md, and the two install screenshots

## Design

Follows the Climate Tech Cities design system: one olive green ink (`#25331a`)
for text, borders and fills; a cream (`#f5f4e9`) paper canvas alternating with
warm white in full-width bands; Jost Light 300 with positive letter-spacing as
the open substitute for Halyard Display; square outlined buttons; no shadows.
Accents are rationed to one home each, lavender on the one-rule band and pale
blue behind the diagram.
