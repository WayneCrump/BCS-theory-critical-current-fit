# Bardeen-Cooper-Schrieffer-theory-critical-current-fit
This program can be used for fitting the self field critical currents of superconductors with various dimensions. 

Our technique and motivation is described in the paper: https://arxiv.org/abs/1609.03670
Thermodynamic parameters of single- or multi-band superconductors derived from self-field critical currents
Authors: Evgeny Talantsev, Wayne Crump, Jeff Tallon.

In particular we show there that self-field Jc is not determined by vortex movement but by a universal current density limit governed solely by the penetration depth.

The program takes the temperature dependent self field critical current and fits it to find the critical temperature Tc, superconducting gap magnitude Delta0, Specific heat jump at Tc dC/C, and penetration depth lambda0.

Installation:

To use the program you must have the matlab runtime (download link: http://au.mathworks.com/products/compiler/mcr/) version 7.17 (R2012a).
Simply unzip and run the exe.

Usage: 

This program takes current density measurements in the form of a comma seperated file (.csv) where the first column is temperature in Kelvin and the second column is current density in A/m^2.
Also needed for fitting is the materials kappa=penetration depth/coherence length. If the fit is using the thickness correction then the dimensions are needed as well.

Raw data: Format must be .csv with two columns the first is temperature in Kelvin and the second is Self-field critical current density in A/m^2.

Import the raw data into the program. Use the buttons to choose the geometry and type of fit. Input the sample dimensions and Ginzburg -Landau ratio.
