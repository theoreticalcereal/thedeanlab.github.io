Gateway Cloning
===============

Materials and Reagents
----------------------

BP reactions
^^^^^^^^^^^^

- 2 μL of pDonr221 (150 ng/μL) in T.E.
- 60 ng of attB PCR product
- 2 μL of BP clonase
- 5 uL of T.E.

LR reactions
^^^^^^^^^^^^

- 2 μL of Destination Vector (150 ng/μL)
- 200 ng/μL of pDonr221 library

Procedure
---------

For electroporation of library
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Combine two 10 μL LR reactions.
2. Remove salts through ethanol precipitation.
3. Resuspend into 2.5 μL of T.E.

BP reactions
^^^^^^^^^^^^

- Incubate for 18 hours at 25 degrees Celsius.
- The source document notes that this gives around 600,000 clones.

Notes and Cautions
------------------

- BP and LR clonase have different optimal conditions. For optimal efficiency,
  necessary to perform Proteinase k digestion (>4x improvement).
- If the initial library is made by recombining into pDonr221 and then
  maxi-prepping the library, one should perform EcorV digestion of the
  pDonr221-library prior to the LR reaction.
- Combining two reactions for every 50 μL of electrocompetent cells appears to
  work well. No additional gain observed when combining four reactions.
- The LR reaction works best if the donor fragment has been relaxed. So long as
  your gene does not contain EcorV, this restriction endonuclease works well at
  site-specifically cleaving the vector backbone of pDonr221.
- Alternatively, the gene to be cloned into your destination vector with LR
  Clonase II can be amplified from a pDonr221 parent with M13Forward and
  M13Reverse.
- The latter is ideal for generating libraries since this decreases cost,
  preserves diversity of the library, and saves time.

Related Protocols
-----------------

- :doc:`ethanol-precipitation`
- :doc:`bacterial-electroporation`

