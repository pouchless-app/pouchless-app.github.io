# 06 — Progress: daily bar chart

Status: ready-for-agent
Blocked by: 03
Spec: `../spec.md`

## What to build

The core gets a daily-series query: one entry per Day from the first plan's start Day to today, with the Pouch Count, the Daily Limit that applied that Day, and an Over flag.

The Progress tab draws it with Recharts:
- a bar per Day, red when Over
- the Daily Limit as a step line
- the whole tracked period, scrollable sideways and opening on the most recent weeks

## Acceptance criteria

- [ ] Core tests: the series covers every Day, including untouched Days as 0, with the correct limit per Day and correct Over flags
- [ ] The chart is readable at iPhone width with a few months of fake data, and opens scrolled to the latest Days
