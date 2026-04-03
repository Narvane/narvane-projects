# Is Following Principles

## Purpose

This checker verifies whether each project satisfies the **Follow Principles** definition.

---

## Execution Instruction

> **Check if each project follows the definition of “Follow Principles”.**

1. Navigate to `definition_of_defined/Follow Principles.md`
2. Read and understand the definition
3. Navigate to `defined_projects/`
4. For each project, if **`by_pass_definition_principles.md`** exists at the project root, read it and treat **only** the documented, scoped items as acceptable deviations when judging principle alignment
5. For each project:

   * Evaluate whether it complies with that definition, **accounting for valid bypass entries** where applicable

---

## Output Format

For each project, provide:

* Status:

  * ✅ Following Principles
  * ❌ Not Following Principles

* Short justification based on the definition (and cite `by_pass_definition_principles.md` if it changed the verdict)

---

## Final Note

> **This checker does not define principles — it verifies alignment with the definition of following them.**
