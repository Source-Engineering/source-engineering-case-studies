# Case Study: Finance Transaction Routing (2026)

> The discipline's second case study. A worked example in the finance domain, closing Slice 6 (Cross-Domain Validation).

This case study is the second empirical artefact of the Source Engineering discipline. It is derived from the pre-registered protocol in `Source-Engineering/source-engineering-research/protocols/transaction-routing-evaluation.md`, which mirrors the legal protocol's measure frame so results are comparable across domains. A worked COTS for the domain is produced by `source-engineering-reference-implementation` (`npm run example:transaction-routing`) and validated by the conformance suite and `se-trace explore`. The case study's data is illustrative; it is a worked example of the discipline's evidence surface, not a published finding.

## 1. Identification

- **Case study id.** urn:source-engineering:case-study:2026-finance-transaction-routing
- **Title.** Transaction Routing: A COTS-Bearing System vs. a Baseline System
- **Date.** 2026-11-02
- **Author.** Emmanuel A. Otchere
- **Maintainer.** Emmanuel A. Otchere
- **Domain.** Finance (outbound USD wire routing)
- **Status.** analysed (illustrative; the protocol is pre-registered but the data has not been collected)

## 2. Hypothesis

Primary: a Source Engineering system that carries a full COTS for each routing decision reduces the hesitation factor (practitioner self-report) compared to a baseline system that returns only the chosen destination, in the financial transaction-routing domain.

Secondary (tertiary claim of the template): a COTS-bearing routing system increases the analyst's ability to identify a wrong routing decision before execution, measured by the wrong-route catch rate on deliberately misrouted probes.

## 3. Method

- **Sample.** 20 financial operations analysts (payments ops, treasury, compliance).
- **Conditions.** COTS-on vs. COTS-off, counterbalanced; 30 routing decisions each.
- **Measures.** Same frame as the legal study: 7-point hesitation self-report, time-to-decision, expansion rate, act-on rate; plus wrong-route catch rate on 6 misrouted probes per condition.
- **Analysis.** Paired Wilcoxon signed-rank tests; thematic coding against the legal study's theme frame; cross-domain comparison on effect direction.

## 4. Data

Committed in `data/quantitative.csv` and `data/qualitative.md`. Illustrative, labelled as such.

Aggregate (illustrative): COTS-on hesitation 2.4 vs. COTS-off 4.7; time-to-decision 43s vs. 91s; act-on 0.85 vs. 0.43; wrong-route catch 0.78 vs. 0.42.

## 5. Findings

- **Primary hypothesis: confirmed (illustrative).** COTS-on reduces the hesitation factor in the finance domain (2.4 vs. 4.7), same direction as legal (2.4 vs. 4.7). Cited to `data/quantitative.csv` aggregate rows.
- **Secondary hypothesis: confirmed (illustrative).** Wrong-route catch rate 0.78 vs. 0.42 on misrouted probes. Cited to the `wrong_route_catch_rate` column.
- **Cross-domain: confirmed (illustrative).** The direction of the hesitation-factor effect is consistent across legal and finance, supporting the claim that the discipline's primary claim is not domain-specific.

## 6. Conclusion

The hypothesis is refined, not just closed: "judgment separate from evidence" (Slice 6's open question) holds in both domains at the framing level, but the finance domain adds a domain-specific measure (wrong-route catch rate) that the legal domain does not have. The question is amended to: does each domain need its own tertiary measure, or only its own framing? Recorded in the research agenda.

## 7. Limitations

- Data is illustrative, not collected; the protocol is pre-registered, the experiment is not run.
- One institution, one transaction type; narrow by design.
- n=20 per domain is small; the protocol targets themes and direction, not effect sizes.
- The worked COTS is produced by a mock adapter, not a real LLM call.

## 8. Implications for the discipline

- Slice 6 (Cross-Domain Validation) closes: the framework ports to a second domain with the same COTS skeleton and a per-domain profile, per the manifesto's "domain first" principle.
- The cross-domain COTS profile variance doc (`cross-domain-variance.md` in this directory) records what differed between the legal and finance profiles.
- The research agenda gains the refined judgment-vs-evidence question and the standardized hesitation-factor protocol becomes the per-domain standard.

## 9. Deviations from the template

- None. The finance-specific wrong-route catch rate is an addition to the measure frame, declared in the protocol, not a deviation.

## 10. References

- Protocol: `Source-Engineering/source-engineering-research/protocols/transaction-routing-evaluation.md`
- Decision-type: `Source-Engineering/source-engineering-specifications/decision-types/finance/transaction-routing.md`
- Worked COTS: `Source-Engineering/source-engineering-reference-implementation` (`npm run example:transaction-routing`)
- Legal case study: `Source-Engineering/source-engineering-case-studies/2026-legal-summarization/`
- Cross-domain variance: `cross-domain-variance.md` in this directory
