Saturated Mutagenesis
=====================

Materials and Reagents
----------------------

Standard PCR conditions apply
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- 40 μL deionized H2O
- 5 μL 10x Pfu Buffer
- 1 μL 10 mM dNTP
- 1 μL 1DNA template (⇡ 100 ng/1 μL)
- 1 μL 25 μM Primer 1
- 1 μL 25 μM Primer 2
- 1 μL 25 of Pfu Polymerase

PCR setup
^^^^^^^^^

- 1 x 95 degrees - 2 minutes
- 3 x 95 degrees - 2 minutes
- 1 x 56 degrees - 30 seconds
- 1 x 72 degrees - (1 min/kb)
- 3 x 95 degrees - 2 minutes
- 1 x 54 degrees - 30 seconds
- 1 x 72 degrees - (1 min/kb)
- 20 x 95 degrees - 2 minutes
- 1 x 52 degrees - 30 seconds
- 72 degrees - (1 min/kb)
- 1x 72 degrees - 10 minutes

Procedure
---------

1. Design primers to introduce mutations at the specified position within the gene.
2. In separate PCR reactions, amplify fragments using Pfu.
3. Purify DNA fragments with 2% agarose gel, and determine the reaction yield
   for each individual fragment with a NanoDrop UV-Vis spectrophotometer.
4. Take 5 μL of each fragment (100 ng each fragment) and combine in a single
   PCR tube using Pfu reaction components (buffer, etc.).
5. Repeat with PCR reaction, as above, except with 60 seconds of annealing time
   instead of 30 seconds, and with the elongation time adjusted to provide
   amplification of the entire gene.
6. Gel purify resulting DNA fragment with 1% ultra-pure agarose with ethidium bromide.
7. If fragment size is as expected, continue to ligation, gateway recombination, etc.

Notes and Cautions
------------------

- The nucleotide wildcards should be approximately located within the center of
  the primers, secondary structure should be minimized, and the annealing
  temperature should be kept high (>65 C).
- In general, the fragments of the gene that you amplify should be greater than
  70 base pairs because of difficulties in PCR amplification and purification of
  smaller DNA fragments.
- Pfu is always used for amplification of the fragments.
- For site-overlap extension, Pfu is preferred over Taq given that it will
  introduce less errors outside of the regions of interest.
- However, for some challenging site-overlap extension reactions where Pfu
  fails, Taq has been used.
- It is very common to see partially amplified fragments in this reaction.

Related Protocols
-----------------

- :doc:`gateway-cloning`

