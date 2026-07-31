# Operational Playbook — Chapter: City Newsletters

> Draft for the CTC Operational Playbook. Two parts, per manager direction:
> **Part 1** — how to launch a new city newsletter. **Part 2** — the full weekly
> production process. The NYC newsletter is the pilot used to validate every step
> below before this chapter is considered final.

---

## Part 1 — Launching a New City Newsletter

### 1.0 Readiness check (before anything else)

A city newsletter launches only when all four are true:

- [ ] A chapter lead (or interim editor) owns the newsletter and can commit ~3 hrs/week
- [ ] At least 8–10 recurring event sources exist for the city (see 1.1)
- [ ] A starting audience exists — chapter members, Luma calendar subscribers, or a partner list
- [ ] The first three issue dates are on the calendar

### 1.1 Build the source registry

The registry is a standing, per-city list of everywhere events come from. It is
set up once at launch and refreshed quarterly. Harvest sweeps exactly this list —
if a source isn't in the registry, its events don't exist.

Source types to cover (aim for 8–15 total):

| Type | Examples | Notes |
|---|---|---|
| Luma calendars | City climate calendar, org calendars | Highest quality; start here |
| Eventbrite feeds | "climate" + city search | Noisier; expect fetch friction |
| Meetup groups | Climate tech, cleantech, energy groups | |
| University calendars | Public lectures, sustainability centers | Refresh each semester |
| Org event pages | Cleantech alliances, incubators, accelerators | |
| Government/civic | City sustainability office, utilities | Low volume, high credibility |

Registry columns: **Source name · Type · URL · Fetch tier (plain fetch / browser / paste) · Last refreshed · Owner**

Quarterly refresh: verify each URL still resolves, drop dead sources, add new ones
surfaced during the quarter (the sheet's Source column shows which registries are pulling weight).

### 1.2 Set up the infrastructure

1. **Event sheet template** — copy the master template: the 14 standard columns
   (as specified in the climate week export format) **plus the `Block` column**
   (`this_week` / `upcoming`) used only for weekly issues.
2. **Skills** — the three production skills are city-parameterized, not city-specific:
   - `ctc-harvest` — pass the city and timezone (e.g. `--tz EDT` for NYC)
   - `ctc-assemble` — produces the nine-section draft from the curated sheet
   - `ctc-qa` — pre-send checks
3. **Email platform** — create the city list/publication, install the newsletter
   template (nine sections in canonical order, see 2.3), set the sender identity.
4. **Log** — create the city's issue log tab (see 2.6).

### 1.3 Pilot issues

Run **two full dry runs** before the first public send:

- Dry run 1: full pipeline, internal recipients only. Expect source problems —
  this is where fetch tiers get assigned per source.
- Dry run 2: fix what broke, run again, and time each stage. If the whole cycle
  exceeds ~3 hours of human time, cut sources or tighten curation rules before launch.

### 1.4 Launch checklist

- [ ] Registry complete, every source fetch-tested
- [ ] Two dry runs done, stage timings recorded
- [ ] First issue's opening note drafted by the chapter lead (voice is set locally, from issue one)
- [ ] Subscribe path live and linked from chapter channels
- [ ] Issue #1 date announced to chapter

---

## Part 2 — Weekly Production Process

### 2.0 The pipeline

**Sources → Harvest → Event sheet → Assemble → You write → QA → Send → Log**

| Stage | Who | Time budget |
|---|---|---|
| Harvest | Skill (`ctc-harvest`) | 15 min supervision |
| Curate sheet | Editor | 30–45 min |
| Assemble | Skill (`ctc-assemble`) | 10 min supervision |
| Write human sections | Editor | 45–60 min |
| QA | Skill (`ctc-qa`) + editor review | 15 min |
| Send + log | Editor | 10 min |

Suggested weekly rhythm (adjust per city; send day fixed per city):
**Day 1** harvest + curate · **Day 2** assemble + write · **Day 3** QA + send + log.

### 2.1 Harvest

Run `ctc-harvest` for the city. It sweeps the source registry and outputs the
event sheet in the standard 14-column format plus `Block`, with the controlled
vocabularies (Event Type: In-person/Hybrid/Online; the four Access values; the
22-category list). Escalation is tiered: plain fetch → browser fetch (for empty
shells or 403s) → manual paste. CAPTCHA is a hard stop: the skill reports and
moves on; the editor decides whether the source is worth manual effort.

Harvest **warns, never silently fixes**: missing dates, missing links,
off-vocabulary values, and invented categories get flagged for the editor.

Target volume for a weekly issue: **15–20 events for this week, 25–40 upcoming**
(next 2–3 weeks). If harvest returns far more, tighten curation; far less,
check the registry.

### 2.2 Curate the event sheet

The editor's judgment stage — never automated:

1. **Dedupe** — same event from multiple sources: keep the row with the best link, mark the rest DUPE.
2. **Cut** — off-topic, low-quality, or generic webinars: mark CUT with a one-word reason.
3. **Flag picks** — 2–4 events marked PICK; these drive the Picks section and Events in Detail.
4. **Resolve harvest warnings** — fill missing dates/links or cut the row.

### 2.3 Assemble

Run `ctc-assemble` on the curated sheet. It produces the full draft skeleton in
the canonical nine-section order — note that **the sign-off sits mid-document,
not at the end**:

1. **Opening note** — *placeholder; human writes*
2. **Picks for the week** — skill drafts from PICK rows; runs directly out of the opening note ("Here are our picks for the week:")
3. **Housekeeping** — *placeholder; human writes as needed*
4. **Sign-off** — "'Til next week!" — fixed position, after housekeeping
5. **Opportunities** — *placeholder; human curates*
6. **This Week's Events** — skill, from `this_week` rows; short punchy entries
7. **Upcoming Events** — skill, from `upcoming` rows; one line each
8. **Events in Detail** — skill, PICK rows only; ~3 sentences / 50–70 words each (weekly length, not the ~177-word climate-week guide length)
9. **Footer** — CTC + Streetlife Ventures startup and talent platforms; fixed template

Sections 2, 6, 7, 8 come out styled on past issues but never verbatim from them.

### 2.4 You write (stays human)

The editor writes: the **opening note** (voice of the newsletter), any
**housekeeping**, the **opportunities** section (jobs, grants, calls for
speakers — sourced from chapter channels, not harvested), and tweaks the
drafted picks so the "why this one" is genuinely theirs.

Rule of thumb: if a reader could tell a machine wrote it, it belongs to the
editor. If it's a listing, it belongs to the skill.

### 2.5 QA

Run `ctc-qa` on the full draft. It checks: dead/malformed links (verified live),
duplicate events across blocks, past-dated events, and date/venue mismatches
against the sheet. Output is a numbered issue list or CLEAN. The editor fixes
and re-runs until CLEAN, then does one final human read top-to-bottom.

### 2.6 Send and log

Send via the city's email platform. Then log the issue immediately:

**Issue # · Date sent · Events harvested · Events published · Picks · Open rate (added later) · Notes (what broke, source problems, timing)**

The Notes column is what makes the quarterly registry refresh and playbook
revisions evidence-based rather than guesswork.

---

## Validation plan (NYC pilot)

1. Run one full NYC issue with this chapter open, following it literally.
2. Anywhere reality diverges from the chapter, fix the chapter, not the process notes.
3. After two consecutive smooth issues, submit the chapter for the playbook.
