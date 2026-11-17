
.. _chapter4:

Two-clock freshness
===================

Two clocks, one assertion
-------------------------

The third requirement concerns time. Two clocks run against every assertion, and they
are not the same clock: the time at which the evidence was produced, and the time at
which the decision is taken. A single global time-to-live value cannot serve both a
read-only lookup and an irreversible act, and it cannot serve two jurisdictions whose
supervisory expectations differ.

Staleness as a property of the pair
-----------------------------------

The requirement is that a relying party state an admissible staleness budget paired
with the class of decision it is about to take, and record it alongside the actual age
of the evidence. The effect is that 'stale but acceptable' and 'stale and unacceptable'
become distinguishable after the fact, which is what an auditor needs and what a single
interval destroys.

The pair matters in both directions. A single interval set short enough for an
irreversible act makes read-only lookups unusably expensive and pushes implementers
towards caching; the same interval set long enough to make lookups work silently admits
evidence that no longer supports the act. Neither failure is visible in a log that
records only timestamps.

Where the evidence carries no validity window
---------------------------------------------

One minimum criterion follows from this: where the evidence carries no validity window,
the freshness assessment is ``unknown`` and the decision is left undetermined, rather
than being assessed against a default interval. A default interval is a policy choice
made by one party on behalf of another, and it should be visible as such rather than
embedded in a lookup, where nobody will ever read it.

.. note::

    This chapter deliberately does not say what the classes are. Deciding the classes
    is the working group's work; deciding that the *pair* is the unit of assessment is
    the requirement. A group that adopts the pair but names its classes differently has
    satisfied the requirement, not contradicted it.
