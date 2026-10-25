# 07 — Progress: weekly average and headline numbers

Status: ready-for-agent
Blocked by: 04, 06
Spec: `../spec.md`

## What to build

The core computes:
- weekly averages in 7-Day buckets from the first plan's start Day, with the current partial week averaged over the Days elapsed so far
- **Pouches Avoided** = first Starting Usage × Days tracked (including today) − total Pouches, floored at 0
- **Money Saved** = Pouches Avoided × can price ÷ Pouches per can

The Progress tab shows:
- a weekly average line with Starting Usage as a dashed reference line
- headline numbers: current Streak, longest Streak, Snus-free run, Money Saved (with the currency symbol) and Pouches Avoided

## Acceptance criteria

- [ ] Core tests: bucket boundaries are right and a partial week averages correctly
- [ ] Core tests: Pouches Avoided never goes below 0, always uses the first plan's Starting Usage, and Money Saved uses the price per Pouch
- [ ] Both charts and all five numbers show on Progress
