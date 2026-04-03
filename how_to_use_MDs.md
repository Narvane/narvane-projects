# How to Use MDs

## Purpose

This document explains how to use the definition structure during development and validation.

---

## During Development

> **Always start from the definition structure.**

When developing a new feature or evolving a project:

1. Refer to `Definition Structure.md`
2. Use it as the guide to understand:

   * How the system is organized
   * What “being defined” means
   * What principles and structures must be respected

> The goal during development is always to **move the project toward a defined state**.

---

## During Validation

> **Use the definition checkers to verify alignment.**

When finishing a change or evaluating the project:

1. Navigate to `definition_checker/`
2. Run:

   * `isDefined` for full validation
   * Or individual checkers for focused analysis

This will verify whether the project:

* Follows the defined principles
* Meets all definition criteria

---

## Practical Flow

* **Start** → Use `Definition Structure.md` to guide decisions
* **Build** → Apply principles and definitions
* **Validate** → Use `definition_checker/` to confirm alignment

---

## Final Note

> **Development moves toward definition.
> Validation confirms it.**
