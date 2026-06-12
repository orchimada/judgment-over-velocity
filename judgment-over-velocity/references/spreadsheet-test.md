# The spreadsheet test — full diagnostic

The founding observation: **~80% of business problems can be solved with a table and a spreadsheet.** The valuable skill is identifying the ~20% that genuinely can't — because those are the only problems where building or buying heavy machinery is justified, and they're the only defensible ground for a product bet.

## The three-question gate

Run these in order. The first "yes" classifies the problem.

### Q1 — Is it a discipline problem in a tooling costume?
> Could a competent operator solve this with a table, an operating rhythm, and clear decision rights?

Signals it's a discipline problem:
- The artifact already exists (a roadmap, a tracker, an OKR sheet) but nobody maintains it
- The proposed tool replaces a process nobody owns — ownership, not capability, is what's missing
- The complaint is about alignment, visibility, accountability, or "people not following the process"
- A previous tool was bought for this exact problem and quietly abandoned
- The honest fix is an uncomfortable conversation ("who has final say when sales and engineering disagree?") that the tool purchase postpones

If yes → **DISCIPLINE**. Prescribe: the table schema, the cadence (who updates it, when, reviewed in which meeting), the decision right (one named owner with tiebreak authority), and the escalation rule. Do not propose a build.

### Q2 — Is the gap experiential?
> Does closing it require building and operating something to learn what's possible?

Signals:
- The team can't evaluate options because they've never run one (e.g., "should we use agents for X?" from a team that's never deployed an agent)
- Decision quality depends on pattern recognition that only comes from hands-on builds
- The cost of being wrong about capability is high, and no spreadsheet of vendor claims substitutes for operating experience

If yes → **TOOLING-EARNED** (specifically: proof-of-concept builds, working examples, pattern libraries). The deliverable is capability, not software per se.

### Q3 — Is it synthesis at scale?
> Does the problem involve finding patterns across qualitative signal at a volume where tables collapse?

Calibration thresholds:
- Dozens of inputs per quarter (≈20 interviews, ≈100 feedback items) → a tagged spreadsheet is fine; recommending a platform here is over-tooling
- Hundreds of interviews, thousands of comments, continuous multi-channel signal (support + sales calls + NPS + community) → human-plus-spreadsheet synthesis degrades into sampling bias and recency bias; AI-assisted synthesis or a research repository is earned

If yes at volume → **TOOLING-EARNED**.

If all three answers are no → re-examine whether the problem is real. Problems that fail all three gates are often status anxieties or vendor-induced demand.

## The six-cluster calibration map

Field calibration from CPO pain-landscape research. Use as a prior when classifying incoming problems — most product-org complaints map to one of these clusters.

| Cluster | Typical complaint | Classification | What's actually needed |
|---|---|---|---|
| Strategy–execution gap | "Strategy evaporates before it reaches the team" | DISCIPLINE | Ritual design: outcome-framed roadmap, weekly cadence, single intake with visible trade-offs |
| Stakeholder alignment | "I spend 10 hrs/week aligning people" | DISCIPLINE | Decision rights, intake log, update cadence, named owner of alignment |
| Team & org design | "PMs don't know what good looks like / AI changed the work" | DISCIPLINE | Leadership clarity, role redesign, methodology — consulting, not product |
| Business value proof | "We can't prove product impact to the board" | DISCIPLINE (upstream) | Hypothesis-framed decisions before work starts; the empty dashboard is a symptom of missing upstream thinking |
| AI integration pressure | "We're stuck in pilot purgatory" | TOOLING-EARNED (Q2) | Hands-on builds, working agentic examples, capability transfer |
| Insight & discovery deficit | "We have data but no information" | TOOLING-EARNED at volume (Q3) | AI-assisted synthesis, research repository — only past the volume threshold |

Base rate: **4 of 6 clusters are discipline problems.** When in doubt, the prior favors DISCIPLINE.

## HYBRID handling

Many real problems split. Example: "our feedback is scattered and nobody acts on it" = a synthesis problem (possibly Q3, volume-dependent) wrapped around a discipline problem (no owner, no cadence for acting on insight). Classify each part separately; only the earned part proceeds to Gate 2. State explicitly: "Buying the synthesis tool without assigning the insight owner reproduces the current failure with better UI."

## Anti-patterns to call out by name

- **Tool-as-avoidance:** purchasing software to postpone a decision-rights conversation
- **Dashboard theater:** building measurement for decisions that were never framed as hypotheses
- **Pilot purgatory:** perpetual AI experiments with no scale path and no kill criteria
- **Over-tooling the small:** platform purchases at spreadsheet-scale volume
- **Process cosplay:** adopting a framework's vocabulary (OKRs, JTBD) without its decision discipline
