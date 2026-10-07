# Pattern decomposition using Le Bail method

## Pattern decomposition using Le Bail method
### Basics
Pattern decomposition aims at obtaining reflection intensities I(hkl) from powder diffraction data. The method is pretty similar to Rietveld refinement, in the sense that it tries to mimic an experimental powder diffraction profile by refining certain parameters of a model (function). However, in contrast to Rietveld refinement, pattern decomposition does not require the availability of full crystal structure data. Instead, it just needs unit cell parameters and maybe the space group (if available) for all phases that are present in the sample. Hence, you can also apply it in cases where no atomic coordinates are available.
This is possible because in pattern decomposition using the Le Bail method the reflection (or peak) intensities I(hkl) are not calculated from the given crystal structure data, but are obtained directly from an iterative partitioning of the experimental intensities according to the intensities calculated from the model.
There are basically three purposes for pattern decomposition:
- Obtain reflection intensities I(hkl), e.g. for crystal structure solution
- Determine the lowest possible R-factor (or chi2 value) that can be expected from a corresponding Rietveld refinement.The background is that in pattern decomposition the I(hkl) values are not constrained by the atomic coordinates. Instead, they can be freely adapted to the experimental peak intensities, in order to mimic them as closely as possible, thus leading to the best possible agreement between calculated and experimental diffraction pattern (lowest possible R-factor).
- Verify the space group selection, by comparing the results of two (or even more) calculations in different space groups
### Pattern decomposition in Match! using FullProf
For pattern decomposition, Match! uses the well-known Le Bail method, as it is implemented in the Rietveld program
FullProf
(J. Rodriguez-Carvajal, Physica B 192, 55 (1993)) in its so-called "Profile matching" mode. You do not have to interact with FullProf directly though; instead, you can use the
Match! user interface to define ("turn-on") the parameters, setup the calculations and evaluate the results.
### Prerequisites
Before you start your actual pattern decomposition calculations in Match!, please check the following requirements:
- Path to FullProf must be defined: Normally, Match! determines the path to the FullProf software on your computer automatically. If this is not possible, you will be asked if you would like to manually select this path. Finally, if this is not successful (e.g. if you pressed the "Cancel" button), you
will be asked to download
and install FullProf from the Crystal Impact website.
- Experimental diffraction pattern (profile) must have been imported.
- The qualitative analysis must have been completed, i.e. the match list must contain a list of all phases in the sample. All experimental peaks should have been assigned either to known phases or to the compound you would like to investigate by pattern decomposition.
- All entries in the match list must at least contain unit cell parameters and preferably space group. If the unit cell is still unknown for the compound under investigation, you have to run indexing first.
### Setting up and running pattern decomposition calculations
Once you have checked the prerequisites mentioned above, you are ready to setup and run pattern decomposition calculations. This is achieved by running the menu command "Tools / Pattern decomposition (Le Bail fit) using
FullProf�" or by pressing the corresponding button  in the toolbar. This will open the so-called "Parameter Turn-On" dialog (please follow this link for more instructions).
We recommend to refine the following parameters in subsequent refinement calculations (although you can use your own scheme, of course!):
-  refinement
No parameters selected for refinement (optimize just the I(hkl) values iteratively)
-  refinement
Shift on 2theta axis (zero point)
-  refinement
Shift on 2theta axis (zero point)
- Unit cell parameters
-  refinement
Shift on 2theta axis (zero point)
- Unit cell parameters
- U, V, W (Caglioti half-width parameters, maybe one after the other, starting with W)
-  refinement
Shift on 2theta axis (zero point)
- Unit cell parameters
- U, V, W (Caglioti half-width parameters)
- Profile shape parameters
-  refinement
Shift on 2theta axis (zero point)
- Unit cell parameters
- U, V, W (Caglioti half-width parameters)
- Profile shape parameters
- Asymmetry parameters Asym1, Asym2 (on the "Advanced" or "Experts" tab)
-  refinement
Shift on 2theta axis (zero point)
- Unit cell parameters
- U, V, W (Caglioti half-width parameters)
- Profile shape parameters
- Asymmetry parameters Asym1, Asym2
- Background parameters
Just like in Rietveld refinement, try to reduce the R-factor (chi2 value) as much as possible, while selecting only reasonable parameters for refinement.
### Results viewing and exporting
When the FullProf refinement calculation has finished, there are several facilities to view and evaluate the results of a refinement calculation:
First of all, the convergence, the weighted average Bragg R-factor, the final reduced chi2
and the
FullProf comment are displayed at the top of the Refine tab on the upper right-hand side
of the screen. Below, there are several buttons using which more detailed information is available:
- The View results button displays a table in which you can compare the parameter values
before and after the refinement calculation.
- If FullProf has detected correlated parameters during the calculation, you can
display them by pressing the �Display correlated parameters� button below.
- To the right, you can display the original FullProf files resulting from the calculation,
simply by selecting the file you would like to view in the Display result file combobox.
A window will open where you can view and maybe copy the contents of the selected file.
This facility is especially useful if the result of a calculation is not to your satisfaction
and you would like to view more details of the calculation.
- Finally, you can copy the original FullProf result files to a user-defined directory by pressing
the Save resulting files button. Note that if you do not save the FullProf files using
this button, they will be deleted when you open or create a new Match! document!
If the peak data of a match list entry result from a pattern decomposition calculation, this is indicated by a "[PD]" in the legend of the pattern graphics.
In order to export the resulting I(hkl) data, please run the menu command "File / Export / Reflection data I(hkl) or |F(hkl)|".
### Quantitative analysis
Once a pure Rietveld refinement calculation using FullProf has converged, the amounts of the individual phases
resulting from the calculation are copied back into the match list, so that the results of the
quantitative analysis are available there. Hence, the values in the "Quant. (%)" column in the
match list may change when a Rietveld/FullProf calculation has been run successfully (i.e. convergence
was reached).
However, if a mixed (Rietveld and pattern decomposition) or a pure pattern decomposition refinement has been performed, the entries where pattern decomposition has been applied are not included in the quantitative analysis (their amounts will be displayed as zero (0.0)). In these cases it is possible to perform a full quantitative analysis if the amounts of these phases are known from other sources: You can enter the known amount(s) manually in the match list, by double-clicking the corresponding "missing" amount value "0.0" in the match list, entering the "true" amount, and finally pressing <Return>. Match! will re-scale the amounts of the remaining phases accordingly.
### References
More information about pattern decomposition and its history can be found e.g. here:
- A. Le Bail, Whole powder pattern decomposition methods and applications: A retrospection, Powder Diffraction, Volume 20, Issue 4, December 2005, pp. 316 - 326; DOI: https://doi.org/10.1154/1.2135315
- Advanced Certificate in Powder Diffraction on the Web, School of Crystallography, Birkbeck College, University of London, 1997-2006