# 10 — Replan

Status: ready-for-agent
Blocked by: 02, 04
Spec: `../spec.md`

## What to build

A Replan action in Settings. It reuses the onboarding plan inputs and live preview, and starts a new Quit Plan today. Past Days keep the Daily Limits of the plan that covered them. If the old plan started today, it is discarded. The Streak is not reset by a Replan. Pouches Avoided keeps using the first plan's Starting Usage.

## Acceptance criteria

- [ ] Core tests: after a Replan, past Days return the old limits and today onward return the new ones
- [ ] Core tests: replanning on the old plan's own start Day leaves only the new plan
- [ ] Core tests: the Streak is unchanged by the Replan itself; Pouches Avoided still uses the first Starting Usage
- [ ] The UI asks for confirmation with the preview before replacing the plan
