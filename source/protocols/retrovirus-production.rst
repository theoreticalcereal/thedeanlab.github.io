Retrovirus Production
=====================

Materials and Reagents
----------------------

Day 2 transfection mix
^^^^^^^^^^^^^^^^^^^^^^

- 1 μg pVSV-G
- 8 μg desired DNA in viral vector (usually pCLNCX, or pCL-TetOn)
- 8 μg packaging vector (usually pCL-Ampho)
- 700 μL OptiMem
- 20 μL Trans-IT

Procedure
---------

Day 1
^^^^^

- Plate 293 cells in 10 cm dishes.

Day 2
^^^^^

- Transfect virus into 293 cells using Trans-IT.
- Let mixture sit at room temperature at least 15 min, then add to cells.

Day 3
^^^^^

- Change medium of transfected HEK293 cells.

Day 4
^^^^^

1. Look at cells to see if transfection worked.
2. Remove media and gently filter through a cellulose acetate or polysulfonic
   0.45 micron filter (dont use nitrocellulose) to remove any unwanted cell debris.
3. Change the media, keeping in mind that you will also be adding virus containing supernatant.
4. Add polybrene to fresh media and cells, and swirl in dish to distribute.
5. Add viral supernatant (100 μL to 3 mL, depending upon how optimized the transfection was).

Day 5
^^^^^

- Change the media on the cells that were infected, since polybrene can alter cell growth.

Day 6-7
^^^^^^^

- Select for positive cells.
- If fluorescent, this can be FACS.

Notes and Cautions
------------------

- Cell density should be such that cells are 70% confluent tomorrow.
- You need to do this very carefully since HEK293 cells do not adhere to the
  plate strongly.
- If you are using a fluorescent protein, pCLNCX transfected cells should be brightly fluorescent.
- If you are using pCL-TetOn, addition of doxycycline (final concentration <1μg/mL)
  can trigger gene expression.
- At this point virus can be used to infect cells or can be frozen for future use.
- In general, after 48 hours, virus production is at its maximum rate.
- However, additional virus can be obtained at 72 hours if the HEK293 cells are
  still adhering to the plate.
- If you would like to freeze the virus, flash freezing in liquid nitrogen and
  storage at - 80 Celsius is recommended.
- Note that the titer (infectability) of the virus will decrease after being frozen.
- To carry out infection, the cells should be exponentially growing, and have
  not been trypsinized for 24 hours.
- Retrovirus can only infect dividing cells, and relies upon receptors for internalization.
- The final concentration of polybrene should be 12 μg/mL (although polybrene
  can be titrated from 2 - 12 μg/mL if 12 μg/mL is found to be toxic).
- Virus integration follows a Poisson distribution, and high enough
  concentrations of virus supernatant can inhibit infection.
- For libraries, a multiplicity of infection of ⇡ 10% is desired, and titrating
  the virus can help achieve this.
- For Tet-inducible virus (pCL-TetOn), you will need to also infect the cells
  with pCL-TRE (Tet-Resonsive Element).
- If you infected cells with a library that has variable fluorescence, e.g., a
  mutated FP library, you can treat the cells for 1 week at 1 mg/mL G418 to
  eliminate non-infected cells.

Related Protocols
-----------------

- :doc:`viral-production-imcd-cells`

