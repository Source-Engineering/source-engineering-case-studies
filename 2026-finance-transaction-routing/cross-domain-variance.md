# Cross-Domain COTS Profile Variance (Legal vs. Finance)

> Slice 6's deliverable: what actually differs between the COTS profiles of two high-stakes domains. The shared skeleton is the discipline; the per-domain profile is the implementation (manifesto, "domain first").

## What is shared (the skeleton)

- The five-part COTS structure (Inputs, Context, Decisions, Evidence, Validation) and every normative field.
- The typed question / declared answer shape (Layer 1 interface).
- The evidence-chain requirements: supporting and contradicting evidence, typed relationships, RFC-0002 chain termination.
- The Layer 2 Validation record, Layer 3 guardrails, Layer 4 audit trail, and the TC-L2/L3/L4/RC/CG conformance families.

## What differs (the profile)

| Aspect | Legal (summarisation) | Finance (transaction routing) |
|---|---|---|
| Decision shape | Free-text summary with declared structure | Enumerated: one `destination_id` from a declared set |
| Load-bearing evidence | Source paragraphs and clauses cited by the summary | Destination constraints and routing rules; counterevidence is "would route elsewhere" |
| Failure cost | Liability from a wrong summary | A misrouted financial transaction; measurable as wrong-route catch rate |
| Tertiary measure | Expansion/re-run rate on summaries | Wrong-route catch rate on misrouted probes |
| Guardrail flavour | Jurisdiction and privilege constraints | Amount thresholds, sanctions screening, destination constraints |
| Audit emphasis | Appeal against the summary | Re-run against the same COTS after a rules update; correction linked to the rules source |

## The Slice 6 answer

"Judgment separate from evidence" is the same claim in both domains at the framing level (the evidence chain is structural; the judgment is contextual, in both). What needs per-domain framing is the **tertiary measure** and the **guardrail vocabulary**, not the claim itself. Recorded as the refined open question in `source-engineering-research/agenda.md`.
