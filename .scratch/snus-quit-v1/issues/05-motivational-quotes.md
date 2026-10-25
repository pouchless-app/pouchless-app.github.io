# 05 — Motivational Quotes

Status: ready-for-agent
Blocked by: 03
Spec: `../spec.md`

## What to build

About 60 short, original Motivational Quotes written for someone quitting snus, with no attributions. The core picks today's quote as (days since a fixed epoch) mod list length. Today shows it.

## Acceptance criteria

- [ ] At least 60 quotes, each short enough to fit the Today screen without scrolling
- [ ] Core tests: the same Day always gives the same quote; N consecutive Days (N = list length) give every quote exactly once
- [ ] The quote appears on Today
