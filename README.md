# Discovery evidence: a minimum set, an absence discipline, and a two-clock freshness rule

Contribution submitted for the first meeting of the ITU-T Focus Group on Trust and
Identity for Humans and Agentic AI (FG-TIDA), UNESCO Paris, 30 November – 1 December 2026.

## Propose a new work item

Want to propose a new work item (NWI) to FG-TIDA? Follow the procedure in the contribution guide: https://fg-tida.github.io/.github/#new

## Contribute to this work item

Contributions to the work of a Working Group are possible once a work item has been adopted by that Working Group and its official repository has been created. The instructions are in the contribution guide: https://fg-tida.github.io/.github/#existing

Anything you contribute is offered as input to the Working Group's work and may be incorporated into its deliverables. Participation follows the ITU-T and FG-TIDA participation, conduct, and IPR rules.

---

| Field | Value |
| --- | --- |
| Title | Discovery evidence: a minimum set, an absence discipline, and a two-clock freshness rule |
| Acronym | discovery-evidence |
| Authors | Xinghua Zhao, independent researcher (ORCID [0009-0001-0512-1237](https://orcid.org/0009-0001-0512-1237)) |
| Working Group | No working group yet (declared target: ADXT advisory text, deliverables 2 and 3) |
| DataTracker record | Assigned by the TIDA DataTracker on submission; this repository does not invent one |
| Status | Submitted as a contribution for consideration, version 00 — not an approved text |
| Published site | https://zhaoxinghua09-cell.github.io/fgtida-contribution-discovery-evidence/ |
| Source entry point | `src/doc/index.rst` |
| Related discussions | FG-TIDA themes#60 (decision table), themes#62 (draft ADXT charter) |

This document is a contribution for consideration. It is not an approved text of the
Focus Group, it carries no endorsement, and it makes no claim of priority, novelty or
absence of comparable work.

## What it proposes

Three requirements, each stated as something a record must be able to answer rather
than as something a record must contain:

1. **A minimum evidence set** — five questions a discovery record must answer:
   principal binding, issuer and scope of the acceptance, status and revocation with
   provenance, the validity window of the evidence, and the retrieval receipt.
2. **An absence discipline** — `no_record_found`, `query_failed` and `not_revoked` are
   three states, and no aggregate may count the first two as passes.
3. **A two-clock freshness rule** — admissible staleness is a property of the pair
   (evidence class, decision class), not a single global interval; evidence without a
   validity window yields `unknown`, not a default.

It defines no encoding, schema, wire format or protocol, consistent with the charter's
non-goals.

## Build

```bash
pip install -r requirements.txt
sphinx-build -b html -W --keep-going src/doc build/html
```

The build is warning-free under `-W`. The reading version is generated from the RST
sources in `src/doc/`.

## Disclosure

Prepared with AI assistance under the author's direction and review. The listed
positions are the author's, and the author takes responsibility for them.

## Licence and provenance

Built on the FG-TIDA specification template
([FG-TIDA/spec-template](https://github.com/FG-TIDA/spec-template)); upstream
copyrights and licence are retained in `LICENSE`.
