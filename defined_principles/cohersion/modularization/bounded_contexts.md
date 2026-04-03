# Bounded Contexts

## Purpose

This principle establishes the use of **well-defined boundaries** to organize the system into clear and manageable parts.

The goal is to structure the project as a **well-organized monolith**, where each part has a clear identity, responsibility, and limit.

---

## Core Idea

> **A system should be divided into distinct contexts, each responsible for a specific part of the domain.**

Even within a single codebase, not everything should live together without structure.

A monolith does not mean a lack of boundaries —
it means those boundaries exist **within** the same system.

---

## Monolith, Not Chaos

This system favors a **monolithic architecture**, but not an unstructured one.

> **It should be a structured monolith — not a conceptual mixture.**

All parts may live in the same repository and runtime, but they should still be:

* Separated by purpose
* Organized by domain
* Isolated in responsibility

---

## Defining Contexts

A bounded context represents:

* A specific area of the domain
* A cohesive set of responsibilities
* A clear conceptual boundary

Each context should:

* Be understandable on its own
* Avoid leaking responsibilities into others
* Maintain internal consistency

---

## Signals of Poor Boundaries

When contexts are not well defined, the system tends to show signs such as:

* Difficulty in understanding parts of the code
* Concepts mixed in the same place
* Frequent need to navigate unrelated areas to make changes
* Growing complexity without clear structure

> These signals indicate that boundaries need to be revisited.

---

## Practical Guidance

When structuring the system:

* Group related concepts within the same context
* Separate unrelated responsibilities into different contexts
* Keep each context focused and cohesive
* Avoid creating “generic” or “shared” areas without clear ownership

When in doubt:

* Ask what responsibility belongs together
* Define boundaries based on meaning, not convenience

---

## Working Within a Single System

Even as a single-developer project, structure remains essential.

There is no need for unnecessary architectural complexity, distribution, or fragmentation.

Instead:

> **Invest in clarity through boundaries, not in complexity through architecture.**

A well-structured monolith provides:

* Simplicity in execution
* Clarity in organization
* Control over evolution

---

## Example in practice (Narvane API)

The **Narvane API** monorepo keeps **one runnable host** (`app`) and groups domain code under **`projects/`** (e.g. `hour-manager`, `pandora-box`). Each folder is a **bounded context** with its own Maven module and responsibilities; the host wires them together. HTTP prefixes (`/hour-manager/...`, `/pandora-box/...`) mirror that separation so boundaries stay visible at runtime as well as in the tree.

---

## Final Note

Bounded contexts are a tool for **thinking clearly about the system**.

They are not about adding layers or complexity,
but about preventing everything from becoming one indistinguishable whole.

> **A good system is not the one that is most divided,
> but the one where each part knows exactly where it belongs.**
