# Product Pacing Zones -- Claude Code Skills

Claude Code skills for the [Product Pacing Zones](https://quietbranches.com/work/product-pacing-zones/) framework.

Three gates. One for confidence, one for pace, one for proof.

---

## The framework in one paragraph

Product teams have two decisions they consistently conflate: should we build this, and how fast can we build it. AI has made the second feel obvious. It has not changed the first. Product Pacing Zones separates these two decisions and gives teams a shared language for both. Gate 1 checks confidence before anything gets a ticket. Gate 2 determines how fast a surface can move and what has to clear before it ships. Gate 3 closes the loop after ship: did the behavior change we predicted actually happen? Shipping is a hypothesis. Gate 3 is the proof.

Full framework: [quietbranches.com/work/product-pacing-zones](https://quietbranches.com/work/product-pacing-zones/)

---

## The three gates

### Gate 1 -- PDVF Filter (`/pdvf-filter`)
Before anything gets a zone or a ticket, it needs to pass four evidence tests. Problem, Desirable, Viable, Feasible. Each is a separate confidence call. Any failure means you need a Zone 1 experiment, not a production ticket.

### Gate 2 -- Zone Classifier (`/zone-classifier`)
Four questions to classify a surface by risk. The result is one of four zones, each with a gate requirement that must clear before build or staging begins.

| Zone | Name | Gate |
|---|---|---|
| 1 | Move fast | Internal review only |
| 2 | Coordinated | Named reviewer must clear before staging |
| 3 | Provisional | Vendor + integration confirmed |
| 4 | Move deliberately | Legal or compliance sign-off before design starts |

### Gate 3 -- Outcome Review (`/gate3-review`)
Work is not finished when it hits production. It is finished when the behavior change predicted in Gate 1 actually happens. Gate 3 runs three tests -- did behavior change, is the value sustainable, and the "so what?" test -- and maps the result to a signal tier: maintain, iterate, or pivot/kill.

---

## How to use these skills

These are [Claude Code](https://claude.ai/code) skills. Claude Code is Anthropic's CLI for Claude.

**Setup**

1. Clone this repo into your project's `.claude/skills/` directory, or copy the files from `skills/` directly:

```bash
# option A: clone into an existing project
git clone https://github.com/quietbranches/product-pacing-zones-skills .claude/skills/pacing-zones

# option B: copy the skill files
cp skills/*.md your-project/.claude/skills/
```

2. Open your project in Claude Code.

**Usage**

Invoke a skill by typing its name as a slash command in Claude Code:

```
/pdvf-filter
/zone-classifier
/gate3-review
```

Then describe the feature, bet, or shipped surface you want to evaluate. The skill runs immediately -- no clarifying questions.

**Example**

```
/zone-classifier

We're adding Apple Pay to our checkout flow. The integration is through Stripe,
which is already contracted. Legal has not reviewed yet.
```

```
/pdvf-filter

We want to build a saved search feature for our job board. Users have asked for it
in support tickets. We haven't validated whether it changes application behavior.
```

---

## Design principles

These skills are intentionally opinionated. A few things that should stay true in any fork or extension:

**No hedge language.** "Probably" and "likely" are not passes. The skills name gaps directly.

**Work from incomplete information.** The skills generate output from whatever context is given. They do not ask clarifying questions before producing a result. A partial result with named gaps is more useful than a stalled conversation.

**Gate 1 requires the thinking, not the passing.** Early-stage work will not have complete PDVF signal -- that is expected. What Gate 1 requires is that the team engages with the four dimensions, names the riskiest assumption, and knows what it would take to increase confidence. Running the filter with weak signal and a named gap is not a skip. Proceeding without running it at all is. Gate 2 and Gate 3 are informed by what Gate 1 surfaces, not gated on it closing clean.

**A skip is always noted, not silently absorbed.** If a gate was bypassed, the output says so and names what was skipped. It does not pretend the skip did not happen.

**Stronger evidence costs something to produce.** A quote is easy. A behavior is harder to fake. The skills distinguish between stated and behavioral signal.

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidance on extending or adapting these.

---

## License

[Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE)

You can use, adapt, and build on this work for any purpose, including commercial use, as long as you give appropriate credit to [Quiet Branches Labs](https://quietbranches.com) and link back to the original framework.

---

Built by [Dave Masters](https://quietbranches.com) at Quiet Branches Labs.
