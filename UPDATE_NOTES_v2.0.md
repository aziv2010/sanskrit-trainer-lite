# Sanskrit Trainer Lite v2.0 — Reviewed Vocabulary Update

Based on the user-supplied `fixes_for_developer.json`, applied strictly to `data.reviewed-proposal.json`, with every `from` field verified before modifying.

- Applied **68 field changes** across **16 word records** and **15 asana records**.
- Added **2 glossary words**: Ugra and Brahmacharya; **72 words total**, **76 asanas**.
- Added `quiz_he` only where necessary to avoid the Hebrew question revealing a Sanskrit name; original user-approved `he` preserved for explanations.
- Resolved Marichi/Marichya via `compound_form` for asana breakdown and examples.
- Excluded Paryanka (`uncertain=true`) and Utt (empty meaning) from automatic quizzes.
- Displays literal meanings and alternate names (when provided) in the answer breakdown, not the question.
- Preserved existing progress IDs and localStorage key; new terms naturally start unlearned.
- Preserved the user-requested `.app-version` CSS class under Settings and set the label to Version 2.0; advanced the offline service worker cache to v11 so the updated HTML refreshes on installed devices.

**Important:** Settings **Import Progress** accepts only `iyengar-sanskrit-lite-backup` progress files, not `data.json` or correction patches. Publish the full app update via GitHub Pages.

**Review items:** The submitted patch states that `W-043 Paryanka` remains unresolved against `Priyanka` in an example exam. Its `uncertain=true` is respected. The patch also notes 46 original words with `exam=false`; these have not been reclassified. Source-level Sanskrit accuracy was not independently revalidated in this implementation pass.

## Files to copy into your local Git repository (v1.9 → v2.0)

| File | Action | Reason |
|---|---|---|
| `index.html` | Modified | Embedded corrected data, version display with `.app-version`, quiz compatibility updates |
| `data.json` | Modified | Reviewed translations, new words and metadata |
| `service-worker.js` | Modified | Updated offline cache identifier (`sanskrit-lite-v11`) |
| `README.md` | Modified | Updated application documentation |
| `UPDATE_NOTES_v2.0.md` | New | Release notes and deployment instructions |

All other packaged assets are unchanged from the previous v2.0 archive. The complete ZIP includes unchanged installation icons and manifest for convenience.
