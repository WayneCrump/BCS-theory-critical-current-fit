# Bardeen-Cooper-Schrieffer-theory-critical-current-fit
This program can be used for fitting the self field critical currents of superconductors with various dimensions. 

Thermodynamic parameters of single and multi-band superconductors derived from self-field critical currents.

Authors: Evgeny Talantsev, Wayne Crump, Jeff Tallon.

Installation:
To use the program you must either have matlab or have the matlab runtime (download link: http://au.mathworks.com/products/compiler/mcr/).
Matlab version 2012a or later is recommended.
Simply unzip and run the exe.

Usage: 

This program takes current density measurements in the form of a comma seperated file (.csv) where the first column is temperature in Kelvin and the second column is current density in A/m^2.
Also needed for fitting is the materials kappa=penetration depth/coherence length. If the fit is using the thickness correction then the dimensions are needed as well.
