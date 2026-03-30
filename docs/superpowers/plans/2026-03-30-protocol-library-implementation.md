# Protocol Library Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Convert the first batch of uploaded Dean Lab protocol documents into a categorized public protocol library inside the Sphinx site without changing any scientific values.

**Architecture:** Keep `source/protocols.rst` as the protocol hub, create `source/protocols/` with one normalized page per protocol, preserve day-by-day and note-heavy source structure inside a shared page template, and verify the whole section with a strict Sphinx build.

**Tech Stack:** Sphinx, reStructuredText, `pandoc`, `sphinx-build`

---

### Task 1: Build the protocols hub and directory structure

**Files:**
- Modify: `source/protocols.rst`
- Create: `source/protocols/`

- [ ] **Step 1: Replace the placeholder protocols hub with categorized navigation**

```rst
Protocols
=========

This section collects public Dean Lab protocols in a categorized library.

Cloning and Mutagenesis
-----------------------

- :doc:`Gateway Cloning <protocols/gateway-cloning>`
```

- [ ] **Step 2: Add a hidden toctree listing every protocol page**

Run: `rg -n "protocols/" source/protocols.rst`
Expected: every protocol slug appears in the hub file

### Task 2: Convert cloning, bacterial, and cleanup protocols

**Files:**
- Create: `source/protocols/gateway-cloning.rst`
- Create: `source/protocols/dna-shuffling.rst`
- Create: `source/protocols/error-prone-pcr.rst`
- Create: `source/protocols/saturated-mutagenesis.rst`
- Create: `source/protocols/colony-pcr.rst`
- Create: `source/protocols/chemically-competent-cells.rst`
- Create: `source/protocols/bacterial-electroporation.rst`
- Create: `source/protocols/bacterial-colony-fluorescence.rst`
- Create: `source/protocols/bacterial-facs.rst`
- Create: `source/protocols/protein-solubility.rst`
- Create: `source/protocols/gst-protein-purification.rst`
- Create: `source/protocols/purification-small-dna-fragments.rst`
- Create: `source/protocols/ethanol-precipitation.rst`
- Create: `source/protocols/recipes.rst`

- [ ] **Step 1: Normalize the cloning and mutagenesis pages into the shared structure**

```rst
Use sections such as Summary, Materials and Reagents, Procedure, and Notes and Cautions when the source supports them.
Keep all values exactly as extracted from the `.docx` files.
```

- [ ] **Step 2: Normalize the bacterial and cleanup pages without inventing missing details**

```rst
Preserve sparse documents as sparse pages.
Keep operational notes in Notes and Cautions rather than rewriting them into stronger claims.
```

### Task 3: Convert tissue, imaging, and viral protocols

**Files:**
- Create: `source/protocols/labeling-tissue-samples.rst`
- Create: `source/protocols/babb-2-0.rst`
- Create: `source/protocols/agarose-cube-cleared-samples.rst`
- Create: `source/protocols/coating-beads-on-coverslip.rst`
- Create: `source/protocols/quantum-yield-protocol.rst`
- Create: `source/protocols/retrovirus-production.rst`
- Create: `source/protocols/viral-production-imcd-cells.rst`

- [ ] **Step 1: Preserve day-based workflows in the Procedure section**

```rst
Keep `Day 1`, `Day 2`, or weekday labels exactly where the source uses them.
```

- [ ] **Step 2: Cross-link clearly related protocols**

Run: `rg -n "Related Protocols|Related Recipes" source/protocols`
Expected: BABB links to the agarose-cube protocol where appropriate, and related protocol links only appear when the source or workflow clearly supports them

### Task 4: Verify the documentation build and scope

**Files:**
- Test: `source/protocols.rst`
- Test: `source/protocols/*.rst`

- [ ] **Step 1: Run a strict HTML build**

Run: `uv run sphinx-build -W --keep-going -b html source build/html`
Expected: exit code 0 and `build succeeded`

- [ ] **Step 2: Inspect the protocol-library diff**

Run: `git diff -- source/protocols.rst source/protocols docs/superpowers/specs/2026-03-30-protocol-library-design.md docs/superpowers/plans/2026-03-30-protocol-library-implementation.md`
Expected: only protocol-library files and the corresponding spec/plan docs appear in the scoped diff
