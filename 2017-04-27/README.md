# Gammapy Telcon

* Thursday, April 27, 2017 at 11 am
* CTA eZuce, password "dcgammapy" -> anyone interested welcome to join!

## Bruno: introduction

* Regular Gammapy telcons for the coming months?
  Which day / time?
* Sign up on the Gammapy mailing list for announcements:
  https://groups.google.com/forum/#!forum/gammapy

## Roberta: infos on CTA 1DC 

* Slides: [20170427_Gammapy_DC.pdf](20170427_Gammapy_DC.pdf)
  (removed for now, because CTA-DC is a CTA-internal affair. Contact Roberta if you're interested)
* CTA 1DC wiki page: https://forge.in2p3.fr/projects/data-challenge-1-dc-1/wiki


## Christoph: Gammapy update

Basic info:

* Docs: https://gammapy.readthedocs.io/en/latest/
* Tutorials: https://nbviewer.jupyter.org/github/gammapy/gammapy-extra/blob/master/index.ipynb


Updates:

* Will make Gammapy 0.6 release later today:
  https://github.com/gammapy/gammapy/milestones/0.6
* Plan to make releases more often now.
  Next release 0.7 very soon (before 1DC data release), in the coming weeks.
* A lot has happened in the past few months in Gammapy:
  https://gammapy.readthedocs.io/en/latest/changelog.html
  (will add PRs from the past weeks today before making the release).
* There has also been some work on the data format specs: 
  https://gamma-astro-data-formats.readthedocs.io/en/latest/
    * Tarek Hassan added HDUCLASS header keys and support for energy-dependent
      on region for 1D spectral analysis.
    * Matthew Wood defined HEALPIX-based map and cube formats
      (still some discussion) and has started to implement them
      in ``gammapy.maps`` (will then be imported and use in Fermipy)
    * Some polishing of SED formats

High priority (for 1DC):

* Rewrite 3D Background models (current class is broken).
  We'll do it next week.
* Write documentation examples how to analyse the data.
    * For now all we have is this one tutorial: https://nbviewer.jupyter.org/github/gammapy/gammapy-extra/blob/master/notebooks/cta_data_analysis.ipynb 
    * It uses some preliminary test data (in a very similar format that will be used for 1DC)
      Three observations of the Galactic center (EVENTS), plus IRF files in CALDB
      and index files for observation selection and access in the format the
      Gammapy DataStore uses: https://github.com/gammapy/gammapy-extra/tree/master/test_datasets/cta_1dc
    * Besides examples showing how to do an analysis, we need examples
      (or even additions to Gammapy) of how to simulate some (binned) data
      and use it for sensitivity or required observation time calculations,
      or computation of CTA key science project (KSP) metrics.
* Implement (spectral and morphology )models properly (yes, including XML I/O support)
  and then add more models.

For the coming months:

* Support energy-dependency on region in spectral analysis (for MAGIC, CTA)
* Matthew Wood and I are working on merging maps classes
  (WCS and HEALPIX based)
* A lot of small and medium issues and features and cleanup
  https://github.com/gammapy/gammapy/milestones/0.7
* Another f2f meeting before the summer break? Gammapy paper also. 

Conclusion:

* Gammapy is making progress ...
* Try it out, report issues and missing features.
* If you have some time, consider contributing to the code.
  Note that **all contributions are welcome**.
  We'll work with you to help you get your code in order
  (implement it as a re-usable function or class, add a test and write a docs example).
  The starting point can be "I want to do analysis X" or "I have this script that does X"
  with messy code. No worries!

## Discussion

* tbd
