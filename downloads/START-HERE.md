# Start here

You're going to run a weekly climate events newsletter for your city. This package does most of the work.

You don't need to know how to code. You do need a paid Claude account and about two hours for setup.

---

## What you're building

Every week your newsletter goes out with a short note from you, a handful of picks, and a list of everything happening in your city. The lists are the tedious part — a mature newsletter carries 40 to 55 events, each needing a link and an emoji placed by hand.

**These skills do the lists. You write the words.**

That split is deliberate. The listings are mechanical and a tool does them better than you would at 11pm. The note and the picks are why anyone subscribes, and they need a person who actually goes to these events.

Expect roughly two hours a week once you're set up.

---

## Setup — do this once

### 1. Install the three skills

In Claude, go to **Settings → Capabilities → Skills**, and upload these three files:

- `ctc-source-map.skill`
- `ctc-harvest.skill`
- `ctc-assemble.skill`

Turn on **code execution** in the same settings area. The skills need it to build your spreadsheet and document.

### 2. Install the Claude Chrome extension

Some event sites hide their data from simple requests. Claude needs to look at those pages in a real browser — yours.

Search for "Claude for Chrome", install it, sign in with the same account.

### 3. Fill in your city config

Open `city-config-template.md`. Fill in your chapter name, timezone, which neighbouring towns count as local, who signs the newsletter, and your footer.

Takes ten minutes. Save it as `city-config.md`.

### 4. Create a Claude project

Make a new project called something like "Boston Newsletter". Upload your `city-config.md` to it.

Everything you do from now on happens inside that project, so Claude always knows your city.

---

## Setup — build your source list

**This is the most important hour you'll spend.** Everything downstream depends on it.

In your project, type:

> Build the source map for Boston.

Claude researches your city — Luma calendars, Eventbrite organisers, university calendars, incubators, city government, professional groups, arts venues — verifies each one is real and actually active, and gives you a spreadsheet of sources.

**Read what it gives you.** You live there and Claude doesn't. If it missed the obvious weekly meetup everyone goes to, say so and have it add them. Aim for 20 to 30 verified sources.

Save that file as `sources.csv` and upload it to your project too.

**Redo this every three months.** Calendars die quietly and nobody notices until the newsletter has been thin for two months.

---

## The weekly routine

Four steps. Do them on the same days every week.

### Thursday — collect (about 15 minutes of your attention)

> Harvest this week's events for Boston.

Claude sweeps every source on your list and hands you a spreadsheet. It collects **everything** — no filtering. That's on purpose.

It may ask to use your Chrome browser. Say yes; it's reading pages, not clicking anything.

### Friday — cut (about 30 minutes)

Open the spreadsheet. Delete rows.

This is your job and nobody can do it for you. Cut anything outside your scope rule, anything not really climate, anything with a dead link. If two rows are the same event from different calendars, keep the better one.

**How many events end up in your newsletter is decided right here.** There's no target. A good week is however many good events your city has.

Save it.

### Monday — write (about 45 minutes)

> Assemble the Boston issue from this sheet.

Upload your edited spreadsheet. Claude gives you two files:

- A **Word document** and an **HTML page** — same issue, both formatted to match Substack. Use whichever you prefer.

Most of it is finished: all the event listings, links, emoji, day headers, the footer.

Three parts come back as placeholders in square brackets, because Claude can't know them:

- **The opening note** — two or three sentences about your city this week. The weather, something in the news, how your last event went.
- **The picks** — Claude drafts the structure. You add the personality. Real ones read like *"make calls (and friends!)"* and *"an infrastructure tour on wheels"*. That's the difference between a newsletter and a list.
- **Opportunities** — fellowships, grants, deadlines. Keep a running list; most stay open for weeks.

Write those three. Don't let Claude write them — generated prose reads like generated prose, and readers can tell.

### Tuesday — send (about 15 minutes)

Open the HTML file or the Word document, select all, copy, paste into Substack. Formatting and links come across.

Check it once. Then send.

---

## Your first month

**Your first issue will be small.** Maybe eight events, maybe five. That's what every newsletter looks like at the start — the biggest one in this network launched with three events and a long personal note.

**Send anyway, on the same day, every week.** A thin issue that arrives beats a good issue that doesn't. The most common way these fail isn't bad writing, it's silence.

**If you miss a week**, just send the next one. No apology, no explanation. That's the house answer and it works.

**After four weeks**, look back. What took longest? What did you skip? Fix that before adding anything new.

---

## When something breaks

**Harvest returns almost nothing.** A source broke — sites change. Ask Claude which sources returned zero, and check those by hand.

**A calendar stops working.** Tell Claude to mark it `manual` in your sources file and check it yourself each week.

**Claude asks for your browser a lot.** Normal. Eventbrite in particular blocks simple requests.

**A page asks you to prove you're human.** Claude will stop and tell you. Open it yourself and paste what you see.

**The output sounds like a robot.** You skipped the writing step. Those three placeholder blocks are the whole point.

---

## What's in this package

| File | What it's for |
|---|---|
| `ctc-source-map.skill` | Finds your city's event sources. Run once, refresh quarterly |
| `ctc-harvest.skill` | Collects the week's events into a spreadsheet. Weekly |
| `ctc-assemble.skill` | Builds the issue. Weekly |
| `city-config-template.md` | Fill in once, upload to your project |
| `START-HERE.md` | This file |

Each skill carries its own reference material — house style, worked examples from real issues, the emoji vocabulary, and platform-specific techniques. You don't need anything else.

---

## The one rule

**Automate the lists. Write the words yourself.**

Everything else in here is detail.
