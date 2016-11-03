# Bardeen-Cooper-Schrieffer-theory-critical-current-fit

INSTALLATION:
To use the program you must have the matlab runtime (download link:http://mathworks.com/products/compiler/mcr/) version 7.17 (R2012a). The file is around 350 MB in size. You may need to restart your computer after installing the runtime.

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
The technique and motivation is described in the paper.

USAGE:
This program takes raw experimental transport self-field critical current density data in the form of a comma separated variable file (.csv), where the first column is temperature in K and the second column is current density in A/m^2.  

After loading the Jc(sf,T) data set, you have several options to choose how to fit the data.

1.  Choose the sample geometry:

    2D sample:  The sample is 2 dimensional e.g. a monolayer of atoms;
    
    3D sample:  The sample is rectangular in shape e.g. thin film samples. Here you will have to input the width (2a) and the thickness (2b) in micron;
    
    Wire - Bessel:  The sample is a wire. The exact Bessel functions are used in this solution. Here you will have to input the diameter (2a) in micron;
    
    Wire - tanh:  This is an approximation of the Bessel function solution. Use this when the ratio of the wire radius to the london penetration depth will be higher then 700. Here you will have to input the diameter (2a) in micron;
   
2.  Choose the superconductor type to be I or II and input the Ginzburg-Landau parameter kappa;
3.  Choose the superconductor gap symmetry to be S-wave or D-wave;
4.  The anisotropy should be set to 1. In cases where the current flows perpendicular to the c-axis and the london penetration depth in the a or b direction is different to the penetration in the c direction (the cuprates), you can set this to be the anisotropy in the penetration depth. The fitted penetration depth will be in the c direction.
5.  Choose whether you are fitting a single band or two band superconductor. The alpha model assumes the the critical temperature and penetration depth of each band is the same. The independent model assumes each band has a seperate critical temperature and penetration depth. The Uemura model links the second band penetration depth to the first band using the ratio of the critical temperatures under a square root.

Next you may press “fit”. You may choose the number of iterations the fit will work through. When the program is fitting text should appear in the DOS windows showing the progress of the fit. The fit will stop if the tolerance is reached before the number of iterations is up.

After the fit is complete the derived parameters along with their errors and dependencies will appear. These parameters are the critical temperature (Tc) in K, the ground state of superconducting energy gap (Delta0) in meV, the relative jump in specific heat at Tc (dC/C), and the ground state of London penetration depth (lambda0) in nm.

The tick boxes beside each parameter will choose whether the program will try and fit it or not.

The "Calc" button will use the fit parameters to calculate the self-field current density from 0 K to the critical temperature and this will appear as a blue line. The number of points used to make the line can be changed.

OUTPUT FILE:
 
The output may be saved using the "Save fit" button. This will save the fit options, fit parameters and the calculated points making up the blue line.
The "Blue Jc line to lambda" button will save a file containing the calculated blue line self-field critical current density converted to penetration depth values using the formula in the paper.
The "Experiment data Jc to lambda" button will save a file containing the green experimental data points converted to penetration depth values using the formula in the paper.

These output files will have the *.dat designation.
The program will ask you where to save these *.dat files.

EXAMPLE FILE:

We have provided a data set from Romijn et al, PRB 26 3648 (1982). This is self-field critical current data for a rectangular Aluminium sample. This is a thin film rectangular sample. It is a type I s-wave superconductor. Load up the file and choose these options for fitting as well as the single band option. Also you need to input the width, thickness and kappa values.

Make sure you increase the number of fitting iterations from 1. If the fit is run until it converges you should obtain parameters from the fit around these values: Tc ~ 1.2 K, Delta0 ~ 0.18 meV, dC/C ~ 1.5, lambda0 ~ 55 nm.
