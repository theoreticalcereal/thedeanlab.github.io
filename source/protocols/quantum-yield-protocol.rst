Quantum Yield Protocol
======================

Procedure
---------

1. Decide which wavelength region that you are particularly interested in.
2. Once you have repeated this for all of your solutions, you can plot a graph
   of the integrated fluorescence versus absorbance. Make sure that you measure
   the fluorescence on a blank sample for each different solvent that you use,
   and subtract this value from your integrated fluorescence values.
3. Fit the integrated fluorescence intensity versus absorbance plot to a linear
   equation, and force the y-axis through 0.
4. Take the slopes from the fit, and insert the values into the following equation:

   ``phix = phiref × (Slopex / Sloperef) × (ηx^2 / ηref^2)``

Notes and Cautions
------------------

- Measuring the fluorescence quantum yield is relatively easy, but
  time-consuming, and often somewhat inaccurate.
- The inaccuracies of the method can be overcome by minimizing the number of
  transfers, i.e., between the spectrophotometer and the fluorimeter,
  performing the appropriate zero/baseline, cleaning vigorously between
  measurements, and minimizing the time between the measurements.
- All of these things decrease the amount of protein/dye that can absorb onto
  the cuvette, or evaporation that can decrease the sample volume.
- Overall error within 10% of established values is deemed a success.

Reference dye selection
^^^^^^^^^^^^^^^^^^^^^^^

- For citations regarding these references, refer to Lakowicz - Principles of Fluorescence Spectroscopy.
- Be cautious however, many of these dyes show a rather large concentration,
  pH, and temperature dependence with regard to their quantum yield.
- The dye should be selected such that your sample, and the dye can both be
  excited at the same wavelength, and the entire emission can be observed.
- The excitations listed below are not absolute, and I recommend measuring the
  excitation/emission spectra of your sample and the reference dye, and picking
  a wavelength that works best for you.
- Furthermore, the use of two reference dyes is far better than one, preferably
  one with a quantum yield greater than your sample, and one with a quantum
  yield less than your sample.
- This not only gives you two measures of quantum yield, thus providing a
  measure of error, but allows you to cross-calibrate each reference dye with
  the other and estimate the amount of error in the measurement.

Cuvette Choice
^^^^^^^^^^^^^^

- All measurements must take place on a dilute sample whereby the maximum
  absorbance red-shifted of where you measuring the absorbance is 0.1 for a 1
  cm cuvette, or 0.4 for a 4 cm cuvette.
- For example, if you are measuring the absorbance at 530, but the dye has an
  absorbance maximum at 560, then the peak at 560 should never be greater than
  the aforementioned ODs.
- In JILA, I have machined a cuvette holder for the 4 cm cuvette and highly
  recommend its use given that the error decreases substantially with the
  longer path-length.

Spectrophotometer Choice
^^^^^^^^^^^^^^^^^^^^^^^^

- I prefer to use the Cary spectrophotometer in JILA given that this instrument
  is extremely sensitive and reproducible.
- One needs to make sure that the instrument is in dual-beam mode such that
  intensity changes are corrected for.
- Also, prior to reading your sample, one should place the cuvette into the
  spectrophotometer with your buffer solution, zero, then baseline this
  solution, and then without moving the cuvette, add your protein and measure
  the absorbance.
- It is at this stage that I write down the absorbance at the exact wavelength
  that I will excite at in the fluorimeter, transfer about a mL (4 cm cuvette)
  into an eppendorf tube, dilute the original sample without introducing
  bubbles, and measure again.
- I repeat this process until I have 4-5 samples of appropriate intensity
  (OD= .4, .3, .2, .1, .05).
- Under ideal conditions, one would be able to take the cuvette directly from
  the spectrophotometer and place it into the fluorimeter, thereby measuring
  the exact same solution.
- This will no doubt decrease your error, but in cases with multiple samples,
  the duration of time to do this would be too onerous.

Fluorimeter Choice
^^^^^^^^^^^^^^^^^^

- The Perkins lab fluorimeter is nice because it offers temperature control,
  and is also much faster and appears to be more sensitive than the PTI
  fluorimeter in BioFrontiers.
- Furthermore, it is in the same building as the spectrophotometer, an obvious
  advantage.
- However, I have measured the exact same solutions on both fluorimeters, and
  both fluorimeters have given me the exact same quantum yield.

Equation notes
^^^^^^^^^^^^^^

- Here, is the quantum yield of your unknown (subscript x) and your reference
  standard (subscript ref).
- The slopes are determined from the aforementioned linear-fit.
- η is the refractive indices for the solutions used, and NIST reported
  refractive indices are the following: water (1.3336), Methanol (1.3290),
  Ethanol (1.3614).
- One can also measure the refractive index yourself with the refractometer
  that is available in Dr. Robert Kutchta's lab.
- It is likely that the refractive index between buffered solutions and
  deionized water will be different.

Outcome checks
^^^^^^^^^^^^^^

- Linear relationship between absorbance and fluorescence.
- Graph naturally goes through zero.
- Cross-calibration of each reference dye gives the reported value within 10% error.

