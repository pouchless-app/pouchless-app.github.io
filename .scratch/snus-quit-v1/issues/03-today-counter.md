# 03 — Today screen: Pouch counter, Daily Limit, left/Over, Phase

Status: ready-for-agent
Blocked by: 02
Spec: `../spec.md`

## What to build

The Today tab:
- today's Pouch Count shown big, with +1 and −1 buttons
- the Daily Limit, and either "N left" or "N over" (red, with no pop-ups)
- the current Phase as "Week i of N"

The core gets increment/decrement commands and a Today view query. A Day with no Day Log counts as 0, and Days roll over at local midnight. The core takes `today` as an argument and never reads the clock.

## Acceptance criteria

- [ ] Core tests: +1/−1 change only today's Pouch Count; −1 at 0 stays 0; a missing Day Log reads as 0
- [ ] Core tests: left/Over are computed correctly at, below and above the Daily Limit
- [ ] Core tests: the "Week i of N" label is right on the first Day, on a Phase boundary, and after the Quit Date
- [ ] Counts survive a reload; after midnight the screen shows a fresh Day with 0
