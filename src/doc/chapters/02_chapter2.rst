
.. _chapter2:

A minimum evidence set
======================

A discovery record, in the sense used here, is what a relying party receives when it
asks a registry or resolver about an agent or an issuer. The proposal is that such a
record should be able to answer five questions, and that a record unable to answer any
one of them should be treated as insufficient rather than as a partial success.

Principal binding
------------------

Which principal the agent acts for, and the instrument on which that authority rests.
The answer is a statement about a relationship, not a statement about a name. A record
that names an operator without naming the authority it exercises has moved the
question, not answered it.

Issuer and scope of the acceptance
----------------------------------

Whether the relying party should accept is a judgement about the pair (issuer, scope),
not about the issuer alone. A record that answers 'this issuer is trusted' without
answering 'for what' has answered a different question than the one being asked. Scope
is part of the answer, not metadata about the answer.

Status and revocation assertions, with their provenance
-------------------------------------------------------

An assertion about current status must carry the query that produced it: which source
was consulted, over which set of issuers, at what time, and with what outcome. Without
provenance, a status assertion is indistinguishable from a cached opinion, and a
cached opinion that has outlived its source is the failure mode that a status field
alone cannot prevent.

The validity window of the evidence itself
------------------------------------------

Distinct from the age of the record, this is the interval during which the assertion
was intended to hold, with a stated production time and a stated end. Age answers
'how old'; the window answers 'until when was this meant to be true'. A record that
carries only a timestamp leaves the relying party to guess the second answer.

The retrieval receipt
---------------------

Who retrieved what, from where, at what time, and what the retrieval covered. This is
the part that makes the previous two auditable after the fact, and the part that is
most often absent. An absence of a receipt is not evidence of absence of an answer:
it is evidence that nobody can say afterwards what was asked.

None of the five is a field name
--------------------------------

Each of the five is a question that the record must support. The working group
remains free to decide how a record supports it, whether in one structure or several,
and whether the answers are carried in the record or resolvable from anchors the
record points to. A reader who takes these five as a required field list has read them
one level too literally.
