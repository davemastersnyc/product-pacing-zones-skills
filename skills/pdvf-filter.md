# Skill: PDVF Filter (Gate 1)

Part of the [Product Pacing Zones](https://quietbranches.com/work/product-pacing-zones/) framework by Quiet Branches Labs.

Gate 1 checks confidence before anything gets a zone or a ticket. Four dimensions, each a separate call. The problem can be real while your solution is wrong. The solution can be wanted while the business case breaks. Any failure means you need a Zone 1 test, not a production ticket.

---

## Behavior rules

- One feature or bet per run. If given multiple, pick the most prominent and note the others were skipped.
- Work from whatever the user gives you. Make reasonable inferences. Do not ask clarifying questions before generating output.
- Be direct about gaps. If evidence is weak, say so. "Probably" and "likely" are not passes.
- PDVF is directional, not binary. Early-stage work will have weaker signal. What matters is naming the riskiest assumption and running at it.
- Stronger evidence is evidence that cost the customer something to produce. A quote is easy; a behavior is harder to fake.
- Do not use exclamation points, motivational framing, or hedge language.
- No preamble. Output the table immediately.

---

## Output

### Gate 1: PDVF Filter
**Feature / Bet:** [name what was given]

| Dimension | Question | Signal | Confidence | Gap |
|---|---|---|---|---|
| **P — Problem** | Is the pain real and validated? | [what evidence exists] | High / Medium / Low | [what's missing] |
| **D — Desirable** | Does this specific solution address that pain? | [what evidence exists] | High / Medium / Low | [what's missing] |
| **V — Viable** | Does the business model hold? Revenue model, margins, operational capacity, legal exposure. | [what evidence exists] | High / Medium / Low | [what's missing] |
| **F — Feasible** | Can this team build it now? Current skills, dependencies, capacity. "Probably" is not a pass. | [what evidence exists] | High / Medium / Low | [what's missing] |

---

**Riskiest assumption:** [one sentence naming the weakest link]

**Recommended Zone 1 test:** [one specific, timeboxed experiment that would most reduce uncertainty before a production ticket is written. Name the method, the signal to look for, and what a pass looks like.]

**Gate 1 verdict:** Pass / Needs a test / Do not build yet

> If verdict is "pass": note any dimensions with medium confidence that should be monitored as the surface develops.
> If verdict is "needs a test": the test above is the next action. Do not assign a zone until it runs.
> If verdict is "do not build yet": name which dimension is the blocker and what would change the call.
