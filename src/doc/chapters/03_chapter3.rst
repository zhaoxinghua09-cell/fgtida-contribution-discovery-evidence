
.. _chapter3:

Absence discipline
==================

The second requirement concerns what happens when the answer is missing. Three
outcomes are routinely collapsed into two, and the collapse is where an absence
becomes an affirmative statement.

Three states, not two
---------------------

``no_record_found`` and ``not_revoked`` are different answers. A registry that returns
nothing has told the relying party that it found nothing, not that nothing exists.
Treating the first as the second is the most expensive mistake available in this
domain, because it converts a gap in coverage into a positive assurance, and the
conversion leaves no trace in the record.

A second collapse follows. ``query_failed`` and ``scope_unknown`` must be surfaced as
undetermined, and must not be counted as passes in any aggregate. A failed query is a
fact about the querying party's reach, not a fact about the subject. An aggregate that
counts a failed query as a pass reports coverage that does not exist, and reports it
in the same units as coverage that does.

The labels in this chapter name outcomes, not field values: ``no_record_found``,
``query_failed`` and ``not_revoked`` describe what happened when the question was
asked, and the rule against merging them binds any representation that carries them.

Empty coverage is not global completeness
-----------------------------------------

Any claim of absence must state the set of issuers that was examined, the extent of the
examination, and the basis on which the absence conclusion rests. An absence claim
without a stated examined set is a claim about the examiner, not about the world. This
is the third state in practice: not an answer about the subject, but a statement about
the reach of the asker, which a reader must be able to see and weigh.

What is reused from the decision table, and what is not
-------------------------------------------------------

The distinction this chapter rests on is recorded in the group's decision
table, where content-binding and occurrence-binding are kept as two separate,
separately testable properties and a per-field test is recorded as necessary but not
sufficient. What is reused here is the classification of failure, not any particular
field set: the three states above are the failure classes that a per-field test cannot
distinguish on its own, because a per-field test asks whether each field is well
formed, not whether the collection of fields distinguishes an empty answer from a
negative one.

.. note::

    The requirement is a requirement about the record's *answers*, not about its
    storage. A record can carry the three states in one enumerated value, in three
    separate assertions, or in a single assertion plus a receipt; what it must not do
    is leave the reader unable to tell which of the three happened.
