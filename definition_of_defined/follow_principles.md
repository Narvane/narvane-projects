# Follow Principles

## Purpose

This definition establishes that:

> **A project is only considered defined if it follows all declared principles.**

It ensures that structure, organization, and design decisions are aligned with the system’s foundational rules.

---

## Definition

A project **follows principles** when:

* All principles defined in `defined_principles/` are respected
* Structural and conceptual decisions reflect those principles
* There are no significant violations of the declared guidelines

This is not about superficial compliance, but about **true alignment**.

---

## Evaluation Criteria

To be considered as following principles, a project must:

* Maintain clear and coherent structure
* Respect modular boundaries and contexts
* Avoid unnecessary coupling or over-separation
* Keep naming consistent with defined philosophy
* Preserve clarity and readability through organization
* Align with all other declared principles in intent and execution

---

## How It Is Verified

Verification is performed by:

* Reading all documents inside `defined_principles/`
* Interpreting their intent
* Comparing them against the project’s structure and organization

This evaluation is **holistic**, not rule-by-rule mechanical checking.

---

## Allowed Flexibility

Principles are not meant to be applied rigidly.

A project may still be considered compliant if:

* Deviations are intentional
* Trade-offs are justified
* The overall structure remains coherent
* Specific deviations are **declared in writing** in that project’s root file **`by_pass_definition_principles.md`** (see `definition_checker/is_defined.md` for how aggregators must honor it)

> **The goal is alignment, not blind adherence.**

---

## Failure Conditions

A project does **not** follow principles when:

* Core principles are ignored or contradicted
* Structure becomes inconsistent or unclear
* Naming and organization introduce confusion
* Boundaries are violated without justification

---

## Final Note

> **Following principles is what transforms a project from implementation into definition.**

Without alignment to principles, structure becomes accidental.
With alignment, it becomes intentional.
