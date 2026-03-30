# Figure Preparation Page Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add a standalone handbook page that formalizes the Dean Lab's expectations for manuscript-ready figures and links it into the existing handbook structure.

**Architecture:** Create one new top-level RST page for figure-preparation, update the Lab Resources hub to surface it, and add small cross-links from adjacent handbook pages that already discuss figures or meeting preparation.

**Tech Stack:** Sphinx, reStructuredText, Makefile/`sphinx-build`

---

### Task 1: Add the figure-preparation handbook page

**Files:**
- Create: `source/figure-preparation.rst`

- [ ] **Step 1: Draft the standalone policy page**

```rst
Include sections for purpose, core principle, lab non-negotiables, journal specifications, working defaults, Nature guide notes, and review standard.
```

- [ ] **Step 2: Encode the objective lab rules clearly**

```rst
State the font, label-size, line-weight/panel-style, vector-text, AI-image, and two-second-test rules as the non-negotiable checklist.
```

### Task 2: Link the new page into the handbook

**Files:**
- Modify: `source/resources.rst`
- Modify: `source/data-management.rst`
- Modify: `source/meetings.rst`

- [ ] **Step 1: Add the page to the Lab Resources overview and toctree**

Run: `rg -n "figure-preparation" source/resources.rst`
Expected: the new page appears in both the overview bullets and the toctree

- [ ] **Step 2: Add light cross-links from related pages**

```rst
Link from data-management for figure formatting context and from meetings for one-on-one preparation context.
```

### Task 3: Verify the documentation build

**Files:**
- Test: `source/figure-preparation.rst`
- Test: `source/resources.rst`
- Test: `source/data-management.rst`
- Test: `source/meetings.rst`

- [ ] **Step 1: Run a strict HTML build**

Run: `uv run sphinx-build -W --keep-going -b html source build/html`
Expected: exit code 0 and `build succeeded`

- [ ] **Step 2: Inspect the scoped diff**

Run: `git diff -- source/figure-preparation.rst source/resources.rst source/data-management.rst source/meetings.rst docs/superpowers/specs/2026-03-30-figure-preparation-design.md docs/superpowers/plans/2026-03-30-figure-preparation-page.md`
Expected: only the new figure-preparation page, handbook links, and the spec/plan docs are included

