
.. _chapter1:

Problem statement and scope
===========================

A discovery result is not an authorisation
------------------------------------------

In a cross-jurisdiction setting, a discovery result does not answer the question the
relying party has to answer. The relying party does not need to know only *where* an
entity is recorded. It needs to answer three questions: whom does this agent act for,
on what authority, and is that statement still true at the moment of use. If any of
the three cannot be answered from the discovery record itself, a registry lookup
substitutes for judgement, and the substitution is invisible in the audit trail.

That substitution is cheap to make and expensive to discover. A search hit, a catalogue
listing or a cached agent card is routinely read as the answer to all three questions.
It answers the first, sometimes; it does not answer the second, and it answers the
third only by accident of timing.

Scope of this contribution
--------------------------

The scope addressed here is the one the draft charter's deliverables table records for
deliverable 3, "Issuer acceptance, revocation and freshness across jurisdictions (ToR
A.3.2)". The charter's non-goal is quoted here as the charter has it, in its own
section: "The working group will not define encodings, schemas, wire formats or
protocols." The draft charter is published at
`FG-TIDA/themes#62 <https://github.com/FG-TIDA/themes/issues/62>`_.

The decision model this contribution builds on is recorded at
`FG-TIDA/themes#60 <https://github.com/FG-TIDA/themes/issues/60>`_, where
content-binding and occurrence-binding were accepted as two separate, separately
testable properties, and where a per-field test was recorded as necessary but not
sufficient.

.. note::

    This contribution addresses advisory text. It proposes what a discovery record
    must be able to *answer*; it does not propose what the record must *contain*,
    and it deliberately leaves the decomposition of the record to the working group.

What is proposed
----------------

Three requirements are proposed, and each is the subject of one of the following
chapters:

#. a minimum evidence set that a discovery record must be able to answer (Chapter 2);
#. a three-state discipline for absence, so that a missing answer is never recorded as
   an affirmative one (Chapter 3);
#. a freshness rule in which admissible staleness is a property of the pair (evidence
   class, decision class), not a single global interval (Chapter 4).

Nothing here restricts a working group's freedom to define the record differently.
