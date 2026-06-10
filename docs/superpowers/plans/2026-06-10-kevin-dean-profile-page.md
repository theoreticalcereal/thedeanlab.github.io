# Kevin Dean Profile Page Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add a canonical Kevin Dean profile page to the existing Sphinx site with professional native styling, downloadable assets, and structured data.

**Architecture:** Keep the implementation Sphinx-native: one new RST page, one small static stylesheet, copied static profile assets, and a homepage navigation update. A focused pytest protects the canonical identity language, polished section labels, profile links, asset references, and structured data markers.

**Tech Stack:** Sphinx, reStructuredText, Read the Docs theme, CSS, pytest, JSON-LD embedded through raw HTML.

---

### Task 1: Add the failing profile content test

**Files:**
- Create: `tests/test_kevin_dean_profile.py`

- [ ] **Step 1: Write a test for the expected profile source**

```python
from pathlib import Path


ROOT = Path(__file__).resolve().parents[1]
PROFILE = ROOT / "source" / "kevin-dean.rst"
INDEX = ROOT / "source" / "index.rst"
CONF = ROOT / "source" / "conf.py"


def test_kevin_dean_profile_contains_canonical_public_identity():
    text = PROFILE.read_text(encoding="utf-8")

    required = [
        "Kevin M. Dean, Ph.D.",
        "I build open-source, adaptive light-sheet microscopes and image-analysis workflows to reveal rare metastatic colonization events in intact tissues.",
        "Assistant Professor",
        "Lyda Hill Department of Bioinformatics",
        "Executive Director, Cancer Cell Imaging Core",
        "Research thesis",
        "Selected publications",
        "Selected tools",
        "Talks and media",
        "Contact",
        "Download public CV",
    ]

    for phrase in required:
        assert phrase in text


def test_kevin_dean_profile_links_assets_and_structured_data():
    text = PROFILE.read_text(encoding="utf-8")

    required = [
        "_static/kevin-dean-headshot.jpg",
        "_static/kevin-dean-cv.pdf",
        "https://scholar.google.com/citations?user=Uv0B5xIAAAAJ&hl=en",
        "https://orcid.org/0000-0003-0839-2320",
        "https://github.com/thedeanlab/",
        "https://github.com/AdvancedImagingUTSW",
        "https://www.linkedin.com/in/kevin-m-dean/",
        "https://bsky.app/profile/kevin-dean.bsky.social",
        "https://profiles.utsouthwestern.edu/profile/155475/kevin-dean.html",
        '"@type": "ProfilePage"',
        '"@type": "Person"',
        '"sameAs"',
    ]

    for phrase in required:
        assert phrase in text


def test_kevin_dean_profile_is_linked_and_css_is_enabled():
    index = INDEX.read_text(encoding="utf-8")
    conf = CONF.read_text(encoding="utf-8")

    assert ":doc:`kevin-dean`" in index
    assert "kevin-dean" in index
    assert 'html_static_path = ["_static"]' in conf
    assert 'html_css_files = ["profile.css"]' in conf
```

- [ ] **Step 2: Run the test to verify it fails before implementation**

Run: `uv run pytest tests/test_kevin_dean_profile.py -q`

Expected: fail because `source/kevin-dean.rst` does not exist yet.

### Task 2: Add static profile assets and Sphinx styling hook

**Files:**
- Copy: `/Users/Dean/Library/CloudStorage/OneDrive-UniversityofTexasSouthwestern/Portraits/2024-12-06/24-1206_Kevin Dean_13 copy.jpg` to `source/_static/kevin-dean-headshot.jpg`
- Copy: `/Users/Dean/Documents/GitHub/CV/kevin_dean_cv.pdf` to `source/_static/kevin-dean-cv.pdf`
- Modify: `source/conf.py`
- Create: `source/_static/profile.css`

- [ ] **Step 1: Copy the approved assets into Sphinx static files**

Run:

```bash
mkdir -p source/_static
cp "/Users/Dean/Library/CloudStorage/OneDrive-UniversityofTexasSouthwestern/Portraits/2024-12-06/24-1206_Kevin Dean_13 copy.jpg" source/_static/kevin-dean-headshot.jpg
cp "/Users/Dean/Documents/GitHub/CV/kevin_dean_cv.pdf" source/_static/kevin-dean-cv.pdf
```

Expected: both files exist under `source/_static`.

- [ ] **Step 2: Enable custom static assets in Sphinx**

Set in `source/conf.py`:

```python
html_static_path = ["_static"]
html_css_files = ["profile.css"]
```

- [ ] **Step 3: Add restrained profile styling**

Create `source/_static/profile.css` with styles for `.profile-hero`, `.profile-headshot`, `.profile-links`, `.profile-grid`, `.profile-card`, and `.profile-meta` that preserve the Read the Docs theme while improving layout and spacing.

### Task 3: Add the Kevin Dean profile page and homepage link

**Files:**
- Create: `source/kevin-dean.rst`
- Modify: `source/index.rst`

- [ ] **Step 1: Add `source/kevin-dean.rst`**

Include the approved content sections, headshot, CV download link, hero bio, unlabeled long-form bio, professional positions, selected publications with research thesis intro, tools, talks/media, compact contact details, profile links, and raw JSON-LD structured data.

- [ ] **Step 2: Link the page from the homepage**

Add the `kevin-dean` document link to the visible `Wiki Sections` list and add `kevin-dean` to the hidden toctree.

### Task 4: Verify tests, build, and browser rendering

**Files:**
- Test: `tests/test_kevin_dean_profile.py`
- Test: `source/kevin-dean.rst`
- Test: `source/index.rst`
- Test: `source/conf.py`
- Test: `source/_static/profile.css`

- [ ] **Step 1: Run the focused test**

Run: `uv run pytest tests/test_kevin_dean_profile.py -q`

Expected: all tests pass.

- [ ] **Step 2: Run a strict Sphinx build**

Run: `uv run sphinx-build -W --keep-going -b html source build/html`

Expected: exit code 0 and no warnings.

- [ ] **Step 3: Serve and inspect locally**

Run: `python3 -m http.server 8020 --directory build/html`

Open `http://127.0.0.1:8020/kevin-dean.html` in the browser and verify the page renders without layout overlap, the headshot displays, the CV link resolves, and the page reads professionally in desktop and mobile widths.
