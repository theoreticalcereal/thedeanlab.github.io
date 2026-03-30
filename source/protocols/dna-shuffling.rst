DNA Shuffling
=============

Materials and Reagents
----------------------

Fragmentation reaction
^^^^^^^^^^^^^^^^^^^^^^

In 100 μL combine:

- 3 μg of the DNA substrate(s)
- 0.3 units of DNase I (Promega)
- 10 x RQ1 DNaseI

Primerless PCR mix
^^^^^^^^^^^^^^^^^^

- 10-30 ng/μL DNA
- 2 μL 10 mM dNTPs
- 10 x Taq Buffer (2.2 mM MgCl2, 50 mM KCl, 10 mM Tris-HCl, pH 9.0, 0.1% Triton X-100)
- 2.5 U Taq Polymerase
- 100 μL total reaction volume

Procedure
---------

Fragmentation
^^^^^^^^^^^^^

1. PCR amplify the genes of interest, and gel-purify to remove template and primers.
2. Incubate for 15-20 minutes at 20 Celsius.
3. Add to the reaction with RQ1 Stop Buffer.
4. Incubate at 65 Celsius for 10 minutes.
5. Purify 50-200 base pair fragments by electrophoresis onto a DE81 paper.
6. Elute with 1 M NaCl.
7. Purify DNA by ethanol precipitation.

Primerless PCR
^^^^^^^^^^^^^^

Set up PCR thermocycler:

- 45 x 95 Celsius for 30s
- 1 x 50 Celsius for 30s
- 1 x 72 Celsius for 30s
- 1 x 72 Celsius for 10 min

Follow-up
^^^^^^^^^

1. Dilute primerless PCR reaction.
2. Dilute 1:40 into typical PCR mixture, with store-bought Taq Polymerase
   Buffer and Taq Polymerase.

Notes and Cautions
------------------

- Alternatively, for larger fragments (e.g., >80 base pairs), the appropriately
  sized bands can be excised from the 2% gel and gel-purified using a
  commercial kit.
- Use of Pfu, or homemade Taq buffer (as above in step 3), appears to give an
  unnecessarily large amount of frame-shifts.
- The paper, "Optimization of DNA shuffling for high-fidelity recombination",
  provides useful tips for how to control the error-rate.
- For example, using Mn(II) instead of Mg(II) during the DNase I fragmentation
  step improves fidelity 3-fold (10x reaction buffer: 500 mM Tris-HCl pH 7.4,
  100 mM MnCl2).
- Also, use of higher fidelity polymerases (they use Pfu) for both the original
  PCR amplification, primerless amplification, and standard primer
  amplification, can improve fidelity.
- Additionally, obtaining the fragments to be DNaseI treated from restriction
  digest of a plasmid can decrease the errors.
- Protocol adopted from Stemmer, PNAS, 1994.

Related Protocols
-----------------

- :doc:`ethanol-precipitation`

