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
