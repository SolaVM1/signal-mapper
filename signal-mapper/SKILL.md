---
name: "signal-mapper"
description: "Map a staged signal strategy for an outbound campaign: which signals to collect, in what order, from which sources, with gates, timing, a scoring model with signal priorities, grades, and who to contact. Use when asked to map a signal strategy, signal system or scoring gates for an ICP or list."
---

# Signal Mapper

Turns "who should we contact, and why now?" into a staged plan: cheap, disqualifying signals first; expensive, timing signals later; personalisation hooks last, on the shortlist only. Every signal earns its place by changing **who** gets contacted, **when**, or **what** the message says. Anything else is cut.

Trigger phrases: "map out a signal strategy for X", "what signals should I use for X", "build the gates for this list", "how should I score these accounts".

## Step 1: Intake (goal first, always)

Read what is already available first: project docs, the ICP, the current list, the tools connected. Then ask only for what is missing, in one message, **5 questions at most**, using multiple choice where possible.

**The campaign goal is never assumed.** If the person has not stated it in detail, the first question is always this one, asked as a single compact question:

> **Goal**: What are you offering, who usually says yes to it, and what does a win look like (e.g. 10 booked calls in 4 weeks)?

Then, only if still unknown:

2. **List**: who is on it (company type, size, geography) and roughly how many rows?
3. **Why now**: what would make an account worth contacting this month rather than any month?
4. **Budget and tools**: credits or cash for data, hours for manual checks, and tools available (e.g. Clay, Deepline, Apollo, a code environment, a browser, a spreadsheet).
5. **Timeline**: when does outreach start, and is this a one-off list or a recurring feed?

If the goal answer is vague (e.g. "more clients"), ask one follow-up to make it concrete before mapping. If the person is in a hurry on everything else, state assumptions and continue. Never continue on an assumed goal.

## Step 2: Ideate candidate signals

List 10 to 20 candidate signals across these six families. Include the obvious ones and at least two non-obvious ones that fit the goal.

| Family | What it tells you | Examples |
|---|---|---|
| **Fit** | They could buy at all | size band, location, industry, tech stack, partner/directory listings, business model |
| **Activity** | They are alive and operating now | date of newest blog/newsletter post, sitemap last-modified, social posting cadence, product changelog |
| **Growth** | They are expanding | headcount change (3 to 6 months), new office, new market, new product line |
| **Trigger / intent** | Something just changed that creates need | open roles (esp. roles you would replace or support), funding, leadership change, launch, tool adoption or churn, review-site activity, job change of a past champion |
| **Engagement** | They already know you | site visits, content engagement, follows, event attendance, replies |
| **Relationship** | You have a way in | mutual connections, past customers, shared community, warm intro path |

For each candidate, name at least one source, marked **free** (code, public pages, public APIs, sitemaps, RSS, public job-board APIs), **cheap** (low per-row credits), **paid**, or **manual** (human time).

## Step 3: Rate every signal on five tests

Rate each candidate 1 to 3 on each test and keep short reasons.

1. **Strength (S)**: how directly does it mean "they need this now"? A relevant job post is strong. A logo strip or case-study page is weak.
2. **Time (T)**: is it dated, and how fast does it decay? Use the decay table below. Undated signals score 1.
3. **Usefulness (U)**: does it change who, when, or what is said? If it changes none of these, drop it.
4. **Cost per row**: free = 3, cheap = 2, paid = 1, manual = 1 (manual is reserved for the smallest set).
5. **Proof**: can a source URL or record be attached so anyone can check it? Self-reported, undated or unverifiable claims score 1.

S, T and U decide how much a signal is **worth**. Cost and Proof decide **when** it runs and whether it may be a gate.

### Typical decay (adjust per market)

| Signal | Useful window |
|---|---|
| Job post | 30 to 60 days |
| Funding round | 60 to 120 days |
| Leadership change | 60 to 90 days |
| Social / content post | 14 to 30 days |
| Site or blog update | 6 months (active), 12 months (quiet) |
| Headcount trend | 3 to 6 months |
| Tech adoption | 3 to 6 months |
| Firmographics | Stable, re-check yearly |

## Step 4: Give each kept signal one role

- **Gate**: removes rows. Only for clear disqualifiers with high proof. Gates never use weak or undated signals.
- **Rank**: adds or removes points in the score.
- **Hook**: not scored, used to personalise the message (e.g. a case study, a recent post, a named client). Collected last, on the shortlist only.

One signal can be a gate at one threshold and a rank above it (e.g. site dead = gate; content age = rank).

## Step 5: Order into stages

Apply these rules in this order:

1. **Disqualify before you qualify.** Gates that remove the most rows for the least cost go first.
2. **Free before paid.** Code and public sources before credits.
3. **Machine before manual.** Human time goes on the final, smallest set.
4. **Fit before timing.** Stable fit signals first; dated timing signals once the list is smaller.
5. **Hooks last.** Personalisation data only for accounts that will actually be contacted.
6. **Test before spend.** Every paid stage runs on a 20-row sample first, with the real cost per row and hit rate shown before the full run.
7. **Kill rules.** Every paid signal has a threshold that cuts it or lowers its weight (e.g. hit rate under 15%: drop it one priority level).

The budget decides **which signals get collected and on how many rows**. It does not decide grades (Step 7).

## Step 6: Scoring model and signal priority

Every rank signal gets a **priority**, a **maximum number of points**, and a **points ladder**. Always present them in one table, highest priority first, so the person can see at a glance which signals matter most and where to spend first.

### 6a. Points come from the tests, not guesses

Add S + T + U (each 1 to 3) and convert:

| S + T + U | Max points | Priority | Meaning |
|---|---|---|---|
| 9 | 5 | **P1, must-have** | Strongest "why now" for this goal. Spend credits here first; fill gaps with a paid source if free coverage is weak. |
| 7 to 8 | 4 | **P2, strong** | Confirms timing or momentum. Collect for every row that passed the gates. |
| 5 to 6 | 3 | **P2, strong** | Same as above. |
| 4 | 2 | **P3, supporting** | Tie-breaker. Collect only if free or cheap. |
| 3 | 1 | **P3, supporting** | Tie-breaker. Skip if it costs credits. |

A hook gets no points and no priority. It is listed separately.

### 6b. Points ladder inside each signal

Split each signal's max points into steps, and say what a negative looks like:

- e.g. hiring: 2+ relevant roles = 5, 1 = 4, careers page live but no relevant role = 1, nothing found = 0.
- e.g. activity: active = 3, quiet = 1, unknown = 0, stale = -2.
- Negative points only for **confirmed** bad news (stale, shrinking), never for missing data.

### 6c. Scoring rules

- **Deterministic only**: a formula, never a model judgement.
- **Missing data = 0**, not a penalty. Report coverage per signal (e.g. "headcount found for 82% of rows").
- **Noise floors**: percentage signals need a minimum absolute change (e.g. headcount growth counts only if the team changed by 2+ people), or tiny teams swing wildly.
- **One signal, several sources**: combine with a stated rule (e.g. take the higher count) and record which source the value came from. Flag a source that is not filtered to the goal (e.g. a jobs count with no title filter).
- **One rulebook**: keep the points table in one place (a config file or spec). If the score is calculated in another tool (e.g. a Clay formula), re-check it against an export.
- Mark the weights as a hypothesis until checked against a blind hand-ranked sample of ~40 rows.

## Step 7: Grades (A to D), set by signal strength

The grade says **how strong the evidence is** that this account needs the offer now. It is set by **which priority signals fired**, not by how many accounts you can afford to contact.

A signal has **fired** when it reaches at least half its max points (e.g. hiring 4 of 5 = fired; careers page only, 1 of 5 = not fired).

| Grade | Rule | Plain meaning |
|---|---|---|
| **A** | a P1 fired **and** at least one P2 fired | Strong reason + confirmation. Contact first. |
| **B** | a P1 fired alone, **or** two or more P2s fired | One strong reason, or several solid ones. Contact next. |
| **C** | one P2 fired, or only P3s fired | Fits, but no clear "why now". Keep and re-check later. |
| **D** | nothing fired, or the account has more negative than positive points | Not now. |

- A confirmed negative (stale, shrinking) drops the account **one grade**.
- Within a grade, sort by total score.
- A signal that was not collected for a row (budget did not cover it) counts as **not fired**, and the row is marked "partially checked", so you know it might move up if checked.
- Write the grade as a formula next to the score, so it updates when data changes.

## Step 8: Who to contact, based on the signal

The signal that fired decides **who feels the problem**, and gives the opening angle. Map each fired P1/P2 signal to a role:

| Signal that fired | Who to contact | Opening angle |
|---|---|---|
| Hiring sales roles (SDR, AE) | Head of Sales / VP Sales | "You're building a sales team, so pipeline is the bottleneck" |
| Hiring ops/system roles (RevOps, GTM engineer, marketing ops) | COO / RevOps lead / Head of Growth | "You're hiring for the system; it can be built now" |
| Fresh funding | Founder / CEO | "New targets after the raise" |
| Headcount growing fast | Founder / COO | "Growth is outpacing process" |
| New leader joined (sales, marketing, growth) | That new leader, within their first 90 days | "New leaders change tools and vendors early" |
| Expansion to a new market or region | Head of that market / GM | "A new market needs a new pipeline" |
| Tech adoption or churn | Owner of that tool (ops / RevOps) | "You just switched to X; here's what usually breaks" |
| Engagement with your content | The person who engaged | Reference what they engaged with |

Rules:

- **Small companies (under ~20 people): contact the founder**, whatever the signal.
- If two signals point to different people, contact the more senior one and mention the other signal as the second reason.
- Suggest a backup role in case the first person cannot be found or has left.
- Order of the contact stage: find the person, manual check (right person, still there, recently active), then email lookup and verification, then drafts for approval. The paid email step runs only on people who passed the manual check.

## Output format

Deliver, in this order:

1. **Goal** (as confirmed) and **assumptions** (one short list, only if any).
2. **Signal table**: signal | family | role (gate/rank/hook) | source | cost per row | decay window | S/T/U/cost/proof scores.
3. **Scoring model**: priority | signal | max points | points ladder. P1 first.
4. **Grade rules** (A to D) for this campaign, with the signals named.
5. **Stage sequence**: stage | what runs | cost | gate rule | estimated rows in and out. Start from the real list size.
6. **Who to contact**: fired signal | role | backup role | opening angle.
7. **Budget estimate**: total spend and where it goes, plus manual hours.
8. **Test plan**: which stages get a 20-row sample, what is measured, the kill rule for each.
9. **Traps**: 2 to 4 signals that look useful but are not for this goal, and why.
10. **Next step**: the first stage to run and exactly what to run it on.

Keep it tight: tables over prose. If the person has a code repo or spec system, offer to write each stage as a spec file before anything runs.

## Principles to hold

- A signal with no date cannot tell you "now".
- Anything an account writes about itself (case studies, "trusted by" logos, awards pages) is a hook, not proof of activity.
- Every agent-derived value needs a receipt (the URL it came from).
- Losers stay: dropped rows are kept with a reason, never deleted.
- If a cheaper source answers the question well enough, the expensive one is not used.
- Nothing is sent to a prospect without the person's approval.

## Worked example (agency outreach)

**Goal**: book calls with outbound/GTM agencies that are active and growing, to offer them a done-for-you scoring system. **List**: ~290 agencies from partner directories and tool-partner listings. **Budget**: ~450 credits, a few hours of manual review.

**Stages**

| # | Stage | Cost | Role | Rows |
|---|---|---|---|---|
| 0 | Hygiene: has domain, team 2 to 100 | free | gate | 290 -> 247 |
| 1 | Alive: site loads, newest dated content (feed, sitemap) | free | gate (dead) + rank | 247 -> 232 |
| 2 | Hiring, free pass: careers pages, public job-board APIs | free | rank | 232 |
| 3 | Hiring, paid gap: job data for rows the free pass missed, 20-row test first | paid | rank | gap only |
| 4 | Momentum: 6-month headcount growth, survivors only | paid | rank | 232 |
| 5 | Score and grade | free | rank | 232 |
| 6 | Find the person (A and B only) | paid | contact | A + B |
| 7 | Manual check: right person, still there, posting recently | manual | final gate | -> ~30 to 40 |
| 8 | Personalisation: case studies, named clients, recent posts | cheap | hook | ~30 to 40 |
| 9 | Email lookup + verification, then drafts for approval | paid | contact | ~30 to 40 |

**Scoring model**

| Priority | Signal | S/T/U | Max | Ladder |
|---|---|---|---|---|
| P1 | Hiring relevant roles (higher of careers page and paid job count) | 3/3/3 | 5 | 2+ = 5, 1 = 4, careers page only = 1, none = 0 |
| P2 | Headcount momentum, 6 months, needs 2+ people change | 2/2/2 (6) | 4* | >15% = 4, 0.01 to 15% = 2, flat = 0, shrinking = -1 |
| P2 | Activity (newest dated content) | 1/3/2 (6) | 3 | active = 3, quiet = 1, unknown = 0, stale = -2 |
| P3 | Partner tier | 1/1/1 (3) | 1 | top tiers = 1, else 0 |

*Momentum was raised one step above the table because it was the user's stated must-have. Overrides like this are allowed, but must be written down with the reason.

**Grades for this campaign**: A = hiring fired + (momentum or activity fired). B = hiring fired alone, or momentum + activity both fired. C = one of momentum/activity only. D = nothing fired. Stale or shrinking drops one grade.

**Who to contact**: these agencies are almost all under 20 people, so the founder in every case; backup = managing director or head of growth. Opening angle from the fired signal: hiring ("you're adding delivery capacity") or momentum ("you're growing fast").

**Trap found in this build**: a model was about to count case studies on 247 websites (~3 credits each, ~740 credits). Case studies are self-reported and undated, so they say nothing about whether an agency is active today. They were moved to the hook stage, and the budget went to dated signals instead.
