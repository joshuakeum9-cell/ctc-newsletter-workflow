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

## 2.0.0 - 2026-07-31

- Restructured around the four weekdays: Thursday Collect, Friday Cut, Monday Write (assemble folded in), Tuesday Send (checks folded in). Source registry moved into Set up; Log is a thin bar
- Setup is expanded on first visit and collapses to a one-line summary once a city is saved
- New install verification step: ask Claude which newsletter skills it has
- Browser triage table removed; cutting happens in the spreadsheet, guidance kept as prose
- localStorage reduced to city, week, sources, and log. Writing blocks replaced with copy-the-scaffold buttons
- Troubleshooting section added
- The page is now the current guide; START-HERE.md is the offline reference
- Accessibility and mobile pass: focus rings, aria-expanded on collapsibles, text alternative for the diagram, shape plus colour in the legend, reduced-motion support

## 2.1.0 - 2026-08-01

- Re-skinned to the Climate Tech Cities design system: one olive green ink (#25331a) for text, borders and fills; cream (#f5f4e9) paper canvas alternating with warm white in full-width bands; Jost Light 300 with positive letter-spacing as the substitute for Halyard Display; square outlined buttons with no radius; no shadows anywhere
- Accents rationed to one home each: lavender on the one-rule green band, pale blue behind the workflow diagram
- Structure, copy and behaviour unchanged from 2.0.0

## 3.0.0 - 2026-08-01

- The page is now setup, workflow and prompts only. Removed the source registry table, the issue log, backup export and import, and the workspace, along with everything they stored. The page saves nothing and clears anything earlier versions left in the browser
- Removed the three writing scaffolds: the assemble skill already produces them, with the gaps marked, inside the document it hands back
- Setup is open by default and no longer collapses
- One city field fills all three prompts. Nothing is stored

## 4.0.0 - 2026-08-01

- Skills updated to the latest account versions (American spelling pass across all three) and repackaged
- Prompts now include the skill reference, e.g. /ctc-harvest Harvest this week's events for Boston
- START-HERE is now a PDF that opens in a new tab to read on screen instead of downloading
- city-config-template is now .docx, and setup states it must be added to the Claude project's knowledge as context
- Added a sample finished issue with shading showing which blocks Claude builds and which the lead writes
- Removed the changelog section, the zip line from the download list, and the third legend item
- Rebuilt the UI on the Starbucks-inspired design system: warm cream canvas, four-tier green, pill buttons, 12px cards, layered soft shadows, sticky nav

## 4.1.0 - 2026-08-01

- ctc-assemble updated from the account: it now asks three questions before building (which events are the picks, any opportunities this week, anything the sheet cannot know) and waits for the answer. Picks come from the lead's answer rather than the skill's own ranking, and the opportunities block is omitted rather than padded when there are none
- Monday section documents the three questions so leads can have answers ready
- Friday flag guidance updated to four to six picks, and notes that marking PICK makes Monday's first question a one-line answer
- ctc-harvest and ctc-source-map unchanged; repackaged alongside for consistency

## 4.2.0 - 2026-08-01

- Sample issue now shows three categories instead of two. Picks and opportunities are marked as collaborative: the lead chooses the events and adds the asides while the skill writes the framing around them, and the lead supplies each opportunity while the skill drafts the description
- The remaining human blocks state what the skill does contribute, so no block overstates either side
