
.. _chapter-appendices:

Appendix A — Checks performed on the quoted material
====================================================

Two strings in this contribution are reproduced as quotations from the draft charter
published at `FG-TIDA/themes#62 <https://github.com/FG-TIDA/themes/issues/62>`_. Both
were compared against the charter text as published, character by character, including
case and punctuation, before submission:

.. list-table::
    :header-rows: 1
    :widths: 55 20 25

    * - Quoted string
      - Section of the charter
      - Result
    * - Issuer acceptance, revocation and freshness across jurisdictions (ToR A.3.2)
      - Deliverables table, row 3
      - matches
    * - The working group will not define encodings, schemas, wire formats or protocols.
      - Out of Scope / Non-Goals
      - matches

Two further points of care are recorded here, because both are easy to get wrong in
a contribution that quotes a charter while proposing text for it:

#. The charter's proposal text and its non-goals are different places, and a sentence
   from one must not be presented as adjacent to a sentence from the other. The non-goal
   quoted above is reproduced alone, with its section named.
#. The charter expresses the non-goal twice, in slightly different words: once in the
   proposal paragraph ('encodings, schemas or protocols') and once in the non-goals
   section ('encodings, schemas, wire formats or protocols'). Only the second is quoted
   here, because it is the normative statement.

Every other double-quoted phrase in this document is the author's own shorthand, used
to name a failure mode, and is not presented as a quotation from any source.

Outside opinion received in review
----------------------------------

The three requirements above were put to an independent third party before this
contribution was filed. Kenne Ives (AgentAvow) reviewed them without payment and
answered each one. The answers are reproduced below in full, as an outside opinion,
not as an endorsement of this contribution, of any review, or of the draft charter;
that condition is the author's own reading of the correspondent's instruction, and
the instruction is reproduced with the answers.

Because two of the three answers say the underlying point is not new, and the second
one names a configuration in which a two-state design is defensible, the answers are
quoted here rather than cited in support. They are attributed, unedited, and are not
presented as agreement with the contribution:

  1. Agree, true but not new. A valid signature shows the bytes were signed by the key
     that verified them. Whether that key is the one the relying party expected is a
     second check (a pinned key, a resolved DID, a trust anchor), and a receipt should
     report it separately.

  2. Agree. Revocation checking already separates good, revoked and unknown, and
     treating a failed query as "not revoked" is the familiar soft-fail mistake. A
     two-state design is defensible where credentials are short-lived enough that no
     revocation check is made at all, so expiry does the work.

  3. Agree, mostly true but not new. One number can work in practice if it is set for
     the strictest decision class, at the cost of refetching for cheap reads. Our own
     scan results are cached for one hour, with a forced re-scan when a caller needs
     fresh evidence, which is in effect two classes.

  You may quote these, provided you quote all three answers in full and as an outside
  opinion, not an endorsement of the review or the charter.

The second answer's qualification is material to the second requirement as drafted: a
deployment that performs no revocation check at all, and relies on expiry, is not
described by a three-state rule. That case is left to the working group as an explicit
open question rather than resolved here.
