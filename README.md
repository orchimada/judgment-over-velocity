# Judgment over Velocity

> The job isn't to build faster. It's to decide what **not** to build — faster.

A [Claude skill](https://docs.claude.com/en/docs/agents-and-tools/agent-skills) that turns Claude into a structured product-judgment engine. Give it a product idea, a backlog, a "should we buy a tool?" question, or any CPO-level problem — and instead of cheerfully helping you build it, the skill **classifies the problem first** and runs it through four kill-gates.

It is explicitly willing to answer **"don't build anything"** — the most common right answer and the rarest one product teams hear.

Made by [Artem Domozhakov](https://orchimada.github.io) · [How it works (long version)](https://orchimada.github.io/skill.html)

## The four gates

```
Problem/Idea → [1. Spreadsheet test] → [2. 80/20 structural cut] → [3. Figure/ground] → [4. Evidence probes] → Verdict + cheapest test
                      ↓ kill                  ↓ kill                    ↓ kill              ↓ kill
                   epitaph                 epitaph                   epitaph             epitaph
```

1. **The spreadsheet test** — most product problems are discipline problems wearing tooling costumes. Could a competent operator solve this with a table, an operating rhythm, and clear decision rights? Field calibration: 4 of 6 core CPO problem clusters fail this gate.
2. **The 80/20 structural cut** — every option framed in commercial terms; the field scored as a whole. **The no-list is the deliverable**: each cut gets a one-line reason a stakeholder could repeat.
3. **Figure/ground analysis** — products judged by the behavior they install, not the features they list. What becomes scarce when your capability makes something abundant? Which assumptions are load-bearing — and melting?
4. **Evidence probes & adversarial loop** — probes, not opinions. Demand signals ranked: expensive workarounds > apologies > nostalgia > stated feature requests. Survivors get the cheapest **disconfirming** test, with the kill-condition stated in advance.

Each gate can kill the idea — killing early is the point. Killed ideas get epitaphs (what killed them, what would resurrect them).

## Install

### Claude Code

```bash
# personal — available in every project
git clone https://github.com/orchimada/judgment-over-velocity.git /tmp/jov \
  && cp -r /tmp/jov/judgment-over-velocity ~/.claude/skills/

# or project-level — shared with your team via git
cp -r /tmp/jov/judgment-over-velocity .claude/skills/
```

Restart Claude Code (or start a new session) and verify: ask *"do you have the judgment-over-velocity skill?"*

### claude.ai (web & desktop)

1. Download [`judgment-over-velocity.skill`](https://orchimada.github.io/assets/judgment-over-velocity.skill) (it's a zip of the skill folder).
2. **Settings → Capabilities → Skills** → upload the file.

The skill activates automatically whenever you ask Claude to evaluate an idea, prioritize a backlog, or judge a build-vs-buy question.

## Try it on

- *"We're thinking of building an internal dashboard to track product KPIs across teams. Should we?"*
- *"Here are the 14 items on our Q3 roadmap — help me prioritize."*
- *"Sales wants us to buy a customer-feedback platform. We get ~30 feedback items a quarter."*
- *"Evaluate this idea: AI agent that writes PRDs from Slack threads."*

## Every run ends in a verdict

```
## Verdict

**Classification:** DISCIPLINE | TOOLING-EARNED | HYBRID
**The 20%:** the 1–3 moves that carry the impact, each with its business number
**The no-list:** everything cut, one defensible line each
**Behavior installed / scarcity owned:** one line
**Riskiest assumption:** the load-bearing assumption most likely to be false
**Cheapest disconfirming test:** what to run, what it costs, what result kills it
**Epitaphs:** killed ideas — what killed each, what would resurrect it
```

## What's inside

| File | Contents |
|---|---|
| [`judgment-over-velocity/SKILL.md`](judgment-over-velocity/SKILL.md) | The four-gate pipeline, verdict format, and tone rules ("never soften a kill into a maybe-later") |
| [`references/spreadsheet-test.md`](judgment-over-velocity/references/spreadsheet-test.md) | Full diagnostic: three classification questions, the six-cluster CPO calibration map, HYBRID handling, named anti-patterns (tool-as-avoidance, dashboard theater, pilot purgatory) |
| [`references/figure-ground.md`](judgment-over-velocity/references/figure-ground.md) | Five instruments: behavior-installed test, abundance→scarcity table, invisible-assumptions audit, seams between domains, the rear-view-mirror check |
| [`judgment-over-velocity.skill`](judgment-over-velocity.skill) | The same skill folder zipped for claude.ai upload |

## License

MIT © 2026 Artem Domozhakov
