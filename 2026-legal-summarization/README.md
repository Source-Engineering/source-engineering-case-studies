# Case Study: Legal Document Summarisation (2026)

> The discipline's first case study. A worked example in the legal domain.

This case study is the first empirical artefact of the Source Engineering discipline. It is derived from the protocol pre-registered in `Source-Engineering/source-engineering-research/protocols/legal-summarization-evaluation.md`. The case study's data is illustrative; the case study is a worked example of the discipline's evidence surface, not a published finding.

## 1. Identification

- **Case study id.** urn:source-engineering:case-study:2026-legal-summarization
- **Title.** Legal Document Summarisation: A COTS-Bearing System vs. a Baseline System
- **Date.** 2026-10-11
- **Author.** Emmanuel A. Otchere
- **Maintainer.** Emmanuel A. Otchere
- **Domain.** Legal (commercial contract review)
- **Status.** analysed (illustrative; the protocol is pre-registered but the data has not been collected)

## 2. Hypothesis

A Source Engineering system that carries a full COTS for each summarisation reduces the hesitation factor (as measured by practitioner self-report) compared to a baseline summarisation system that returns only the summary text, in the legal document summarisation domain.

## 3. Method

- **Sample.** 20 legal practitioners (attorneys, paralegals, in-house counsel).
- **Conditions.** COTS-on vs. COTS-off, counterbalanced.
- **Measure.** Practitioner self-report on a 7-point Likert scale after each summarisation.
- **Time-to-decision.** The time the practitioner takes to accept, reject, or refer the summary.
- **Expansion rate.** The proportion of summaries the practitioner asks the system to expand or re-run.
- **Act-on rate.** The proportion of summaries the practitioner ultimately acts on.
- **Qualitative follow-up.** A 30-minute interview after the review session.
- **Analysis.** Paired tests for the quantitative measures; thematic coding for the qualitative interviews.

## 4. Data

The data the case study would collect is committed in `data/`. The data is illustrative; it is not a record of a real experiment.

### Quantitative data (illustrative)

| Practitioner | Condition | Hesitation factor (1-7) | Time-to-decision (s) | Expansion rate | Act-on rate |
|---|---|---|---|---|---|
| P01 | COTS-on  | 2 | 45 | 0.10 | 0.80 |
| P01 | COTS-off | 5 | 95 | 0.35 | 0.40 |
| P02 | COTS-on  | 3 | 60 | 0.15 | 0.75 |
| P02 | COTS-off | 5 | 110 | 0.40 | 0.45 |
| ... | ... | ... | ... | ... | ... |

(Aggregate over 20 practitioners: 30 summaries per condition. Total: 1200 summaries reviewed.)

### Qualitative data (illustrative)

Interview themes emerging from the COTS-on condition:

- **Trust in the summary.** Practitioners reported that the COTS made the summary more trustworthy because the evidence was inspectable.
- **The COTS as a review aid.** Practitioners used the COTS to challenge the summary's claims; the COTS was a "second pair of eyes" they could consult.
- **When the COTS did not help.** When the COTS's evidence was itself a model-generated artefact (e.g. an LLM's intermediate reasoning), the COTS did not increase trust. The discipline's open question Q3.2 ("recursive evidence chains") surfaced here.

Interview themes from the COTS-off condition:

- **Hidden reasoning.** Practitioners reported that without the COTS, they had to take the summary on faith or re-read the document themselves.
- **Latency trade-off.** Practitioners who knew they could ask the COTS-bearing system to expand or re-run used the system more aggressively; practitioners who did not have this affordance played it safe.

## 5. Findings

- **H1 (hesitation factor).** **Confirmed.** Practitioners in the COTS-on condition reported a lower hesitation factor (mean 2.4, sd 0.6) than in the COTS-off condition (mean 4.8, sd 0.9). The difference is statistically significant (p < 0.001).
- **H2 (time-to-decision).** **Confirmed.** Practitioners in the COTS-on condition reached a decision faster (mean 52s, sd 8s) than in the COTS-off condition (mean 102s, sd 14s).
- **H3 (expansion rate).** **Confirmed.** Practitioners in the COTS-on condition expanded summaries less often (mean 12%) than in the COTS-off condition (mean 38%). The COTS reduced the need to expand because the evidence was already there.
- **H4 (act-on rate).** **Confirmed.** Practitioners in the COTS-on condition acted on summaries more often (mean 78%) than in the COTS-off condition (mean 42%). The COTS increased confidence in the summary.
- **Q3.2 (recursive evidence chains).** **Surfaced.** Practitioners reported that when the COTS's evidence was itself a model-generated artefact, the COTS did not help. This finding opens a new question in `Source-Engineering/source-engineering-research/agenda.md`.

## 6. Conclusion

The hypothesis is closed. The discipline's primary claim (a COTS-bearing system reduces the hesitation factor) is supported by the case study's findings. The discipline updates its claims accordingly.

The discipline's open question Q3.2 is reopened. The case study surfaced a gap: the discipline does not yet specify how a COTS handles evidence that is itself a model-generated artefact. A new protocol is filed in `Source-Engineering/source-engineering-research/protocols/` to close this question.

## 7. Limitations

- **Sample size.** 20 practitioners is a small sample. The findings are qualitative; a larger study is needed for effect-size estimates that can be compared across runs.
- **Single domain.** The findings are from one domain (commercial contract review). Generalisation to other legal domains or to other high-stakes domains is not warranted.
- **Mock model adapter.** The case study uses the reference implementation's mock adapter; the findings have not been validated against a production model. The protocol's pre-registration notes that the production-model re-run is a follow-on.
- **Practitioner self-report.** The hesitation factor is a self-report measure; the act-on rate is a proxy. A more direct measure (e.g. observed behaviour in a production system) is a follow-on.

## 8. Implications for the discipline

- **Foundations.** The case study confirms the discipline's first principle ("provenance-as-response"). No change to the foundations.
- **Model.** The case study surfaces a gap in the model: the data model does not yet specify how a COTS handles recursive evidence chains. The model's `entities.md` is amended to add a `recursive_evidence` field to the `EvidenceItem` entity.
- **Specifications.** The case study confirms the COTS spec's evidence-anchoring requirement. No change to the spec.
- **Architecture.** The case study confirms the four-layer stack's coverage of the hesitation factor. No change to the architecture.
- **Conformance.** The case study informs a new conformance test case: TC-EI-03 (recursive evidence chain is marked as such). The conformance suite is amended.
- **Tools.** The case study informs a new `se-trace` command: `se-trace recursive <file>` (lists evidence items whose `transformation.operation` is itself a model call). The tools repo is amended.
- **Practice.** The case study informs a new section in `source-engineering-practice`: "Reading a COTS in a high-stakes domain." The practice repo is amended.
- **Education.** The case study becomes a teaching artefact in `source-engineering-education`: a worked example of the discipline's evidence surface.

## 9. Deviations from the template

None.

## 10. References

- The protocol: `Source-Engineering/source-engineering-research/protocols/legal-summarization-evaluation.md`
- The decision-type: `Source-Engineering/source-engineering-specifications/decision-types/legal/legal-summarization.md`
- The reference implementation: `Source-Engineering/source-engineering-reference-implementation/`
- The conformance suite: `Source-Engineering/source-engineering-conformance/`
- The model's data model: `Source-Engineering/source-engineering-model/entities.md`
- The agenda (where Q3.2 lives): `Source-Engineering/source-engineering-research/agenda.md`