---
name: three-kill
description: Test a tentative root cause or other consequential finding against three rival explanations before recording it or dispatching work. Use for unexpected results, unverified relayed claims, or apparent agreement from evidence that shares a source. Skip routine questions and straightforward edits.
license: CC-BY-4.0
---

# The Three-Kill Skill

Use the [differential template](templates/three-kill-differential.md) to record the initial claim, tests, evidence, verdict, and any next check.

1. Write the current claim as one falsifiable sentence. Separate what was observed from the explanation.
2. Name three distinct, credible rivals to that explanation:
   - **Mechanical:** a filter, default, hardcoded value, cutoff, empty field, or data-shape assumption.
   - **Instrument:** the query, parser, report, source, or measurement is misleading.
   - **Worst case:** the credible explanation with the most serious consequences. Do not repeat the initial claim or invent a rival just to fill the slot.
3. For each rival, name the cheapest check that would distinguish it from the others and what result would count against it. Run quick, authorized checks now. Prefer direct evidence; multiple reports from the same source count as one witness. Record access limits and unfinished checks as open, without inventing results or expanding permissions.
4. Record the verdict:
   - **SHIPS:** direct evidence supports the original explanation and rules out all three rivals.
   - **REVISED:** evidence favors a rival over the original and resolves the competing explanations that matter to the decision. State the revised finding and retain the original as superseded.
   - **HELD:** the evidence is insufficient to distinguish material explanations or to support the original. State what remains unresolved and give the next check.

Failure to rule a rival out does not establish it. Keep the work proportional; this is a diagnostic check, not authorization to take action or a substitute for domain expertise.

Source: [InflectAI, Inc., The Three-Kill Skill (2026)](https://github.com/Inflect-ai/three-kill-skill), licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
