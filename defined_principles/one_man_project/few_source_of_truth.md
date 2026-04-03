# Few Sources of Truth

## Purpose

This principle defines how truth should be managed within the system:

> **Reduce the number of sources of truth as much as possible — but not artificially to one.**

The goal is to avoid duplication, inconsistency, and unnecessary maintenance effort, while still respecting the natural boundaries of the system.

---

## Core Idea

> **Truth should be centralized where possible, and limited where not.**

In an ideal scenario, there would be a single source of truth for everything.
In practice, different contexts may require their own controlled sources.

This leads to a more realistic principle:

> **Have as few sources of truth as necessary — no more.**

---

## Why This Matters

Multiple sources of truth introduce:

* Duplication of logic or data
* Risk of inconsistency
* Increased maintenance effort
* Hidden coupling through synchronization

In a single-developer project, this cost is even more significant:

* Time is limited
* There is no parallel ownership
* Every duplication becomes a direct burden

---

## Avoiding Extremes

### 1. Artificial Unification

Forcing everything into a single source of truth can:

* Break natural boundaries
* Create oversized, hard-to-manage structures
* Introduce unnecessary coupling

> Not everything belongs in the same place.

---

### 2. Uncontrolled Duplication

Allowing multiple sources without control leads to:

* Diverging behaviors
* Repeated logic
* Synchronization problems

> If the same concept exists in multiple places, it must be intentional — not accidental.

---

## The Assertive Middle

> **Each concept should have a clear, primary source of truth — and as few alternatives as possible.**

When multiple sources exist, they should be:

* Justified by context
* Clearly separated
* Minimally overlapping

---

## Practical Perspective

When modeling the system:

* Prefer defining a concept in one place
* Reference it instead of replicating it
* Avoid reimplementing the same logic in different contexts

If duplication appears, ask:

* Can this be centralized?
* If not, why does it need to exist in multiple places?
* Is the separation intentional or accidental?

---

## Controlled Distribution

There are valid cases where multiple sources of truth exist:

* Different bounded contexts
* Different layers with distinct responsibilities
* Performance or lifecycle constraints

In these cases:

* Each source must have a **clear ownership**
* The relationship between them must be **understood and controlled**

---

## Time as a Constraint

This system operates under a key constraint:

> **Limited time and single ownership.**

Because of this:

* Reducing duplication is not just a design preference — it is a necessity
* Every additional source of truth increases long-term cost
* Simplicity and centralization directly impact productivity

---

## Practical Guidance

When defining or modifying a concept:

* Where is its **primary source of truth**?
* Am I duplicating this unnecessarily?
* Can I reference instead of replicate?
* If I must duplicate, is it controlled and justified?
* Will this increase maintenance effort later?

---

## Example in practice (Narvane API)

The build aligns **one** set of module paths for Maven and Docker (`projects/hour-manager`, `projects/pandora-box`) so dependency resolution and image layers do not drift from the source tree. OpenAPI is maintained as **one** hand-authored spec for documentation; runtime routes stay consistent with that spec. Where the database still uses an older schema name for **historical and cost reasons**, that single exception is **written down** in `by_pass_definition_principles.md` so it stays a conscious trade-off, not a hidden second story.

---

## Final Note

This principle is about **efficiency and clarity**.

Not everything can live in one place —
but nothing should exist in many places without reason.

> **The fewer the sources of truth,
> the easier it is to understand, maintain, and evolve the system.**
