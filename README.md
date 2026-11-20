# Review progress dashboard

A one-page static site. Everything shown comes from `data.json`; `index.html` never needs editing.

## How to update

1. Open `data.json` in the GitHub repository and click the pencil (Edit) icon.
2. Change the numbers or text, for example:
   - `"last_updated"`: today's date (YYYY-MM-DD).
   - `"current_step"`: what you are working on now.
   - `phases[].progress`: 0 to 100 for each phase. Overall progress is calculated from these (weighted by `weight`).
   - `prisma`: replace a `null` with a number once it is known (for example `"included": 42`). `null` shows as "Pending".
   - `agreement`: set `"value": "κ = 0.82"` and `"status": "done"` when a kappa is computed.
   - `tasks[].status`: `next`, `active`, `planned` or `done`.
3. Click "Commit changes". The live page updates in about a minute.

Keep commas and quotes intact; if the page shows "Could not load data.json", a comma or quote was probably removed.

## Privacy

Public page: no emails, no reviewer or adjudicator names (roles only), no record-level data.
