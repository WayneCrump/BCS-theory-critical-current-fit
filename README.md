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

Raw data: Format must be .csv with two columns the first is temperature in Kelvin and the second is Self-field critical current density in A/m^2.

Import the raw data into the program. Use the buttons to choose the geometry and type of fit. Input the sample dimensions and Ginzburg -Landau ratio.

The parameters of the fit are the critical temperature (Tc), the zero temperature energy gap (Delta0), the jump in specific heat at Tc (dC/C), and the zero temperature penetration depth (lambda0). You can manually change these parameters yourself or the program will try to fit them using a least squares approach.
