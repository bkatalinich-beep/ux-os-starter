# Decision registry

Decisions that matter: what we decided, why, what we traded away, and what would make us revisit it. Newest entries at the top.

The registry exists because teams relitigate decisions they cannot reconstruct. Six months after a call is made, the people who made it have moved on to other problems, the context has evaporated, and someone new asks "why is it like this?" Without a record, the team either re-argues the whole thing or shrugs and lives with mystery. With a record, the answer takes thirty seconds and has a date on it.

## What counts as a decision worth logging

Log a call when it would be expensive to re-argue, when someone outside the room will eventually ask why, or when you chose between real alternatives and gave something up. Scope cuts, descopes, and "we are deliberately not doing this" calls belong here just as much as the things you chose to build. Routine calls that any designer would make the same way do not need an entry.

## The format

Every entry gets the same six fields. The revisit clause is the one most teams skip and the one that earns its keep: it names, at the moment of deciding, what new evidence would change your mind. When that evidence shows up later, the team can bend without anyone losing face, because the original decision already promised it would.

Copy this block for each new entry:

```markdown
## YYYY-MM-DD — Short title of the call

**Decision:** What was decided, stated plainly enough that someone outside the room understands it.

**Why:** The reasoning at the time, in a sentence or two.

**Trade-offs:** What you gave up or accepted by deciding this way.

**Owner:** Who made or carries the decision.

**Evidence / links:** The meeting, doc, ticket, or thread where it happened.

**Revisit if:** The specific evidence or condition that would reopen this.
```

## Worked example

A real entry from the Firefox Nova program, included so you can see the format carrying weight. Months after this was logged, community feedback during early access provided exactly the evidence the revisit clause named, and the team could act on it without re-arguing the original call.

## 2026-06-04 — Corner radius customization option (pursue in Labs)

**Decision:** Add a corner radius (square vs rounded) customization option in Labs, framed as a leadership-level "should we offer this at all" decision, distinct from the earlier design and engineering scoping of tab roundness.

**Why:** Community debate over square vs rounded corners raised the question of whether to offer it as a setting. It is unknown whether this is a reaction to change or a genuinely important option. Shipping it in Labs signals we are listening and lets us evaluate next steps from Labs data.

**Trade-offs:** Labs only keeps it out of the default path; if the demand is real, a Labs gate delays reaching the users asking for it.

**Owner:** Design leadership · product · TPM

**Evidence / links:** Decision brief; related design and engineering scoping logged separately.

**Revisit if:** Labs adoption data shows broad demand (argues for Settings, not Labs), or shows it was change-reaction noise (argues for dropping it).

---

Your first entry goes above this line. Start with the most recent consequential call your team made, even if it happened weeks ago; backfilling one decision is the fastest way to learn the format.
