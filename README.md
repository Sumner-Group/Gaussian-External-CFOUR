# Gausian-External-CFOUR
Script to couple CFOUR with Gaussian via the "External" keyword
This script was written so that a Gaussian16 anharmonic calculation could be performed using
second derivative data from CFOUR. This is especially useful since Gaussian16 can calculate
sextic distortion constants, whereas the publically available version of CFOUR cannot. The current
has been tested with Gaussian17 A.03 and CFOUR-v2.0beta.

To invoke in Gaussian, use the following set of keywords: 

external="./g16-cfour.script" freq=anharmonic nosymm test

Problems to be addressed:
1) Currently hardwired for CCSD(T)/cc-PVTZ calculations
2) Restart capability is clunky
3) Calculations for 1st/2nd derivatives of normal mode displacements is not parallelized
4) Does not correctly get dipole moment, dipole derivatives and polarizability. Sets them all to zero.

**Do you want to cite this work?**
---
Bunn, H.; Soliday, R. M.; Sumner, I.; Raston, P. L. “Far-infrared spectroscopic characterization of anti-vinyl alcohol” The Astrophysical Journal, 2017, 847, 67-72. [doi:10.3847/1538-4357/aa8870](https://doi.org/10.3847/1538-4357/aa8870)

[![DOI](https://zenodo.org/badge/100960252.svg)](https://zenodo.org/badge/10.5281/zenodo.846364/100960252)
