# 🦊 NoteFox Quest

A game-like web app for children learning to read music notes, violin-first but generalized to other instruments and clefs.

## Run it

No build, no dependencies — just open `index.html` in any browser, or serve it from the project folder:

```sh
python3 -m http.server 8765
```

## Features

- **Instruments / clefs**: Violin (treble), Viola (alto), Cello (bass), Flute (treble). Add more by editing the `INSTRUMENTS` object in `index.html` — each entry is just a clef, a tone color, and a list of levels with note pools.
- **Levels**: Open Strings → Line Notes → Space Notes → Full Staff → ledger lines, with 3-star ratings saved per instrument+level (localStorage).
- **Sound feedback**: every note plays its real pitch via Web Audio synthesis (bowed-string or flute timbre), correct answers get a sparkle arpeggio, wrong answers get a gentle buzz followed by the correct pitch, and 2–3 star rounds end with a fanfare + confetti.
- **Note names**: letters (C D E…) or solfège (Do Re Mi… / Dó Ré Mi…).
- **Modes**: Practice (notes the child misses come back more often, remembered across sessions) or Quiz (perfectly even mix, for assessment).
- **Languages**: English and Português (PT-PT), auto-detected from the browser and switchable on the home screen.
- **Kid-friendly game loop**: progress bar, streak multiplier, floating emoji, praise messages, fox mascot.

Clef shapes are public-domain vector paths from Wikimedia Commons (GClef.svg, FClef.svg, CClef.svg).
