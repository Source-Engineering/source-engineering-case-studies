# How to file a case study

> The process for contributing a new case study to the Source Engineering discipline.

A case study is the discipline's evidence. Filing a case study is a normative act: the case study becomes a permanent artefact in the discipline's evidence base, and the discipline's claims are amended to reflect the case study's findings.

## When to file a case study

File a case study when:

- You have tested a hypothesis in a domain.
- You have data that supports or refutes the hypothesis.
- You have implications for the discipline as a whole.

A case study is not an essay. An essay argues a position; a case study reports a finding. The two are different acts.

## The process

1. **Read the template.** Start at `template.md`. The template is normative; deviations must be justified.
2. **Open an issue.** Describe the case study's domain, the hypothesis, the planned method, and the planned data.
3. **Link the protocol.** The case study's method is derived from a protocol in `Source-Engineering/source-engineering-research/protocols/`. If no protocol exists for the domain, file an RFC in `Source-Engineering/source-engineering-governance/RFC/` to add a protocol.
4. **Write the case study.** Follow the template. Section 4 (Data) and section 5 (Findings) are the load-bearing sections; the rest of the case study is the context.
5. **Open a PR.** The PR is reviewed by the discipline's domain maintainer and one additional reviewer.
6. **Merge and publish.** The case study is published at `https://github.com/Source-Engineering/source-engineering-case-studies/<year>-<slug>/`.
7. **Reflect.** A reflection lands in the discipline's snapshot doc: what the case study found, what the discipline changed as a result, what the next case study should test.

## Cardinal rules (binding on every case study)

- **No decisions leading to creating an org or repo are logged on GitHub.** The case study's "Author" and "Maintainer" sections use the contributor's GitHub id or name only.
- **No reference or tagging to the coding agent or another agent in any GitHub surface.** Commit messages and PR titles use the contributor's GitHub identity only.
- **Activity/identity refers to the user's GitHub id or name only.** All commits are authored by the contributor's own GitHub identity.

## Review criteria

A case study PR is reviewed on:

- The hypothesis is stated clearly.
- The method is derived from a registered protocol.
- The data is committed in section 4.
- The findings are cited to the data.
- The conclusion is one of the three valid forms.
- The implications are actionable.

A case study that fails any of these criteria is returned for revision.