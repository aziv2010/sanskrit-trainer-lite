# Sanskrit Trainer Lite v2.2 — Quiz clarity and numbered options

## Modified files
- `index.html` — Embedded v2.2 data, fixed Hebrew quiz clues, numbered-option selection safeguard, Settings version label `2.2`.
- `data.json` — Hebrew quiz clues updated for 8 asanas; five of those also received revised general Hebrew names. Matsyendra/Bharadvaja/Marichi breakdown descriptions clarified.
- `service-worker.js` — cache key incremented to `sanskrit-lite-v13` for device updates.

## New files
- `UPDATE_NOTES_v2.2.md` — this report.

## Quiz behavior
- Hebrew answer choices for Ardha Matsyendrasana I now use a meaning-based description ("half lord of the fishes") rather than the phonetic transcription.
- Marichyasana I/III and Bharadvajasana I/II use meanings or identifying context rather than phonetic Sanskrit in Hebrew answer choices.
- A numbered asana now has two *additional* numbered distractors, where available (3 numbered answers among 4). This rule applies in either question direction and does not expose a correct answer through the number alone.
- The asana breakdown retains the contextual explanation about Matsyendra ("lord of the fishes").

## Notes
- `data.json` is a reference file; `index.html` embeds the data actually used by the app. Both must be copied.
- Local saved progress is not reset; no storage schema changes.
- This fix is based on the packaged v2.1 release, to retain all previous v2.1 improvements.
