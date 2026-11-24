# Sanskrit Trainer Lite v2.3 — Same-version answer choices

## Fixed

- A numbered asana now receives up to **two wrong answers with the same Sanskrit version numeral** (I, II, III etc.), before other distractors are selected.
- For example, *Virabhadrasana II* can now appear alongside other **II** poses instead of being the only answer meaning “second”.
- The same rule applies in both Sanskrit-to-Hebrew and Hebrew-to-Sanskrit questions, including Hebrew forms like “השנייה” and “גרסה שנייה”. The numeral is determined from the source asana name, not by searching answer text.
- If there are too few same-version alternatives, fall back to other numbered asanas, then to general choices.
- Settings version label preserved and updated to **2.3**.
- Service-worker cache changed to `sanskrit-lite-v14` to help installed applications retrieve the new files.

## Files to copy

- **Modified** `index.html`
- **Modified** `service-worker.js`
- **New** `UPDATE_NOTES_v2.3.md`

`data.json` is **unchanged** from v2.2, so do not replace it.

## Limits

- This fix changes multiple-choice construction, not any vocabulary or translation.
- Browser-level Android testing has not been performed.
