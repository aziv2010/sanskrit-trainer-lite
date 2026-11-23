# Sanskrit Trainer Lite — v1.3 — Corrected ambiguous exam terms

One-page, mobile-first Hebrew/Sanskrit learning PWA for Iyengar Yoga Level 1.

## Open / test

- Quick desktop test: open `index.html` in a browser. All quiz data is embedded in this file.
- Phone test and install: upload the **contents** of this folder to a static HTTPS host (for example GitHub Pages). Open that URL on Android in Chrome; use the browser menu → Add to Home screen / Install app. The web app then supports offline use after initial loading.
- To run locally on a computer: `python -m http.server 8000` from this folder; open `http://localhost:8000`.

## What's included
- 76 RIMYI 2020 Level 1 syllabus entries, including variants and optional positions; 70 raw vocabulary entries, excluding unresolved Utt from word quizzes (69 available, including Paryanka).
- Learn Asanas and Learn Words; reverse direction; all available words and all Level 1 asanas without group filtering; multiple-choice and self-check; saved progress; JSON export/import.
- Quiz answer options based on actual entries, not invented asanas.

## Important data status
- Asana names are transcribed from RIMYI 2020, pages 35–37.
- Word segmentation and Hebrew glosses come from the **provisional** project database v0.1; they have not yet been independently linguistically verified. Asana questions now use natural Hebrew pose names instead of literal word fragments. The separate component explanations and some traditional name translations remain provisional pending linguistic review.
- This is a usable prototype for feedback, not a formally validated Sanskrit learning reference.

## Storage
Progress uses browser localStorage on that origin and does not sync between devices. Export JSON periodically if important. Opening a local file and an HTTPS-hosted copy will have separate progress.

## Files
- `index.html` — main self-contained application
- `data.json` — readable data snapshot for review
- `manifest.webmanifest`, `service-worker.js`, `icon.svg` — install / offline support

## v1.2 update
Removed the “קבוצת לימוד” selector from the main screen. Both learning modes now draw from the entire available respective collection. “כיוון שאלה” remains. Unresolved Sanskrit words without vetted Hebrew meanings remain excluded from auto-graded quizzes.

## v1.3 terminology update
- Source sheet **Priyanka** is now treated as probable **Paryanka** (bed/couch), with **Paryankasana** as an additional example outside Level 1; original spelling is retained as metadata, since the paper itself was not corrected.
- **Utt** remains excluded from automated word quizzes because it could abbreviate **Uttana** or **Utthita**. Both words are already separate quiz entries.
- The source-sheet corrections and the rest of the provisional dataset should still be reviewed with the teacher; no claim is made that these are official exam answers.
- Cached PWA assets updated to cache version v4. Local progress storage key unchanged.


## v1.6 typography update
English and romanized Sanskrit now prefer Chalkboard SE Regular with system fallbacks. Hebrew retains a separate legible system-font stack. Chalkboard SE is not bundled and is generally not available on Android; Android uses a fallback. No font files are distributed.

## v1.7: Android font and Hebrew readability
- Hebrew typography: Varela Round (Google Fonts), larger across questions, answers, settings and buttons.
- Latin / transliterated Sanskrit: Patrick Hand (Google Fonts), friendlier handwritten alternative to Chalkboard SE.
- Font stylesheets are loaded via Google Fonts with local system fallbacks. On first load internet is needed to obtain the web fonts; if offline and not already cached, fallback fonts render. No font files are redistributed.
- Learning logic, progress key, and quizzes are unchanged.

## v1.8 — Approved launcher icon and Settings readability
- Android launcher artwork: approved colorful lotus + Om on a blue gradient. PNG icons at 192px and 512px plus maskable variants; updated install manifest and SVG fallback.
- Settings action labels replaced by large explicit Hebrew text plus descriptions: export, import, reset. Existing JavaScript actions and progress storage key unchanged.
- Service worker cache bumped to v8 so existing installs refresh assets. Existing v1.7 typography and learning functionality retained.
- On Android after deployment, installed app icons may be cached by the launcher; uninstall/reinstall the home-screen app if the old icon remains. Back up progress first.
