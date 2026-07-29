# Worked Example: The Payment Report

## Initial claim

> The weekly payment report is low because the processor is dropping transactions.

The report is 18 percent below the previous week. The first explanation is plausible. It is also expensive if wrong: support starts contacting the processor, finance starts forecasting a cash shortfall, and engineering begins planning a remediation.

## Differential

| Rival | Cheap discriminator | Result |
| --- | --- | --- |
| A report filter excluded one merchant segment. | Compare the report predicate to the prior-week version. | **Survived.** A new default excluded transactions with a blank optional campaign field. |
| The reporting query is reading a stale replica. | Compare query timestamp and row count against the primary store. | Killed. Both match. |
| The processor is dropping live transactions. | Compare processor settlement count with the primary transaction ledger. | Killed. Counts reconcile. |

## Verdict

**REVISED.** The payment processor is not dropping transactions. A report filter excluded a segment from the weekly view. The initial claim is removed from the incident record and replaced with the surviving explanation.

## Why this example exists

The first explanation was coherent and alarming. The mechanical explanation was boring. The boring explanation was true.
