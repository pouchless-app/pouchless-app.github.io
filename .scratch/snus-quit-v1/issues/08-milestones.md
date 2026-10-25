# 08 — Milestones

Status: ready-for-agent
Blocked by: 04, 07
Spec: `../spec.md`

## What to build

The fixed Milestone list from the spec:
- first Day within the limit
- Streak of 3, 7, 14 and 30 Days
- a Phase finished with no Over Days
- Quit Date reached
- first Snus-free Day, then Snus-free runs of 7, 30, 100 and 365
- Money Saved of 1 can and 10 cans

The core checks them after every command and on app open, stores newly earned ones with the Day they were earned, and never takes them back. Conditions based on how Days turned out use completed Days only (yesterday and earlier). Quit Date reached is earned on the Quit Date itself.

The UI:
- a celebration screen for each newly earned Milestone
- a Milestones tab showing earned ones highlighted and locked ones greyed out with their condition

## Acceptance criteria

- [ ] Core tests: each Milestone triggers on its condition and not before
- [ ] Core tests: nothing is earned from today's still-open Day, except Quit Date reached
- [ ] Core tests: an earned Milestone stays earned after a past-Day edit or a broken Streak
- [ ] Commands report newly earned Milestones; the UI celebrates each one once
- [ ] The Milestones tab lists every Milestone with the right state
