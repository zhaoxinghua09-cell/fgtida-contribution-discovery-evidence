
.. raw:: latex

    \pagestyle{plain}
    \thispagestyle{plain}
    %% Suppress all TOC entries for the overview chapter (sections, subsections,
    %% Copyright addcontentsline) — restored just before \sphinxtableofcontents
    %% so chapters from Introduction onward appear in the TOC normally.
    \let\osiaorigaddcontentsline\addcontentsline
    \renewcommand{\addcontentsline}[3]{}

.. _chapter-overview:

Discovery evidence: a minimum set, an absence discipline, and a two-clock freshness rule
========================================================================================

.. only:: html

    **Contribution to FG-TIDA, first meeting (Paris, 30 November – 1 December 2026)**

.. raw:: latex

    \begin{center}\textbf{Contribution to FG-TIDA, first meeting (Paris, 30 November – 1 December 2026)}\end{center}

Abstract
--------

A discovery record in a cross-jurisdiction setting does not answer the question a
relying party has to answer. This contribution proposes three requirements for the
advisory text of the Agent Discovery and Cross-Border Trust (ADXT) working group, so
that a relying party can tell, from the record itself, whom an agent acts for, on what
authority, and whether that statement still holds at the moment of use:

#. a **minimum evidence set** that a discovery record must be able to answer;
#. a **three-state discipline** in which 'no record found', 'query failed' and
   'affirmatively not revoked' are never collapsed into two;
#. a **two-clock freshness rule** in which admissible staleness is a property of the
   pair (evidence class, decision class) rather than a single global interval.

The distinction the three-state discipline rests on is already accepted in the
decision table recorded in the group's theme discussion: content-binding and
occurrence-binding are kept as two separate, separately testable properties, and a
per-field test is necessary but not sufficient. What is reused here is the
classification of failure, not any particular field set.

The contribution defines no encoding, schema, wire format or protocol, consistent with
the draft charter's non-goals. It is offered as text that the working group may adopt,
amend or reject, and it seeks no role, seat or editorship.

History
-------

.. list-table::
    :header-rows: 1
    :widths: 10 26 18 14 32

    * - Version
      - Document
      - Approval
      - Focus Group
      - Working Group
    * - 00
      - Discovery evidence: a minimum set, an absence discipline, and a two-clock freshness rule
      - 2026-11-17 (contribution, not an approved text)
      - TIDA
      - No working group yet (declared target: ADXT advisory text, deliverables 2 and 3)

Authors
-------

.. list-table::
    :header-rows: 1
    :widths: 30 40 30

    * - Name
      - Affiliation
      - Contact
    * - Xinghua Zhao
      - Independent researcher (ORCID 0009-0001-0512-1237)
      - zhaoxinghua07@126.com

Keywords
--------

Agent discovery, cross-border trust, revocation, freshness, absence of evidence,
agentic AI, requirements, protocol-neutral.

.. raw:: latex

    \newpage
    \osiacenternextsection

Foreword
--------

Agentic AI systems now act as autonomous entities capable of reasoning, planning, and
executing tasks across services, infrastructures, and organizational boundaries. This
fundamentally changes the nature of identity in digital systems: identity is no longer
limited to human users and static machine instances but must also encompass autonomous,
dynamic, and goal-oriented agents. And identity alone is insufficient — the core question
extends beyond "what an entity is" to "whether, and under what conditions, that entity
should be trusted to act".

The Focus Group on Trust and Identity for humans and agentic AI (FG-TIDA) addresses trust
management and interoperable digital identity infrastructure for humans and for agentic AI,
supporting the development of secure, trustworthy digital ecosystems in which humans and
agentic AI can safely interact and collaborate.

FG-TIDA was established under Recommendation ITU-T A.7 (Focus groups: Establishment and
working procedures), with ITU-T Study Group 17 as its parent group. Further details are
available in the group's terms of reference.

This document is a contribution submitted for consideration at the first FG-TIDA meeting.
It is not an approved text of the Focus Group, and it carries no endorsement.

.. raw:: latex

    \osiacenternextsection

Note
----

**Two limits, stated before the argument.** First, this contribution does not assert that
the present state of the art lacks these ideas. No systematic survey was performed, so no
novelty or priority claim is made, and a reader who knows comparable work should read the
three requirements as a proposal for wording rather than as a claim of a gap. Second, the
requirements are stated at the level of what must be answerable, not at the level of fields.
A design that satisfies them with a different decomposition of the record is not excluded.

**Disclosure.** This contribution was prepared with AI assistance, under the author's
direction and review; the positions are the author's and the author takes responsibility
for them. Two quoted strings are reproduced from the draft charter and are marked as
quotations where they appear; every other double-quoted phrase in this document is the
author's own shorthand, not a quotation from any source.

.. raw:: latex

    %% Restore \addcontentsline so the TOC below (and Chapter 1 onward) populate.
    \let\addcontentsline\osiaorigaddcontentsline
    \sphinxtableofcontents
    \osiamainmatter

.. toctree::
    :maxdepth: 3
    :numbered:
    :hidden:

    chapters/01_chapter1
    chapters/02_chapter2
    chapters/03_chapter3
    chapters/04_chapter4/index
    chapters/05_annex/index
    chapters/06_appendix/index
    chapters/07_references
