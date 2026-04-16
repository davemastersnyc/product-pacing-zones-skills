# Contributing

Thanks for wanting to build on this. A few things to know before you do.

---

## What this is

These skills are the opinionated layer on top of the Product Pacing Zones framework. The framework has a specific point of view: that speed is not the problem, and that most product failures happen because teams conflate confidence with pace. The skills are designed to operationalize that point of view, not to be a generic product planning assistant.

Contributions that sharpen the thinking are welcome. Contributions that soften it are not.

---

## What good contributions look like

**Refinements to the existing skills.** If a question is ambiguous, an output format is confusing, or a rule produces the wrong behavior in an edge case, fix it and explain why.

**New signal types or evidence patterns.** The PDVF filter uses a stated/behavioral signal distinction. If you have worked in a domain (hardware, regulated industries, B2B enterprise, consumer mobile) and the evidence patterns are meaningfully different, document them and extend the skill accordingly.

**Domain-specific forks.** A fork calibrated for fintech, for healthcare, for marketplace products -- useful. The zone definitions may shift. Zone 4 gets wider in regulated industries. Note the changes explicitly.

**Additional gates or checks.** If there is a genuine gap in the three-gate sequence for your context, add a skill for it. Don't collapse it into an existing one.

---

## What does not belong here

- Generic product management templates that are not grounded in the framework
- Skills that ask a lot of clarifying questions before generating output -- that is not how these work
- Output that softens or hedges the result to avoid conflict -- if a PDVF check fails, it fails
- Assumption mapping methodology -- that is David Bland's work, not ours. Link to [Testing Business Ideas](https://www.amazon.com/Rapid-Testing-Business-Ideas-Customer/dp/1119551447) and [Precoil](https://precoil.com) instead

---

## Principles to preserve

**Gates are checkpoints, not ceremonies.** Each skill should produce a clear result with a clear next action. If someone reads the output and cannot tell what to do next, the skill failed.

**Skips are documented, not absorbed.** If a gate was bypassed, the output says so explicitly and names what was skipped. It does not pretend the skip did not happen.

**The zone defaults conservative.** When signal is ambiguous, the classification goes up, not down. This is intentional. Getting to a lower zone requires a named gate event, not a judgment call.

**Named people, not named roles.** A gate without a named person is not a gate. The skills should reinforce this.

---

## How to submit

Open a PR with your change and a brief description of the problem it solves or the gap it fills. Include an example input and output if the change affects skill behavior.

If you are building a significant fork or domain-specific variant, open an issue first so we can discuss whether it belongs here or is better as a standalone repo with a link from this one.
