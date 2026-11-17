# Worked Example: The Payment Report

## Initial claim

> The weekly payment report is low because the processor is dropping transactions.

The report is 18 percent below the previous week. The first explanation is plausible. It is also expensive if wrong: support starts contacting the processor, finance starts forecasting a cash shortfall, and engineering begins planning a remediation.

## Differential

| Rival | Cheap discriminator | Result |
| --- | --- | --- |
| A report filter excluded one merchant segment. | Compare the report predicate to the prior-week version. | **Survived.** A new default excluded transactions with a blank optional campaign field. |
| The reporting query is reading a stale replica. | Compare query timestamp and row count against the primary store. | Killed. Both match. |
| Checkout is failing before payment requests reach the processor. | Check checkout completion rates and failures before payment submission. | Killed. Both are within the usual range. |

## Verdict

**REVISED.** Processor settlement counts reconcile with the primary transaction ledger. Removing the new filter restores the excluded transactions and accounts for the report's shortfall. The finding is a reporting error. Keep the initial claim in the investigation history as superseded.

## Why this example exists

The first explanation was coherent and alarming. The mechanical explanation was boring. The boring explanation was true.
