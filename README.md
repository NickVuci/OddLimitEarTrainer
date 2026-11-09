# Odd-Limit Ear Trainer

A Nick Vuci applet for learning to hear just intervals, one odd limit at a time, up to the 15-odd-limit.

**Play it:** https://nickvuci.github.io/OddLimitEarTrainer/

The trainer is a single pathway. Each odd limit is broken into ratio stages, one per interval, followed by a full-limit stage for that odd limit's tonality diamond. A ratio stage starts with listening to the interval from random starting notes. Then you identify it against the nearest interval you've already covered, then against the two nearest, and finally against every interval covered so far.

### Sing it

The **Sing** button in the control bar swaps the quiz for a singing exercise on the current stage. Hear the interval, then sing its upper note over a root (an optional drone) while a live trace shows your pitch against the ratio lines. Hold it within tolerance for about a second to match it. Pick one interval or draw from every ratio the stage covers. Any octave counts, since pitch is folded into one octave above the root. It's a warm-up for recognition and never affects path progress. It needs a microphone, and headphones keep the drone out of it. The browser only offers the mic on HTTPS or localhost.

## This repo is the single source of truth

| Path | What it is |
| --- | --- |
| `index.html` | **The current Odd-Limit Ear Trainer.** The single-path version and live app. |
| `reference/ear-trainer-classic.html` | **Reference only.** The earlier multi-mode version (Learn, Progression, Tuning). It's kept so its features can be ported into the main app, such as the options menu. |
| `reference/harmonic-ear-trainer.html` | **Singing prototype.** A separate harmonic ear trainer being refined before its singing and visualization features move into the main app. |

The classic reference is a frozen snapshot. The harmonic trainer is a working prototype. Both are published so you can open them beside the main app:

- https://nickvuci.github.io/OddLimitEarTrainer/reference/ear-trainer-classic.html
- https://nickvuci.github.io/OddLimitEarTrainer/reference/harmonic-ear-trainer.html

## Running locally

Each app is a single self-contained HTML file with no build step. Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server
```

Progress and settings are saved in the browser's `localStorage`. The main app uses `olet-path-*` keys (`olet-path-sing` holds the singing tallies), the classic version `olet-*` and the harmonic trainer `harmtrainer`. The three apps share the `theme` key, so the light/dark choice carries across them.

## Hosting

The site is served by GitHub Pages from the root of `main`. `.nojekyll` turns off Jekyll processing.

---

Part of [nickvuci.com](https://nickvuci.com).
