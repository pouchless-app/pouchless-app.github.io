# Snus Quit

A personal app for quitting snus: count the pouches you take each day, follow a step-down plan to zero, and see your progress over time.

## Language

### Tracking

**Pouch**:
One snus pouch taken. The only unit the app counts; nicotine strength is not tracked.
_Avoid_: Dose, portion, snus

**Day**:
A calendar day in the user's local time, starting at midnight.

**Day Log**:
The record of one Day, holding that Day's Pouch Count.
_Avoid_: Entry, check-in, record

**Pouch Count**:
The number of Pouches taken on a given Day.
_Avoid_: Usage, intake, total

### Planning

**Quit Plan**:
The schedule that steps the user down from their current usage to zero Pouches a day. Every user has exactly one.
_Avoid_: Program, schedule, taper

**Phase**:
One contiguous stretch of a Quit Plan with a single Daily Limit. The final Phase has a Daily Limit of zero.
_Avoid_: Stage, step, week

**Daily Limit**:
The maximum number of Pouches the current Phase allows per Day.
_Avoid_: Target, goal, allowance

**Starting Usage**:
The user's typical Pouch Count per Day before the Quit Plan, as they report it when planning.
_Avoid_: Baseline, current usage

**Quit Date**:
The first Day of a Quit Plan's final Phase, from which the Daily Limit is zero.
_Avoid_: End date, target date

**Replan**:
Replacing the Quit Plan with a new one that starts today. Past Day Logs keep the Daily Limits that applied to them.
_Avoid_: Reset, restart

**Over**:
A Day whose Pouch Count exceeds its Daily Limit.
_Avoid_: Failed, slipped, relapse

### Motivation

**Streak**:
The number of consecutive Days, ending today, that are not Over. Today breaks it as soon as it goes Over.
_Avoid_: Run, chain

**Snus-free Day**:
A Day with a Pouch Count of zero.
_Avoid_: Clean day, quit day

**Pouches Avoided**:
How many fewer Pouches the user has taken since they started tracking than their first Starting Usage would predict over the same Days. Never shown below zero.
_Avoid_: Pouches saved

**Money Saved**:
Pouches Avoided valued at the user's price per Pouch.
_Avoid_: Savings

**Motivational Quote**:
A short line of encouragement from a built-in list, shown one per Day.
_Avoid_: Tip, message

**Milestone**:
A one-time achievement earned when a defined condition is first met. Once earned, it is kept.
_Avoid_: Badge, achievement, trophy
