# Protocol

## When to use it

Run the Three-Kill Skill before a conclusion becomes durable when any of these are true:

- A result conflicts with what you expected.
- One explanation appeared quickly and everyone is ready to move on.
- Several signals agree, but they share the same source or calculation.
- The claim was relayed and nobody has checked the underlying material.
- You are about to name a cause, owner, bucket, defect, or diagnosis.

Premature closure often feels exactly like being right. That is why the trigger is the situation, not a subjective feeling of uncertainty.

## The procedure

### 1. State the claim

Write one falsifiable sentence.

> The weekly payment report is low because the payment processor is dropping transactions.

### 2. Name three rivals

You must include all three types.

| Type | Question to ask |
| --- | --- |
| Mechanical | Is a filter, default, hardcoded value, empty field, cutoff, or data-shape assumption causing this? |
| Instrument | Is the report, query, parser, dashboard, source, or measurement wrong? |
| Worst case | What is the most damaging credible explanation if it turns out to be true? |

### 3. Pick the cheapest discriminator

For every rival, name one observation that would distinguish it from the others. Prefer a query, a diff, a trace, or a short hand-read. Run checks that take minutes now. Assign and record anything larger.

### 4. Record the verdict

Use the [template](templates/three-kill-differential.md).

- **SHIPS:** all three rivals were killed by evidence.
- **REVISED:** a rival survived. It is the finding now.
- **HELD:** one or more discriminators remain open. The claim is a hypothesis, not a conclusion.

## Operating rules

- Evidence, not confidence, kills a rival.
- Agreement from dependent sources is still one witness.
- A surviving rival replaces the original claim. It does not become a caveat.
- Keep the exercise proportional. The protocol is designed for minutes, not an all-day investigation.

## What this protocol does not do

It does not guarantee the correct answer. It does not replace expertise, peer review, safety procedures, or professional judgment. It creates a small pause before the first plausible answer becomes organized work.
