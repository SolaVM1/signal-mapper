# Signal Mapper

A Claude skill that turns "who should we contact, and why now?" into a staged outbound plan: which signals to collect, in what order, from which sources, how to score them, how to grade accounts, and who to contact at each one.

Built while scoring ~290 outbound and GTM agencies for a real campaign. The rules in it come from decisions made (and money nearly wasted) during that build.

## What it gives you

Ask it to *"map out a signal strategy for [your ICP]"* and it returns:

1. **Goal** (it always asks for this if you haven't given it)
2. **Signal table**: each signal rated on strength, time, usefulness, cost and proof
3. **Scoring model**: P1 / P2 / P3 priority, max points and a points ladder per signal
4. **Grades A to D**, set by which priority signals fired, not by how many accounts you can afford
5. **Stage sequence**: free and disqualifying first, paid and timing later, with rows in and out
6. **Who to contact**: the role each fired signal points to, a backup role and an opening angle
7. **Budget, test plan, traps and the next step to run**

## Principles

- A signal with no date can't tell you "now".
- Disqualify before you qualify. Free before paid. Machine before manual.
- Every paid stage runs on a 20-row sample first.
- Missing data scores 0, never a penalty.
- Case studies and "trusted by" logos are hooks, not proof of activity.
- Every agent-derived value keeps a receipt (the URL it came from).

## Install

**Claude app:** download this repo as a zip (Code → Download ZIP), then upload the `signal-mapper` folder as a zip in the Skills section of Claude's settings.

**Claude Code:** copy the folder into your skills directory:

```
git clone https://github.com/SolaVM1/signal-mapper.git
cp -r signal-mapper/signal-mapper ~/.claude/skills/
```

Then ask: *"Map out a signal strategy for funded SaaS startups hiring their first SDRs."*

## Example

The skill ends with a worked example from the agency campaign: the stages, the scoring model (hiring P1, momentum and activity P2, partner tier P3), the grade rules and the trap that almost cost ~740 credits.

## Licence

MIT. Use it, fork it, adapt it to your ICP.

Built by Sola.
