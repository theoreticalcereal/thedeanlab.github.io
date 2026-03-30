# Protocol Library Design

## Goal

Build out the `Protocols` section of the public-facing lab website as a categorized protocol library, starting with the first batch of uploaded Word documents and preserving all protocol values exactly.

## Approved Constraints

- All listed protocols are intended to be published on the public site as full step-by-step methods.
- Protocols should be normalized into a shared page structure.
- Normalization must not alter any values, units, concentrations, times, temperatures, volumes, or sequencing that appear in the source documents.
- Sparse or informal source documents should remain sparse rather than being filled in with inferred details.

## Information Architecture

- Keep [source/protocols.rst](/Users/Dean/Documents/GitHub/thedeanlab.github.io/source/protocols.rst) as the protocol hub page.
- Create a `source/protocols/` directory with one `.rst` page per protocol.
- Organize the hub page by category, with direct links to the protocol pages rather than introducing separate category landing pages in this first pass.

## Protocol Page Template

Each protocol page should use a normalized structure when the source supports it:

- `Title`
- `Summary`
- `Materials and Reagents`
- `Equipment`
- `Procedure`
- `Notes and Cautions`
- `Related Recipes` or `Related Protocols`

The template is a structural tool, not a permission to rewrite scientific content.

## Content Handling Rules

- Preserve exact values from the source documents.
- Do not silently fix typos, convert units, or harmonize conflicting wording.
- Keep day-by-day protocols as day-by-day procedures inside the `Procedure` section.
- Keep very short protocols, such as recipes, short.
- If a statement is operationally useful but informal, preserve it in `Notes and Cautions` rather than rewriting it into a stronger instruction than the source supports.
- Do not invent missing reagent lists, equipment, safety notes, or intermediate steps.

## Category Map for the First Batch

### Cloning and Mutagenesis

- Gateway Cloning
- DNA Shuffling
- Error Prone PCR
- Saturated Mutagenesis
- Colony PCR

### Bacterial Methods

- Preparation of Chemically Competent Cells
- Bacterial Electroporation
- Bacterial Colony Fluorescence
- Bacterial FACS

### Protein and DNA Cleanup

- Protein Solubility
- GST Protein Purification
- Purification of Small DNA Fragments
- Ethanol Precipitation

### Tissue Preparation and Clearing

- Labeling Tissue Samples
- BABB 2.0 Protocol
- Agarose Cube for Cleared Samples

### Viral Production

- Retrovirus Production
- Viral Production - IMCD Cells

### Imaging and Calibration

- Coating Beads on Coverslip
- Quantum Yield Protocol

### Recipes

- Recipes

## File Layout

The initial implementation should create stable slugs under `source/protocols/`, including files such as:

- `gateway-cloning.rst`
- `dna-shuffling.rst`
- `error-prone-pcr.rst`
- `saturated-mutagenesis.rst`
- `colony-pcr.rst`
- `chemically-competent-cells.rst`
- `bacterial-electroporation.rst`
- `bacterial-colony-fluorescence.rst`
- `bacterial-facs.rst`
- `protein-solubility.rst`
- `gst-protein-purification.rst`
- `purification-small-dna-fragments.rst`
- `ethanol-precipitation.rst`
- `labeling-tissue-samples.rst`
- `babb-2-0.rst`
- `agarose-cube-cleared-samples.rst`
- `retrovirus-production.rst`
- `viral-production-imcd-cells.rst`
- `coating-beads-on-coverslip.rst`
- `quantum-yield-protocol.rst`
- `recipes.rst`

## Conversion Workflow

- Extract each `.docx` source directly with `pandoc`.
- Translate the extracted content into reStructuredText manually.
- Cross-link protocols and recipes where the source clearly points to another method.
- Run a strict Sphinx build after the first batch is integrated.

## Scope of This First Implementation

This first implementation covers the batch of 21 uploaded protocol documents supplied in the request. The design should make later additions straightforward without restructuring the hub page again.
