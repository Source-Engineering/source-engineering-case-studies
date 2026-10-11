# Case Study Template

> Every case study follows this structure. A case study that does not fit this structure is not a Source Engineering case study; it is an essay.

This template is normative. A case study that omits a section, or moves a section out of order, must explain why in the case study's `## Deviations from the template` section.

## 1. Identification

- **Case study id.** A URN of the form `urn:source-engineering:case-study:<year>-<slug>`.
- **Title.** A short, descriptive title.
- **Date.** YYYY-MM-DD.
- **Author.** The case study's author (one or more).
- **Maintainer.** The case study's current maintainer.
- **Domain.** The domain the case study is in (legal, finance, healthcare, etc.).
- **Status.** One of: `pre-registered`, `data-collected`, `analysed`, `published`, `superseded`.

## 2. Hypothesis

A clear statement of the hypothesis the case study tests. The hypothesis is one of:

- The discipline's primary claim: a COTS-bearing system reduces the hesitation factor compared to a baseline system that returns only the answer.
- A secondary claim: a COTS-bearing system makes the appeal process more efficient.
- A tertiary claim: a COTS-bearing system increases the user's ability to identify a wrong decision.

A case study may test multiple hypotheses, but each hypothesis must be stated separately.

## 3. Method

The experimental method, derived from the protocol in `Source-Engineering/source-engineering-research/protocols/`. The method names:

- The sample (practitioners, their experience, their role).
- The condition (COTS-on, COTS-off, or both).
- The measure (the dependent variable and how it is captured).
- The analysis (the statistical or qualitative method).

## 4. Data

The data the case study collected or would collect. The data is committed in this section; the case study does not assert conclusions from data that is not in the section.

## 5. Findings

The findings the case study produced. Each finding is one of:

- **Confirmed.** The data supports the hypothesis.
- **Refuted.** The data does not support the hypothesis.
- **Inconclusive.** The data is insufficient to support or refute.

A finding must be cited to a specific datum in section 4.

## 6. Conclusion

The conclusion the discipline can draw from the findings. The conclusion is one of:

- The hypothesis is closed (the discipline updates its claims).
- The hypothesis is reopened (the discipline opens a new question in `source-engineering-research/agenda.md`).
- The hypothesis is refined (the discipline amends the question).

## 7. Limitations

The limitations of the case study. The limitations are part of the case study's evidence; they are not a footnote.

## 8. Implications for the discipline

The implications of the case study for the discipline as a whole. The implications are the discipline's response to the case study: what changes in the foundations, the model, the specifications, the architecture, the conformance suite, the tools, the practice, or the education.

## 9. Deviations from the template

Any deviation from this template, with the reason.

## 10. References

- The protocol the case study is derived from.
- The data the case study collected.
- The findings the case study produced.
- Any other case study, essay, or artefact the case study cites.