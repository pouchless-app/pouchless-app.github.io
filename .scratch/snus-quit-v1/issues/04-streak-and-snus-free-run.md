# 04 — Streak and Snus-free run on Today

Status: ready-for-agent
Blocked by: 03
Spec: `../spec.md`

## What to build

The core computes:
- the **Streak**: consecutive Days ending today that are not Over; 0 if today is Over
- the **longest Streak**, worked out from the full history
- the **Snus-free run**: consecutive Snus-free Days ending today

Today shows the Streak with a flame. Once the user is in the zero Phase, it also shows the Snus-free run.

## Acceptance criteria

- [ ] Core tests: the Streak counts today while today is within the limit; it drops to 0 the moment today goes Over; an Over Day in the past ends the Streak there
- [ ] Core tests: the longest Streak survives a broken current Streak
- [ ] Core tests: the Snus-free run counts only zero Days and stops at the most recent non-zero Day
- [ ] Today shows the flame and the Streak count, and shows the Snus-free run in the zero Phase
