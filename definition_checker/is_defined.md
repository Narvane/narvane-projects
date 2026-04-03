# isDefined

## Purpose

This checker acts as the **aggregator of all definition checks**.

> **A project is defined only if it passes all checkers within `definition_checker/`.**

---

## Execution Instruction

> **Execute all checkers inside `definition_checker/` and aggregate their results.**

1. Navigate to `definition_checker/`
2. Identify all checker files within the directory
3. For each project under `defined_projects/`, if the file **`by_pass_definition_principles.md`** exists at that project’s root, **read it** and keep its declared exceptions in mind for step 4
4. Execute each checker independently
5. Collect all results, **applying declared exceptions** where they apply (see below)

---

## Declared exceptions (`by_pass_definition_principles.md`)

Some projects may include, at their root, a file named exactly:

> **`by_pass_definition_principles.md`**

When this file is present:

* Read it **before** concluding that a checker failed for reasons covered there
* In a monorepo-style layout (e.g. one folder under `defined_projects/` containing `projects/<module>/`), treat **each** `by_pass_definition_principles.md` found at (1) that top-level folder’s root and/or (2) a module root such as `projects/<module>/` as applying to findings scoped to that folder
* Each entry must be a **scoped, justified** deviation (what is bypassed, why, and what remains in scope)
* The bypass file **does not** waive description requirements, empty checklists, or vague “ignore everything” claims — only **documented, delimited** exceptions count
* In the aggregated output, list bypassed items explicitly — for example: *Follow principles: ✅ Passed (with documented exceptions per `by_pass_definition_principles.md`)* — when the only failures would have been those exceptions

If no such file exists, there are **no** automatic exceptions.

---

## Evaluation Logic

For each project:

* If **all checkers pass** (after applying valid entries from `by_pass_definition_principles.md` when present) → ✅ Defined
* If **any checker fails** on grounds **not** covered by a valid bypass entry → ❌ Not Defined

---

## Output Format

For each project, provide:

### 1. Final Status

* ✅ Defined
* ❌ Not Defined

### 2. Checker Results

* List each checker executed
* Show its result:

  * ✅ Passed
  * ❌ Failed

---

## Expected Behavior

* Do not skip any checker
* Do not assume results — execute all
* Treat each checker as a required condition **except** where a project’s `by_pass_definition_principles.md` explicitly and justifiably covers the finding
* Always mention bypass files in the aggregated report when they affect the outcome

---

## Final Note

> **Definition is the result of all validations combined — not a single check.**
