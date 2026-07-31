# Climate Tech Cities — Newsletter Workflow

A mock website for the CTC newsletter production pipeline:

**Sources → Harvest → Event sheet → Assemble → You write → QA → Send → Log**

| Stage | Who runs it | Status in this mock |
|---|---|---|
| 1. Sources | Standing per-city registry, refreshed quarterly | Mock table, swaps with city |
| 2. Harvest | **Claude skill** — sweeps sources, fills the sheet | Placeholder prompt, opens in the editor's own claude.ai |
| 3. Event sheet | Human — dedupe, cut, flag picks | Mock table with PICK / CUT / DUPE tags |
| 4. Assemble | **Claude skill** — builds This Week's Events, Upcoming Events, Events in Detail | Placeholder prompt |
| 5. You write | Human — opening note, picks, opportunities, sign-off | Text areas |
| 6. QA | **Small Claude skill** — dead links, duplicates, past dates | Placeholder prompt |
| 7. Send | Email platform integration | Mock button |
| 8. Log | Issue history per city | Mock list |

## How the "runs in your Claude" part works

No API keys and no account access. Each skill button builds a prompt for the
selected city and opens `claude.ai/new?q=<prompt>` in a new tab — the editor's
own Claude account, their web search, their usage. They review the pre-filled
prompt and hit send.

The three prompts live in `SKILL_PROMPTS` inside `index.html` and are
**placeholders** — replace them with the real packaged skill instructions.

## Run it

It's a single static page — open `index.html` in a browser, or deploy the
folder to Vercel/GitHub Pages as-is.
