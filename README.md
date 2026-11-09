# Odd-Limit Ear Trainer

A Nick Vuci applet for learning to hear just intervals, one odd limit at a time, up to the 15-odd-limit.

**Play it:** https://nickvuci.github.io/OddLimitEarTrainer/

The trainer is a single pathway. Each odd limit is broken into ratio stages, one per interval, followed by a full-limit stage for that odd limit's tonality diamond. A ratio stage starts with listening to the interval from random starting notes. Then you identify it against the nearest interval you've already covered, then against the two nearest, and finally against every interval covered so far.

## This repo is the single source of truth

| Path | What it is |
| --- | --- |
| `index.html` | **The current Odd-Limit Ear Trainer.** The single-path version. This is the live app and the only file under active development. |
| `reference/ear-trainer-classic.html` | **Reference only.** The earlier multi-mode version (Learn, Progression, Tuning). It's kept so its features can be ported into the main app, such as the options menu. |
| `reference/harmonic-ear-trainer.html` | **Reference only.** A separate harmonic ear trainer with features meant for the main app. |

The reference files are frozen snapshots. They aren't maintained, and they're published only so you can open them side by side with the main app:

- https://nickvuci.github.io/OddLimitEarTrainer/reference/ear-trainer-classic.html
- https://nickvuci.github.io/OddLimitEarTrainer/reference/harmonic-ear-trainer.html

## Running locally

Each app is a single self-contained HTML file with no build step. Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server
```

Progress and settings are saved in the browser's `localStorage`. The main app uses `olet-path-*` keys, the classic version `olet-*` and the harmonic trainer `harmtrainer`. The three apps share the `theme` key, so the light/dark choice carries across them.

## Hosting

The site is served by GitHub Pages from the root of `main`. `.nojekyll` turns off Jekyll processing.

---

Part of [nickvuci.com](https://nickvuci.com).
