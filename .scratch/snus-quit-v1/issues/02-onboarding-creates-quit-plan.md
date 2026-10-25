# 02 — Onboarding creates the Quit Plan

Status: ready-for-agent
Blocked by: 01
Spec: `../spec.md`

## What to build

The first end-to-end slice through the domain core.
- Define the versioned Stored Data shape: settings, Quit Plans, Day Logs and earned Milestones (the spec's Implementation Decisions list the contents).
- Write the storage adapter that loads and saves it from `localStorage`.
- Implement plan generation in the core: Starting Usage S and N weeks give weekly Phases with Daily Limit = max(1, round(S × (1 − i/N))) for i < N, and a zero Phase that starts on the Quit Date and never ends.
- Build the onboarding screen: Starting Usage, "quit in N weeks" (1–12, default 6) with a live Phase preview, can price, Pouches per can (default 20) and currency symbol (default "kr").

The app shows onboarding whenever there is no Quit Plan. Finishing onboarding saves the plan, which starts today, and opens the Today tab.

## Acceptance criteria

- [ ] Core tests: S = 10, N = 5 gives 8, 6, 4, 2, 0; the limit never drops below 1 before the zero Phase; limits never increase; N = 1 gives just the zero Phase starting today; the Quit Date is start Day + 7(N−1)
- [ ] Core tests: the Daily Limit query returns the right value for any Day in any Phase, including Days long after the Quit Date
- [ ] The preview updates live while S and N change
- [ ] After onboarding, reloading the app keeps the plan and skips onboarding
