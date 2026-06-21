# 🎯 Darts Trainer

A self-contained web app for the core darts-counting skills:

- **Subtract** — quickly work out your remaining score after a visit (501 down).
- **Adds** — total three darts at a glance.
- **Closings** — practice finishing combinations on a tappable dartboard.
- **Full Leg** — play a whole 501 leg: subtract every visit, then check out.

Daily progress and all settings are saved locally on your device. No build
step and no runtime dependencies — just static `index.html`, `icon.svg` and a
web manifest.

## Run it

**Easiest:** open `index.html` in any browser (desktop or phone).

**Or serve it locally:**

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## How it works

### Subtract
You're shown a current score and the total you threw this visit. Type what's
left and press <kbd>Enter</kbd>. With **Chain** on, a correct answer continues
the same leg downward so it feels like a real game.

### Closings (checkouts)
You're given a checkout score (2–170). Enter a valid finishing combination —
**the last dart must be a double**. Any mathematically valid checkout is
accepted; **Reveal** shows the standard pro path.

Dart notation:

| Input | Meaning            |
|-------|--------------------|
| `T20` | treble 20 (60)     |
| `D16` | double 16 (32)     |
| `20`  | single 20          |
| `DB`  | double bull (50)   |
| `SB`  | single bull (25)   |

Separate darts with spaces, e.g. `T20 T20 DB` for 170.

### Full Leg
A complete 501 leg. Realistic visit totals are generated for you; subtract each
one, and when you reach checkout range you enter the finish to win the leg in as
few darts as possible.

Stats (accuracy, average answer time, streak) are tracked and saved in your
browser's local storage.
