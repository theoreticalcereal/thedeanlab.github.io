# Lab Resources Handbook Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Restructure the `Lab Resources` section into a public-facing handbook that reflects the approved page map and updated meeting schedule.

**Architecture:** Keep `source/resources.rst` as the handbook hub, expand existing handbook pages in place, add a small set of new top-level pages for cross-cutting topics, and preserve compatibility for older policy-page URLs with short forwarding pages.

**Tech Stack:** Sphinx, reStructuredText, Makefile-based HTML build

---

### Task 1: Create the handbook hub and top-level handbook pages

**Files:**
- Create: `source/meetings.rst`
- Create: `source/digital-tools.rst`
- Create: `source/working-at-utsw.rst`
- Create: `source/departure.rst`
- Modify: `source/resources.rst`

- [ ] **Step 1: Draft the new top-level handbook pages with approved sections**

```rst
Create handbook pages for meetings, digital tools, institutional logistics, and departure guidance.
Use concise public-facing language and omit funding-account specifics.
```

- [ ] **Step 2: Turn `source/resources.rst` into the handbook landing page**

```rst
Add short summaries for each handbook area and list all handbook pages in one toctree.
```

- [ ] **Step 3: Verify the new pages are linked from the handbook hub**

Run: `rg -n "meetings|digital-tools|working-at-utsw|departure" source/resources.rst`
Expected: each page appears in the `Lab Resources` toctree exactly once

### Task 2: Expand existing handbook pages and policy details

**Files:**
- Modify: `source/onboarding.rst`
- Modify: `source/policies.rst`
- Modify: `source/data-management.rst`
- Modify: `source/equipment.rst`
- Modify: `source/protocols.rst`
- Modify: `source/policies/working-hours.rst`
- Modify: `source/policies/leave-time.rst`
- Modify: `source/policies/authorship.rst`
- Modify: `source/policies/lab-cleaning.rst`
- Modify: `source/policies/safety.rst`

- [ ] **Step 1: Replace placeholder copy with handbook content**

```rst
Populate onboarding, policy, data, equipment, and protocol pages using the approved information architecture.
```

- [ ] **Step 2: Apply meeting and public-content updates**

```rst
Reflect the Monday 1:00 PM whole-team meeting, remove focus group meetings, and set the Dean Lab meeting to Monday 3:00 PM.
Remove funding-account specifics.
```

- [ ] **Step 3: Cross-link related pages**

Run: `rg -n ":doc:`" source/onboarding.rst source/policies.rst source/data-management.rst`
Expected: onboarding, policies, and data pages link to the related handbook pages where useful

### Task 3: Preserve compatibility and verify the docs build

**Files:**
- Modify: `source/policies/meetings.rst`
- Modify: `source/policies/data-sharing.rst`
- Modify: `source/policies/lab-jobs.rst`

- [ ] **Step 1: Convert legacy policy pages into short forwarding pages or orphans**

```rst
Keep old policy URLs from breaking by pointing readers to the new top-level handbook pages.
```

- [ ] **Step 2: Run the HTML build with warnings treated as errors**

Run: `make html SPHINXOPTS="-W --keep-going"`
Expected: Sphinx build exits with code 0 and writes HTML to `build/html`

- [ ] **Step 3: Inspect git diff for scope control**

Run: `git diff -- source docs/superpowers`
Expected: only handbook content, spec, and plan changes appear

