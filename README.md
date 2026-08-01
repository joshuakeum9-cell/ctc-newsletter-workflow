# CTC Newsletter Toolkit — companion site

Live: **https://joshuakeum9-cell.github.io/ctc-newsletter-workflow/**

A static companion page for the CTC Newsletter Toolkit: three Claude skills
(`ctc-source-map`, `ctc-harvest`, `ctc-assemble`) that help a volunteer city lead
produce a weekly climate events newsletter.

The page's only job is getting a non-technical person from "I have three files"
to "I sent my first issue." The skills do the work; the page hands out the
prompts, holds the source registry and the issue log, and explains what happens
on each day of the week.

## Structure

The page mirrors the four weekday cards rather than a long numbered pipeline.

| Section | What it holds |
|---|---|
| **Set up** (once, ~2 hours) | Downloads, install steps, install verification, city config, source registry. Expanded on first visit; collapses to a one-line summary once a city is saved |
| **Thursday · Collect** | Harvest prompt, pre-filled with the city, issue week, and source list |
| **Friday · Cut** | Triage guidance as prose. Cutting happens in the spreadsheet the lead already has open |
| **Monday · Write** | Assemble prompt, the one rule, and copy-the-scaffold buttons for the three human blocks |
| **Tuesday · Send** | Pre-send checklist and Substack paste steps |
| **When something breaks** | Troubleshooting, collapsed |
| **Issue log** | Thin bar; per-city history in localStorage |

## Governing rule

Nothing on the page is fake. Every control either does something real in the
browser with no backend, or honestly hands off to Claude with a copy-paste
prompt. There are no mock rows, no placeholder prompts, and no Send button.

## What lives in localStorage

City name, issue week, source registry rows, and issue log entries. Nothing a
lead spends real effort on: the event sheet stays in their spreadsheet file and
the written blocks go straight into the assembled document. Export and import
backup buttons sit in the workspace bar for moving between computers.

## Contents

- `index.html` — the whole site; no framework, no build step, no analytics, no cookies
- `downloads/` — the toolkit: three skills, START-HERE.md (offline reference),
  city-config-template.md, and the zip under a stable filename
- `version.json` — version, date, changelog. The page renders its badge and
  changelog from this file, so shipping a new version is editing one JSON file
  (plus `CHANGELOG.md` for the human-readable record)
- `playbook/newsletter-chapter.md` — Chapter 8 draft for the CTC Operational Playbook
- `TODO.md` — open items: trimming START-HERE.md, and the two install screenshots

## Notes

- Setup and downloads work with JavaScript disabled.
- Stable download URLs never change across versions; the versioned filename is
  applied via the `download` attribute from `version.json`.
- The page is the current guide to the process. START-HERE.md is the offline
  reference that ships in the toolkit, and is due a trim (see `TODO.md`).
