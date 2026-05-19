# MyDetails

Live data feed for my personal portfolio webapp (M-BIOS).

The webapp at runtime fetches `data.json` from this repo's `main` branch via:

    https://raw.githubusercontent.com/shakthimaharaja/MyDetails/main/data.json

Editing `data.json` and committing to `main` updates the live site within seconds — no rebuild, no redeploy.

## Schema

`data.json` is a single JSON object with the following top-level keys:

- `profile`         — name, title, role, location, status
- `details`         — email, github, linkedin, work auth, years, domains
- `summary`         — string[] (5 bullet lines)
- `skillGroups`     — [{ label, items: string[] }]
- `jobs`            — work history entries
- `projects`        — pet projects
- `education`       — degrees
- `achievements`    — string[]
- `currentLearning` — string[]
- `photos`          — [{ src, alt }]

All fields are optional — missing keys fall back to the bundled defaults inside the webapp.
