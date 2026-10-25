# 09 — Edit past Days

Status: ready-for-agent
Blocked by: 04
Spec: `../spec.md`

## What to build

A list in Settings of every past Day from the first plan's start Day to yesterday, newest first. Each row shows the Day's Pouch Count and Daily Limit, and the count can be edited. The core gets a set-past-Day command that rejects today, future Days and Days before the start. Streaks and charts reflect edits immediately.

## Acceptance criteria

- [ ] Core tests: an edit changes only that Day; edits to today, future Days and Days before the start are rejected
- [ ] Core tests: an edit that creates or removes an Over Day changes the Streak and longest Streak accordingly
- [ ] An edit in the UI shows up straight away on Today and Progress
