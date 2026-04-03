# Boxes Inside Boxes

## Purpose

This principle defines how information, structure, and systems should be organized:

> **Everything should be structured as boxes inside boxes — clear, bounded, and meaningful at every level.**

The goal is to make any part of the system **understandable through navigation**, without requiring external explanation.

---

## Core Idea

> **Each element is a box. Each box contains other boxes. Each level must make sense on its own.**

When opening any part of the system — a folder, a module, a file — it should be immediately clear:

* Where you are
* What kind of thing you are looking at
* What exists inside that scope

Understanding should **emerge progressively**, not require reconstruction.

---

## Cognitive Foundation

This principle is grounded in how the human brain processes information:

* We **group elements into chunks**
* We can only hold a **limited number of elements in attention at once**
* We rely on **patterns and expectations** to understand structure



When structure aligns with this:

* Reading becomes natural
* Navigation becomes intuitive
* Understanding compounds with each step

When it does not:

* Every level feels like starting over
* The reader must analyze instead of recognize
* Cognitive load increases unnecessarily

---

## Progressive Understanding

A well-structured system behaves like this:

1. You open a **box**
2. You see a small set of **clear inner boxes**
3. Each inner box represents a **coherent concept**
4. You go deeper, and the same pattern repeats

> **Each level reduces uncertainty and increases clarity.**

If opening a box creates confusion instead of clarity, the structure is failing.

---

## What a Good Box Looks Like

A well-defined box should:

* Represent **one clear concept**
* Contain a **small, coherent set of elements**
* Be understandable **without opening everything inside it**
* Fit naturally within its parent context

The contents should feel like:

> “These belong together.”

---

## Signals of Poor Structure

When this principle is violated, the system starts to show clear signals:

* Too many elements inside a single box
* Mixed types of concepts at the same level
* Difficulty understanding what a container represents
* Need to open many files just to understand one area
* Multiple possible interpretations of the same structure

These are not small issues — they directly impact comprehension.

---

## Not a Hard Limit — A Cognitive Guide

This is not about strict rules like:

* “maximum 5 items per folder”
* “always split after X elements”

Instead, it is about awareness.

> **If a box feels overloaded, it probably is.**

In practice:

* A small number of elements (often around 3–5 meaningful ones) is easier to grasp
* Larger sets may work if they remain clearly coherent
* Heterogeneous sets almost always indicate a structural issue

---

## One Level, One Meaning

Each box should operate at a **consistent level of abstraction**.

If a container mixes:

* high-level concepts
* low-level details
* unrelated responsibilities

the brain cannot form a clear pattern.

Understanding breaks because:

> The reader is forced to constantly switch mental models.

---

## Context Defines Simplicity

Names and structures should leverage context.

Inside a well-defined box:

* Names can be simpler
* Concepts do not need extra qualifiers
* Meaning is derived from **where you are**, not just from the name itself

> **The box gives meaning to what is inside it.**

---

## Structural Navigation as Understanding

The system should be readable **by moving through it**, not by reading explanations.

From root to leaf:

* Each step should **narrow meaning**
* Each layer should **prepare the next**
* The whole should form a **coherent narrative**

This applies to:

* Folders
* Modules
* Files
* Classes
* Any structural unit

---

## Practical Guidance

When creating or modifying structure:

* Think in terms of **boxes and contained boxes**
* Ensure each box has a **clear identity**
* Avoid placing unrelated elements together
* Split when a box starts to lose coherence
* Group when elements naturally belong together

Ask:

* What does this box represent?
* Do its contents clearly match that idea?
* Can I understand this level without opening everything?
* Does going deeper make things clearer or more confusing?

---

## Examples (Applied Situations)

### Example 1 — Mixed Concepts Inside One Container

A container originally held:

* `Floor`
* `Roof`
* `Ceiling`
* `Brick`
* `Sand`
* `Bathroom`

At first glance, it was unclear what this box represented.

* Are these structural parts?
* Construction materials?
* Rooms?

The box mixed **different abstraction levels**, forcing interpretation.

**Refactor:**

* Grouped structural elements (`Floor`, `Roof`, `Ceiling`)
* Moved materials (`Brick`, `Sand`) into a separate context
* Separated rooms (`Bathroom`) into another context

**Result:**

Each box became **coherent and self-explanatory**, reducing ambiguity and cognitive load.

---

### Example 2 — Overloaded Module

A module contained a large number of unrelated elements:

* Business rules
* Data access logic
* UI-related structures
* Utility helpers

Understanding the module required opening multiple files and reconstructing intent.

**Refactor:**

* Split the module into smaller boxes based on responsibility
* Created clear boundaries between domain, infrastructure, and interface concerns

**Result:**

Opening the module now immediately communicates **what it is about**, without needing to inspect everything inside.

---

### Example 3 — Large File Without Clear Internal Boxes

A single file contained:

* Multiple responsibilities
* Different conceptual parts
* Deep nesting of logic

Reading it required constant context switching.

**Refactor:**

* Identified the main conceptual parts
* Extracted them into separate internal boxes (subcomponents / submodules)
* Left the original file as a composition root

**Result:**

The file now reads as **orchestration**, while details are contained in their proper boxes.

---

### Example 4 — Flat Structure With Too Many Siblings

A folder contained a long list of elements at the same level, with no grouping.

* Hard to scan
* No clear relationships
* No sense of hierarchy

**Refactor:**

* Introduced intermediate boxes based on meaning
* Grouped related elements together

**Result:**

The structure became **navigable**, allowing quick understanding through hierarchy instead of inspection.

---

### Example 5 — Context Loss During Navigation

Opening a folder did not clarify what part of the system it belonged to.

* Names required additional explanation
* Meaning depended on external knowledge

**Refactor:**

* Reorganized hierarchy so that each level provides context
* Adjusted grouping to ensure meaning is built progressively

**Result:**

Each navigation step now **adds clarity**, instead of resetting understanding.

---

### Example 6 — Too Many Elements Inside a Single Box

A container had a large number of items, making it difficult to grasp at a glance.

* Relationships were not obvious
* The reader had to scan extensively

**Refactor:**

* Identified natural groupings
* Split into smaller boxes with clearer identities

**Result:**

Each box became **scannable and understandable**, aligning with how the brain processes grouped information.

---

### Example 7 — Ambiguous Box Meaning

A container existed, but its purpose was unclear even after looking at its contents.

* Items did not form a clear pattern
* Multiple interpretations were possible

**Refactor:**

* Redefined the boundary of the box
* Either narrowed its purpose or split it into multiple boxes

**Result:**

The box now communicates a **single, clear idea**.

---

### Example 8 — Structure That Requires Explanation

A part of the system required verbal or written explanation before it could be understood.

* Structure alone was not enough
* Meaning was not visible

**Refactor:**

* Reorganized boxes so that intent is visible through naming and grouping
* Removed the need for external explanation

**Result:**

Understanding now comes from **navigation**, not from documentation.

---

### Example 9 — Clear Composition Root

A component originally mixed:

* High-level structure
* Low-level implementation details

**Refactor:**

* Extracted internal mechanics into their own boxes
* Kept the main component focused on composition

**Result:**

The main box now clearly answers:

> “What is this made of?”

And inner boxes answer:

> “How does each part work?”

### Example 10 — Separating Contexts Instead of Using Composite Names

While modeling a sprint planning system, an initial approach started to produce names like:

* `SprintTemplate`
* `TemplateSprint`

This was a signal that multiple concepts were being forced into the same space.

There were actually two distinct contexts:

* **Template** — defines reusable structures
* **Sprint** — represents real instances in use

**Refactor:**

* Created a `template` module
* Created a `sprint` module
* Each module contains its own `Sprint` concept, defined within its context

The interaction between them was reduced to a minimal interface:

* The system retrieves a template
* Instantiates a sprint from it

No need for both concepts to coexist in the same structural space.

**Result:**

* No composite naming required
* Clear separation of contexts
* Each module became simpler and more coherent
* Communication between them remained minimal and intentional

> Two boxes connected by a small bridge — not merged into one.

---

### Example 11 — Isolating a Complex Component as Its Own Box

While designing a calendar component, it became clear that it had:

* Significant internal complexity
* Its own internal logic and structure
* Many implementation details

Placing all its files at the same level as core business logic would:

* Pollute the main structure
* Increase visual noise
* Make it harder to understand what the system is about

**Initial problem:**

* The calendar is part of the application
* But its internal complexity does not belong to the main domain view

**Refactor:**

* Created a dedicated `components` module
* Placed the calendar inside it as its own internal universe
* Kept its internal structure contained within that box

At the same time:

* The component was **not extracted into a separate system**
* It remained inside the application
* Its interface with the rest of the system was kept **minimal and controlled**

**Result:**

* The main application structure remains focused and readable
* The calendar exists as a **self-contained box** within the system
* Internal complexity is hidden behind a simple interface
* The system avoids both extremes:

  * Overexposure (everything visible everywhere)
  * Over-separation (multiple disconnected systems)

> A complex box, contained and controlled — visible only where it adds meaning.

---

## Example in practice (Narvane API)

At repository root, **`projects/`** is an explicit box: “everything here is a domain module the host app runs.” Inside it, each module (e.g. **`pandora-box`**) is another box with internal layers (`auth`, `challenge`, `security`, …). That progression — root → `projects` → module → feature — matches **progressive understanding** without opening every file.

---

## Final Note

This is one of the foundational principles of this system.

It governs not just code organization, but **how meaning is constructed**.

> **A well-structured system is not one with many parts,
> but one where each part is exactly where it should be —
> inside the right box.**


