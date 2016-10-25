# Bardeen-Cooper-Schrieffer-theory-critical-current-fit

INSTALLATION:
To use the program you must have the matlab runtime (download link:http://mathworks.com/products/compiler/mcr/) version 7.17 (R2012a). You may need to restart your computer after installing the runtime.

Simply open the program exe to run.


GENERAL:
This is the Software used for our paper entitled
“Thermodynamic parameters of single- or multi-band superconductors derived from self-field critical currents”
by E. F. Talantsev, W. P. Crump and J. L. Tallon (https://arxiv.org/pdf/1609.03670.pdf). 
Software authors: Wayne Crump and Evgeny Talantsev.
 
This program extracts fundamental parameters of superconductors from the self-field transport critical current densities, Jc(sf,T). These parameters are:
 
1.      Absolute value of the ground-state London penetration depth
2.      Amplitude of the ground-state superconducting energy gap; or two gap for two-band superconductors
3.      Relative specific heat jump(s) at transition temperature(s) 
4.      Transition temperature, or temperatures for two band model  
5.      For two-band superconductors, weighting fraction of each band  
6.      For samples with two-superconducting-phases, the volume fraction of each phase   

We emphasize that the analysis is not applicable to “magnetic” Jc based on Bean model.  
The analysis does not refer to vortex depinning movement because as we show in the paper this is not relevant to the self-field Jc.
The technique and motivation is described in https://arxiv.org/pdf/1609.03670.pdf.
 
The program provides the possibility to select different options:
 
1.      Single or double superconducting band(s)    
2.      Gap(s) symmetry: s- or d-wave
3.      Sample dimensions: from Angstrom to cm   
4.      Ginzburg-Landau parameter k
5.      For two-band or two-phase model: choose either
  5.a.  Alpha-model for which both bands/phases have:
    5.a.1.  the same transition temperature
    5.a.2.  joint London penetration depth
    5.a.3.  band weight described by normalized parameter alpha: 0 < alpha < 1.
  5.b.  Independent-model for which each band has independent
    5.b.1.  transition temperatures
    5.b.2.  London penetration depths
    5.b.3.  In case of cuprates: Uemura’s relation between London penetration depths of each bands can be chosen.  
 
USAGE:
This program takes raw experimental transport critical current densitye data in the form of a comma separated file (.csv), where the first column is temperature in Kelvin and the second column is current density in A/m^2.  
 
After loading the Jc(sf,T) data set, do the following:
 
1.      Use the buttons to choose cross-section geometry of the sample: 
  a.    Round wire;  
  b.    2D thin film (very thin film, where film thickness = 2b << London penetration depth);  
  c.    3D rectangular sample with entire width (2a) and thickness (2b);
2.      Input the sample cross-sectional dimensions
3.      Choose type I or type II superconductor
4.      Choose the gap symmetry: s- or d-wave  
5.      Choose single or double band model
6.      Input Ginzburg -Landau parameter k.

 
Press “fit”. You may choose the number of iterations the fit will do. When the program is fitting a window should appear showing the norm of the residual as it is reduced. The fit will stop if the tolerance is reached before the number of iterations is up.
DERIVED PARAMETERS:
 
BCS parameters of the fit appear in the window:
 
1.      Critical temperature (Tc) in K;
2.      Ground state of superconducting energy gap (Delta0) in meV;
3.      Relative jump in specific heat at Tc (dC/C);
4.      Ground state of London penetration depth (lambda0) in nm.

 
OUTPUT FILE:
 
Press corresponding buttons to save    
Save fit: Save the Jc(sf,T) fit with fit parameters;
Blue line Jc to lambda: Save the Jc(sf,T) fit and Lambda(T) with fit parameters;
Experiment data Jc to lambda: Save the raw Jc(sf,T) and corresponding converted Lambda(T) data.   

 
These output files appeared in *.dat designation.
The program will ask you to save these *.dat file in your location.
