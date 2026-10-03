# Yale Physics Funding Finder

Grants, fellowships, jobs and student programs for every research area and career stage in the Yale Department of Physics, with Yale's internal and limited-submission deadlines.

- **Live page (updated automatically):** https://claude.ai/artifact/J4VAT4KTPbXMyMqZJgb5gs
- **On GitHub Pages:** https://chiaramingarelli.github.io/yale-physics-funding-finder/
- **This repository:** a self-contained copy you can read, download or host yourself.

## Use it

`index.html` is a single file with all its data built in. Open it in a browser, or publish it with GitHub Pages (Settings → Pages → Deploy from branch → `main`, folder `/`).

On a self-hosted copy everything works for everyone, including:

- filters by research area, career stage, status, type and deadline window
- a **New** tag on programs added in the last 7 days ("New this week", or search for `new`)
- tick boxes to export only the programs you care about as a calendar file (`.ics`, with reminders 6 and 4 weeks before each deadline) or a CSV
- per-program **Google Calendar**, **Outlook** and **Apple Calendar** links

## Data

`data/programs.json` has 648 programs, each taken from the funder's own page. Main fields: `n` name, `f` funder, `c` type, `s` status (open, rolling, watch, closed), `d` next deadline, `dt` deadline note, `a` award, `e` eligibility and notes, `u` official link, `stages` (ug, gr, pd, fj, tt, ten), `added` date added, `checked` date last checked, `unv` anything that could not be confirmed.

The live page reads the shared catalog directly; `data/programs.json` is the snapshot embedded in `index.html`. `engine/export_mod.js` is the export and calendar-link code inlined in the page.

This copy is a snapshot. The live page is rechecked every Monday, with new postings added on Wednesdays and Fridays. Deadlines move, so check the funder's page before you commit to a date.
