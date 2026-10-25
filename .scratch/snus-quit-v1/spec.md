# Snus Quit v1

Status: ready-for-agent

See `GLOSSARY.md` for the meaning of capitalised terms and `docs/adr/0001-local-only-pwa-instead-of-native-ios.md` for why this is a PWA.

## Problem Statement

I take snus every day and want to quit. Willpower alone hasn't worked: I lose track of how many Pouches I actually take, I have no plan for cutting down, and nothing makes small wins feel like progress. Existing apps are bloated, want accounts, or aren't built around stepping down to zero.

## Solution

A small personal app on my iPhone home screen. I tap +1 each time I take a Pouch. During onboarding the app builds a Quit Plan from my Starting Usage and how many weeks I want to take: one-week Phases whose Daily Limit steps down to zero. The Today screen shows how many Pouches I have left today, my Streak, and a Motivational Quote. A Progress screen charts every Day I've tracked against the plan, plus how many Pouches I've avoided and the money I've saved. Milestones reward the wins along the way. Everything stays on the phone; I can export a backup file.

## User Stories

### Onboarding and the Quit Plan

1. As a new user, I want the app to open onboarding the first time, so that I can't land on an empty home screen without a plan.
2. As a new user, I want to enter my Starting Usage, so that the plan starts from where I really am.
3. As a new user, I want to choose to quit in N weeks (1–12, default 6), so that I control how aggressive the plan is.
4. As a new user, I want a live preview of the Phases as I change Starting Usage or N, so that I can see what each week will ask of me before I commit.
5. As a new user, I want the first Phase to start today with a Daily Limit already below my Starting Usage, so that I start making progress right away.
6. As a new user, I want the Daily Limit to step down evenly and reach zero on the Quit Date, so that each week is a manageable step.
7. As a new user, I want Daily Limits never to go up from one Phase to the next, so that the plan always moves toward zero.
8. As a new user, I want to enter the price of a can, how many Pouches a can holds (default 20), and a currency symbol (default "kr"), so that the app can show Money Saved.
9. As a user, I want the final Phase (zero) to continue indefinitely after the Quit Date, so that the app keeps supporting me once I've quit.

### Logging

10. As a user, I want to tap +1 each time I take a Pouch, so that I don't have to remember my count at the end of the day.
11. As a user, I want to tap −1 to undo an accidental tap, so that my count stays accurate.
12. As a user, I want the Pouch Count never to go below zero, so that a stray tap can't create nonsense data.
13. As a user, I want a new Day to start at local midnight, so that each Day's count is unambiguous.
14. As a user, I want a Day I never touched to count as zero Pouches, so that Snus-free Days need no extra action.
15. As a user, I want the app to keep counting when I go Over, so that my data stays honest.
16. As a user, I want to see clearly when I'm Over (e.g. "1 over" in red) without pop-ups or nagging, so that I'm informed but not shamed.
17. As a user, I want to edit the Pouch Count of any past Day since my plan started, so that I can fix mistakes or fill in a Day I forgot.
18. As a user, I want to be unable to edit future Days or Days before my plan started, so that the history stays meaningful.

### Today screen

19. As a user, I want today's Pouch Count shown big with +1 and −1 buttons, so that logging is one tap.
20. As a user, I want to see today's Daily Limit and how many Pouches I have left, so that I can pace myself through the day.
21. As a user, I want to see which Phase I'm in ("Week 3 of 6"), so that I know where I am in the plan.
22. As a user, I want to see my Streak with a flame, so that I feel motivated not to break it.
23. As a user in the zero Phase, I want to see my run of consecutive Snus-free Days, so that I can see how long I've been off snus.
24. As a user, I want a Motivational Quote each Day, so that I get a small bit of encouragement.
25. As a user, I want the same quote all Day no matter how often I open the app, so that it feels like the Day's quote.
26. As a user, I want quotes not to repeat until I've seen the whole list, so that they stay fresh.

### Streaks

27. As a user, I want my Streak to count consecutive Days, up to and including today, that were not Over, so that staying within the plan is what's rewarded.
28. As a user, I want my Streak to break as soon as today goes Over, so that the display is always truthful.
29. As a user, I want my longest Streak remembered, so that a broken Streak doesn't erase my best.
30. As a user, I want Streaks recalculated when I edit a past Day, so that they always match my data.
31. As a user, I want a Replan not to reset my Streak, so that adjusting the plan isn't punished.

### Progress

32. As a user, I want a daily bar chart of every Day I've tracked, so that I can see my whole journey at once.
33. As a user, I want Over Days shown in red on that chart, so that slips are visible.
34. As a user, I want the Daily Limit drawn as a step line on the daily chart, so that I can compare each Day with what the plan asked.
35. As a user, I want the daily chart to open on the most recent weeks and scroll sideways, so that it stays readable after months of data.
36. As a user, I want a weekly average line across the whole tracked period, so that I can see the trend through day-to-day noise.
37. As a user, I want my Starting Usage drawn as a dashed reference line on the weekly chart, so that I can see how far I've come.
38. As a user, I want headline numbers for current Streak, longest Streak, Snus-free run, Money Saved and Pouches Avoided, so that I get the summary at a glance.
39. As a user, I want Pouches Avoided and Money Saved measured against my first Starting Usage, so that replanning can't quietly shrink my numbers.
40. As a user, I want Pouches Avoided and Money Saved never shown below zero, so that a rough start doesn't show negative savings.

### Milestones

41. As a user, I want to earn a Milestone for my first Day within the Daily Limit, so that the first success is celebrated.
42. As a user, I want Milestones for 3-, 7-, 14- and 30-Day Streaks, so that consistency is rewarded.
43. As a user, I want a Milestone for finishing a Phase without any Over Days, so that each clean week counts.
44. As a user, I want a Milestone for reaching my Quit Date, so that the big moment is marked.
45. As a user, I want Milestones for my first Snus-free Day and for 7, 30, 100 and 365 Snus-free Days in a row, so that staying quit is rewarded.
46. As a user, I want Milestones for saving a can's worth and ten cans' worth of money, so that the savings feel real.
47. As a user, I want a celebration screen when I earn a Milestone, so that the moment feels good.
48. As a user, I want a Milestones screen with earned ones highlighted and locked ones greyed out with their condition, so that I know what to aim for.
49. As a user, I want earned Milestones to stay earned even if I later edit a Day or break a Streak, so that rewards are never taken away.

### Settings and plan changes

50. As a user, I want to Replan from Settings with fresh Starting Usage and N weeks, so that I can adjust a plan that's too hard or too easy.
51. As a user, I want a Replan to start today and leave past Days with the Daily Limits they had, so that my history stays accurate.
52. As a user, I want to see the new plan's Phase preview before confirming a Replan, so that I know what I'm committing to.
53. As a user, I want to change the can price, Pouches per can and currency symbol, so that Money Saved stays correct when prices change.
54. As a user, I want a list of past Days in Settings where I can edit each Pouch Count, so that corrections are easy to find.
55. As a user, I want to export all my data to a JSON file, so that I have a backup if the app is deleted.
56. As a user, I want to import a previously exported file, so that I can restore my history.
57. As a user, I want an import of an invalid file to be rejected without touching my current data, so that a bad file can't wipe my history.

### App shell

58. As a user, I want to install the app to my iPhone home screen and have it open full-screen, so that it feels like a real app.
59. As a user, I want the app to work offline, so that logging never depends on signal.
60. As a user, I want the app to follow my phone's light/dark setting, so that it's comfortable at night.
61. As a user, I want a bottom tab bar with Today, Progress, Milestones and Settings, so that everything is one tap away.

## Implementation Decisions

- **Platform** (ADR-0001): a Progressive Web App built with Vite, React and TypeScript, installable via `vite-plugin-pwa` (manifest plus service worker for offline use). Hosted on GitHub Pages from a new public repository `pouchless-app.github.io` owned by the `pouchless-app` GitHub organization, served at https://pouchless-app.github.io (root path), so neither the username nor "snus" appears in the URL, deployed by a GitHub Actions workflow. Mobile-only layout, follows the system colour scheme, single green accent, simple generated icon, home-screen name "Pouchless" (the name avoids the word snus so the phone doesn't advertise it). English only.
- **Modules:**
  - **Domain core**: pure TypeScript with no React, browser or storage dependencies. All rules live here. This is the app's single test seam.
  - **Storage adapter**: thin load/save of the Stored Data to `localStorage` under one key. No logic.
  - **UI**: React screens that call the core and display its results. Charts use Recharts.
- **Stored Data** is the core's whole state, one versioned object:
  - `schemaVersion`
  - settings: can price, Pouches per can, currency symbol
  - Quit Plans: every plan ever made, each with Starting Usage, start Day, N weeks and resulting Phases
  - Day Logs: a map from local Day key (`YYYY-MM-DD`) to Pouch Count. Missing Days count as zero.
  - earned Milestones: each with the Day it was earned

  The export file is exactly this object, serialised as JSON.
- **Core interface** (shape, not final names):
  - **Queries** take `(storedData, today)` and return: the Today view (Pouch Count, Daily Limit, left/Over, Phase "i of N", Streak, Snus-free run, quote), the Progress view (daily series with each Day's limit and Over flag, weekly averages, Starting Usage reference, headline numbers), and the Milestones view (each Milestone with earned/locked and its condition text).
  - **Commands** take the current Stored Data and return new Stored Data: increment today, decrement today (floored at 0), set a past Day's Pouch Count, complete onboarding, Replan, update settings, and import (validate, then replace). Commands return the Milestones newly earned by the change so the UI can celebrate them.
  - `today` is always passed in. The core never reads the clock.
- **Plan generation:** with S = Starting Usage and N weeks, Phase i (i = 1…N−1) covers Days 7(i−1) to 7i−1 from the start Day, with Daily Limit = max(1, round(S × (1 − i/N))). Phase N starts on the Quit Date (start Day + 7(N−1) days), has Daily Limit 0, and is open-ended. With N = 1 the plan is just the zero Phase starting today. Example: S = 10, N = 5 gives 8 → 6 → 4 → 2 → 0.
- **Replan:** the new plan starts today. The previous plan applies only to Days before today. A plan replaced on its own start Day is discarded. A Day's Daily Limit always comes from the plan that covered it. Only the first plan's Starting Usage is used for Pouches Avoided.
- **Day range:** tracking starts on the first plan's start Day. Past-Day edits are allowed from that Day to yesterday. Today changes only through +1/−1.
- **Streak:** consecutive Days ending today that are not Over. If today is Over, the Streak is 0. The longest Streak is computed from the full history, not stored.
- **Snus-free run:** consecutive Snus-free Days ending today.
- **Pouches Avoided** = first Starting Usage × number of Days from the first start Day to today inclusive − total Pouches over those Days, floored at 0. **Money Saved** = Pouches Avoided × (can price ÷ Pouches per can).
- **Weekly averages:** 7-Day buckets counted from the first plan's start Day. The current partial week averages only the Days elapsed so far.
- **Motivational Quotes:** about 60 short, original lines written for quitting, with no attributions. The quote index is (days since a fixed epoch) mod list length, so the quote is stable all Day and cycles through the whole list.
- **Milestones:** fixed list: first Day within limit; Streak of 3, 7, 14 and 30; Phase finished with no Over Days (any non-zero Phase of any plan, once all 7 of its Days are past); Quit Date reached; first Snus-free Day; Snus-free runs of 7, 30, 100 and 365; Money Saved ≥ one can's price; Money Saved ≥ ten cans' price.
  - Conditions that depend on how a Day turned out are checked against **completed Days only** (yesterday and earlier), so nothing is earned at 00:01 just because today is still empty. Quit Date reached is earned on the Quit Date itself.
  - Milestones are checked after every command and on app open. Earned ones are stored and never revoked.
- **Over display:** today's count turns red with "N over". There are no modals or alerts.
- **Import:** parse, check `schemaVersion` and shape, and replace the Stored Data only if valid. Otherwise show an error and leave the data unchanged.

## Testing Decisions

- Tests use Vitest and go **only through the domain core's public interface**: "given this Stored Data and this `today`, the query returns X" and "this command on this Stored Data produces Stored Data whose queries return Y". No tests reach into internal helpers. Tests should survive any internal refactor.
- What gets covered:
  - plan generation, including rounding, the minimum of 1 before zero, N = 1, and a Quit Date that falls on today
  - Daily Limit lookup across Replans
  - left/Over
  - −1 floored at zero
  - Streak and longest Streak, including Over today, edits to past Days and Replan
  - Snus-free run
  - Pouches Avoided and Money Saved, including the floor at 0 and always using the first Starting Usage
  - weekly buckets, including a partial week
  - the quote being stable within a Day and cycling through the list
  - each Milestone condition, the completed-Days-only rule, and earned Milestones never being revoked
  - import validation and an export → import round-trip
- The storage adapter and React screens have no automated tests. They are checked by hand in the browser and on the phone after install.
- The repo has no existing tests, so there is no prior art. The core's tests set the pattern.

## Out of Scope

- Notifications and reminders
- Streak freezes or repairs
- XP and levels
- Tracking nicotine strength or tapering by strength
- Hand-editing individual Phases
- Accounts, backend, sync between devices, multiple users
- Localization
- Craving or trigger journaling
- Home-screen widgets and a native iOS app
- Backfilling Days before the first plan started

## Further Notes

- Data loss is the main risk of a local-only app (ADR-0001). Export/Import is the mitigation, and the Settings screen should make it easy to find.
- Days are local calendar Days. Travelling across time zones is not handled specially; a past-Day edit fixes any oddity.
- The completed-Days-only rule for Milestones was not explicitly discussed. It follows from the decision that an untouched Day counts as zero, which would otherwise award Milestones at the very start of a Day.
