# Avoid Composite Names

## Purpose

This principle defines a clear preference:

> **Avoid composing multiple concepts into a single name.**

Names should represent **one concept at a time**.

When multiple concepts are merged into a single name, it often indicates that boundaries are unclear or that responsibilities are being mixed.

---

## Core Idea

> **If a name needs multiple words to describe different concepts, it may represent more than one responsibility.**

Examples like:

* `HouseDoor`
* `UserAccountProfile`
* `OrderPaymentStatus`

are often signals that:

* Concepts are being artificially grouped
* Boundaries are not well defined
* The structure is trying to compensate through naming

---

## Why This Matters

Composite names tend to:

* Hide underlying design issues
* Increase coupling between concepts
* Make systems harder to reason about
* Encourage “database-shaped thinking” instead of domain thinking

They often emerge from the need to:

* Fit multiple ideas into a single structure
* Mirror relational models instead of modeling behavior and boundaries

---

## A Signal, Not Just a Style

This is not only a naming preference — it is a **design signal**.

> **When a composite name appears, it should trigger a design review.**

Questions to ask:

* Are these truly one concept, or multiple?
* Should these belong to different modules or contexts?
* Is this trying to represent a relationship instead of a responsibility?
* Am I modeling structure instead of meaning?

---

## Relation to Modularization

Composite names often indicate that:

* A module is doing too much
* Boundaries between contexts are blurred
* Responsibilities are not properly distributed

Instead of creating names like `HouseDoor`, consider:

* Separating into distinct concepts (`House`, `Door`)
* Defining clear relationships between them
* Placing them in appropriate modules or contexts

---

## Avoid Database-Driven Thinking

A common source of composite naming is treating structures like database schemas:

* Joining concepts into a single entity
* Reflecting table relationships directly in names
* Designing from storage instead of behavior

> The system should not be shaped by how data is stored,
> but by how concepts are defined and interact.

---

## Practical Guidance

When naming something:

* Prefer **single, clear concepts**
* Avoid combining unrelated or loosely related ideas
* Let structure express relationships — not names

If a name starts growing:

> **Stop and reconsider the design, not the wording.**

---

## Example in practice (Narvane API)

Naming was aligned so **one product narrative** shows through: Java/Kotlin packages under **`br.com.narvane.pandorabox`**, the Maven module **`pandora-box`**, and public paths **`/pandora-box/...`**. The extra word “box” is not random composition — it is the **product name**; structure (module + package + URL) repeats the same idea instead of mixing unrelated concepts in a single class name. When the SQL schema stayed `pandora` for migration stability, that mismatch is **documented as an exception** rather than left unexplained.

---

## Final Note

This is a deliberate constraint.

It may feel restrictive at times, but it exists to preserve:

* clarity
* modularity
* and conceptual integrity

> **Good boundaries eliminate the need for complex names.**
