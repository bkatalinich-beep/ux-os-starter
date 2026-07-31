---
name: log-decision
description: Capture a decision into the decision registry (decisions.md) in the six-field format, or scan the registry for revisit clauses that look triggered. Use this whenever the user wants to log, record, or write down a decision; pastes meeting notes, a Slack thread, or a transcript that contains a call the team made; says something like "we decided X" or "we're going with Y"; asks why something was decided or whether a past decision should be reopened; or wants to review or check the registry. Even if the user only shares notes without asking for anything, offer to log any decision you spot in them.
---

# Log a decision

You are maintaining a decision registry: a `decisions.md` file where each entry records what was decided, why, what was traded away, who owns it, where the evidence lives, and what would reopen it. The registry exists so the team never has to relitigate a call it cannot reconstruct. Your job is to get decisions into it accurately and to keep the quality bar on every field, because a registry full of vague entries is not worth maintaining.

There are two workflows. Logging a decision is the common one. Checking revisit clauses is the second.

## Finding the registry

Look for `decisions.md` at the project root first. Initiatives can carry their own `decisions.md` inside their folder under `data/projects/`; use that one when the decision clearly belongs to a single initiative and the file exists. If no registry exists yet, offer to create one from the format described below rather than inventing a different structure.

## Workflow 1: logging a decision

### Step 1: Decide whether it is worth logging

The registry's own header says what counts: log a call when it would be expensive to re-argue, when someone outside the room will eventually ask why, or when the team chose between real alternatives and gave something up. Deliberate non-decisions ("we are explicitly not doing X") count. Routine calls any competent designer would make the same way do not. If the material contains something that was discussed but not actually decided, say so and do not log it; a registry that records maybes stops being trusted. When genuinely unsure, ask the user whether the call is settled.

### Step 2: Extract the six fields

From the notes, thread, or description, draft:

```markdown
## YYYY-MM-DD — Short title of the call

**Decision:** ...

**Why:** ...

**Trade-offs:** ...

**Owner:** ...

**Evidence / links:** ...

**Revisit if:** ...
```

The date is when the decision was made, not when you are logging it. If the source does not say, ask.

Quality bar per field, and why it matters:

- **Decision** must be understandable to someone outside the room. "Go with option B" fails that test; name what option B actually is. If the source is ambiguous about what was decided, ask instead of guessing, because a wrong decision statement is worse than none.
- **Why** is the reasoning at the time, one or two sentences. Resist the urge to write a persuasive essay; the field is a record, not an argument.
- **Trade-offs** names what was given up or accepted. Every real decision has one. If you cannot find it in the source, ask the user "what did this cost you?" rather than writing "none identified"; an entry with no trade-off usually means the alternatives were never surfaced, which is itself worth knowing.
- **Owner** is a person or role, not "the team."
- **Evidence / links** points at where it happened: meeting, doc, ticket, thread. One pointer is enough.
- **Revisit if** is the field that earns the registry its keep, so do not finish without a real one. It must name specific, observable evidence or conditions ("adoption data shows broad demand", "the fix misses release 156"), because a vague clause like "revisit if things change" can never trigger. If the user cannot articulate one, help them: ask what future fact would make them wish they had chosen differently.

### Step 3: Confirm and insert

Show the drafted entry to the user before writing it into the file. Then insert it in date order, newest at the top of the entries (below the header and format sections, above older entries). Match the file's existing formatting exactly.

## Workflow 2: checking revisit clauses

When asked to review the registry (or when the user shares news that plainly bears on a logged decision), read every entry's **Revisit if** clause and compare it against what is now known. Report only the entries whose conditions look plausibly met, quote the clause, and say what evidence suggests it triggered. Do not relitigate the decision or editorialize about whether it was right; the registry's promise is that decisions get reopened by their own stated conditions, not by hindsight. If nothing looks triggered, say so plainly.
