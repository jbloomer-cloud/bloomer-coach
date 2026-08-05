# REPS - training PWA

Single-file training app. Everything lives in `index.html` (HTML + CSS + one
inline `<script>`). Hosted on GitHub Pages. No build step, no framework.

## Hard rules - never break these
- Dates: use the existing `localDateStr(d)` helper, never `toISOString()` for
  day keys. toISOString() shifts the day in BST and corrupts logs.
- Escape apostrophes inside single-quoted JS strings. A stray apostrophe breaks
  the whole inline script and the app fails to load.
- Modals stay OUTSIDE the `.scroll` container, or iOS Safari breaks fixed
  positioning.
- No service worker. Do not add one.
- The duplicate `fmt` definition is intentional. Leave both. Do not deduplicate.
- Single file only. No modules, no dependencies, no CDN links.

## State
- All state is the `ST` object, saved to localStorage under key `BLMv2`.
- Call `save()` after any state mutation.
- Lazy init pattern: `if(!ST.x)ST.x=...`. There is no defaults object.
- `ST.ergPRs` (row1k/row2k/skiErg1k/skiErg2k) feeds `calcErgSplits`. Never
  write anything else into those fields.

## Workflow - every time
1. Describe the plan and wait for my approval before editing.
2. After editing, validate by extracting the inline script and running
   `node --check` on it. Never finish without doing this.
3. Commit and push to main. GitHub Pages deploys automatically.
4. One feature per commit. Preserve existing behaviour unless asked otherwise.
5. If something is risky or might break on load, tell me instead of shipping it.
