# Sanskrit Trainer Lite v2.1 — Asana component-meaning correction

## Issue resolved
The Asanas mode word-by-word explanation used the general `words[].he` glossary text.
For the derived name component `Marichya` in Marichyasana I/III, that text was not a suitable explanation in context.

## Changes
- Introduced optional `words[].asana_part_he` for a precise **asana breakdown** meaning; retained `he` and `quiz_he` unchanged.
- `Marichya` (from `Marichi`) now displays **של מריצ׳י — שם של חכם; פירוש השם: קרן אור**.
- Added context-specific breakdown text for Bharadvaja, Garuda, Matsyendra and Virabhadra.
- Verified that all component names used in all 76 Level 1 asanas resolve to nonempty Hebrew meanings, including compound form `Marichya`.
- Settings displays **Sanskrit Trainer Lite — Version 2.1** using the existing `.app-version` styling.
- Updated offline cache name to `sanskrit-lite-v12`.
- No changes to progress storage or existing progress IDs.

## Files to copy into your local Git repository (v2.0 → v2.1)
| File | Change |
|---|---|
| `index.html` | Modified: embedded data, asana decomposition renderer, Settings version |
| `data.json` | Modified: asana-specific meanings and version |
| `service-worker.js` | Modified: offline cache version |
| `UPDATE_NOTES_v2.1.md` | New: release notes |

All other app files are unchanged.

Suggested commit: `Fix asana word breakdown meanings in v2.1`
