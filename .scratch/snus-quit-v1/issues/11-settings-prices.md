# 11 — Settings: can price, Pouches per can, currency

Status: ready-for-agent
Blocked by: 07
Spec: `../spec.md`

## What to build

Settings fields to edit can price, Pouches per can and currency symbol after onboarding, through a core update-settings command. Money Saved recomputes everywhere.

## Acceptance criteria

- [ ] Core tests: changing the price or pack size changes Money Saved and nothing else; invalid values (≤ 0, non-numeric) are rejected
- [ ] Changes persist across a reload and show on Progress
