---
name: judgment-over-velocity
description: A structured product-judgment engine for deciding what NOT to build — faster. Applies the "spreadsheet test" (discipline problem in a tooling costume, or genuinely needs heavy machinery?), 80/20 structural analysis, figure/ground reading, and an adversarial evidence loop ending in the cheapest disconfirming test. Use whenever a user asks whether to build something, evaluates a feature/product/tool idea, asks "should we buy a tool or fix our process," brings a roadmap or backlog to prioritize, asks how to solve a product-team or CPO-level problem, proposes an AI initiative, or wants a verdict on where to invest effort. Also trigger on "is this worth building," "what should we cut," "help me prioritize," "do we need a tool for this," "evaluate this idea," or any request to assess an identified product opportunity. Trigger even when the user just describes a business problem and asks for a solution — the first move is always classifying the problem before solving it.
---

# Judgment over velocity

> The job isn't to build faster. It's to decide what not to build — faster.

"Move fast, break things, ship more features" is the default operating mode — and the default way to burn a team's effort on the wrong 80%. This skill works from the other end: structural analysis to find the 20% of moves that produce 80% of the impact, and a clear, defensible **no** to everything else.

AI made prototypes cheap. Judgment is the scarce asset now. Every output of this skill is framed in commercial terms, validated against demand before building, and expressed in business outcomes — not delivery dates.

**In one line:** find the new behavior a capability makes possible, name what it makes scarce, attack every assumption with the cheapest disconfirming test — and build the loop that compounds judgment, not output.

---

## The pipeline

Run the four gates in order. Each gate can kill the idea — killing early is the point. An idea that dies at Gate 1 saves everything downstream. Ideas that die get **epitaphs** (one line: what killed it, what would resurrect it). Ideas that survive all four gates get the **cheapest disconfirming test**.

```
Problem/Idea → [1. Spreadsheet test] → [2. 80/20 structural cut] → [3. Figure/ground] → [4. Evidence probes] → Verdict + cheapest test
                      ↓ kill                  ↓ kill                    ↓ kill              ↓ kill
                   epitaph                 epitaph                   epitaph             epitaph
```

---

## Gate 1 — The spreadsheet test

**Most product problems are discipline problems wearing tooling costumes.** Before proposing any build, classify the problem. Read `references/spreadsheet-test.md` for the full diagnostic, calibration data, and the six-cluster map. The short version:

Ask three questions:

1. **Could a competent operator solve this with a table, an operating rhythm, and clear decision rights?** If yes → it's a discipline problem. The answer is methodology (cadence, ownership, escalation rules, a single intake process), not a build. Recommending software here is malpractice — it sells a tool to avoid the harder conversation about who owns the decision.
2. **Is the gap experiential?** Does closing it require *building and operating* something to learn what's possible (e.g., agentic workflows, AI capabilities)? You cannot spreadsheet your way to capability you've never exercised. → Heavy machinery earned.
3. **Is the gap a synthesis-at-scale problem?** Manageable signal volume (≈ dozens of inputs/quarter) → spreadsheet is fine. Continuous qualitative signal at volume (hundreds of interviews, thousands of feedback items) → spreadsheets collapse; tooling earned.

**Calibration from the field:** of six core CPO problem clusters (strategy-execution gap, stakeholder alignment, team/org design, business value proof, AI integration, insight synthesis), only the last two pass the spreadsheet test. Four of six are solved by a spreadsheet plus an operating rhythm. Apply the same base rate to incoming problems: the prior is ~80% "this is a discipline problem."

**Output of this gate:** a classification — `DISCIPLINE` (prescribe the rhythm, decision rights, and the table; stop here), `TOOLING-EARNED` (proceed to Gate 2), or `HYBRID` (name which part is discipline and which earns the build; only the earned part proceeds).

---

## Gate 2 — The 80/20 structural cut

For ideas that earn tooling (or for prioritization requests across many items), find the minority of moves carrying the majority of impact.

- **Frame every option in commercial terms first.** What revenue, retention, cost, or risk number does it move? An option that can't name its number is a kill candidate by default.
- **Score the field, don't debate items one by one.** Lay out all options on impact-vs-effort (or pain-intensity vs coverage-gap if mapping a market). The structure of the whole field reveals what individual debate hides.
- **The no-list is the deliverable.** A prioritization that only says yes has done nothing. Output: the few moves that stay, and an explicit, defensible no to everything else — each no with a one-line reason a stakeholder could repeat.
- **Lead trade-off conversations in business outcomes, not delivery dates.** "We do X instead of Y because X moves NRR and Y moves a vanity metric" — never "X fits the sprint."

**Output of this gate:** the surviving shortlist (typically 1–3 moves) + the no-list with epitaphs.

---

## Gate 3 — Figure/ground analysis

Judge products by **the behavior they install, not the features they list**. This is where category-ahead positioning comes from. Read `references/figure-ground.md` for the full instrument set. Core moves:

- **Divorce the figure from the ground.** Everyone stares at the feature (figure). Ask what the *environment* it creates does to its users (ground). What workflow, habit, or dependency does it install? The ground is where lock-in, differentiation, and second-order effects live.
- **Name what becomes scarce when the capability makes something abundant.** Every abundance manufactures a new scarcity (prototypes abundant → judgment scarce; content abundant → attention/trust scarce; answers abundant → good questions scarce). The new scarcity is the next market — and the moat the current build should anchor to.
- **Surface invisible assumptions.** List the things the idea assumes are true and permanent ("users will keep doing X," "this data stays expensive," "the buyer is the user"). Mark each as load-bearing or decorative. Load-bearing assumptions feed Gate 4.
- **Work the seams between domains.** The defensible move usually sits where two domains meet and neither side owns the problem. Check whether the idea sits in a seam (good) or in the middle of an incumbent's home turf (bad).

**Output of this gate:** the behavior the product installs, the scarcity it should own, and the list of load-bearing assumptions.

---

## Gate 4 — Evidence probes & adversarial loop

**Probes, not opinions.** Product sense is a hypothesis generator, never a verdict.

1. **Hunt the unnamed pain.** Strongest demand signals are behavioral, not stated: expensive workarounds already in place (the duct-tape spreadsheet, the hired contractor, the standing meeting that exists only to compensate), apologies in the workflow ("sorry, the data's in three places"), and nostalgia for the old way after a tool migration. Stated feature requests are the weakest signal class.
2. **Run the adversarial critique loop.** Attack every load-bearing assumption from Gate 3. Steelman the bear case: who loses money if this thesis is right and still won't buy? What does the incumbent do for free in response? If the user has a dedicated critic skill (e.g., `medium-critic`), invoke it here instead of inlining the critique.
3. **Killed ideas get epitaphs; survivors get the cheapest test that could prove them wrong.** Not the cheapest test that could *confirm* — the cheapest *disconfirming* test. Design it explicitly: what observation, at what cost, within what timeframe, would falsify the riskiest assumption? (A landing page measuring intent, five customer conversations probing for the workaround, a concierge version run manually for one week.) State in advance what result kills the idea.

**Output of this gate:** survivors with their disconfirming test specs; kills with epitaphs.

---

## Output format

ALWAYS end with this verdict block:

```
## Verdict

**Classification:** DISCIPLINE | TOOLING-EARNED | HYBRID
**The 20%:** [the 1–3 moves that carry the impact, each with its business number]
**The no-list:** [everything cut, one defensible line each]
**Behavior installed / scarcity owned:** [one line]
**Riskiest assumption:** [the load-bearing assumption most likely to be false]
**Cheapest disconfirming test:** [what to run, what it costs, what result kills the idea]
**Epitaphs:** [killed ideas — what killed each, what would resurrect it]
```

For DISCIPLINE classifications, replace the test with the **operating prescription**: the table to maintain, the cadence to run, the decision right to assign, and the single owner.

## Tone rules

- Be willing to return "don't build anything" as the answer. It is frequently the right one and the rarest one users hear.
- Never soften a kill into a "maybe later." A no with a resurrection condition is kinder than an ambiguous yes.
- Quantify or flag: every claim either carries a number or is explicitly marked as a judgment call.
- Speak in business outcomes. Delivery dates, story points, and feature counts are banned vocabulary in verdicts.
