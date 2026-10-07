# Some Hints, Tips and Tricks for Rietveld Refinement

## Some Hints, Tips and Tricks for Rietveld Refinement
With Match! we have tried to get you into Rietveld refinement as gently as possible by offering
different approaches with increasing difficulty level, from the "Automatic refinement" option
to the "Expert" facilities. Nevertheless, Rietveld refinement is a complex subject that can
require quite some experience. We would like to provide you with some hints and facts you
should keep in mind in order to avoid running into problems at an early stage:
### General remarks
First of all, Rietveld refinement uses a local optimization method (least-squares refinement).
This means that the method will try to reach the next minimum available from the starting point.
You cannot expect from the method to investigate large parts of the cost function hypersurface
in order to find the global minimum!
In practice this means that your starting model (e.g. crystal structure data, scaling factors,
profile parameter values etc.) should be as close to the final model as possible, in order
to reach convergence. You should avoid to give the system any "room" for getting stuck in
a false minimum or being blown up by a singular matrix.
### Strategy for refinement
A reasonable strategy for performing a Rietveld refinement is not to vary all parameters
straight away from the beginning, but to introduce them one after the other in a certain
reasonable order. For example, there is little sense in trying to refine your atomic
coordinates as long as the scaling factors of the phases are far off their arbitrary values!
On the "Beginner" tab of the Parameter Turn-On dialog
you can see "our" suggestion for the order of parameter introduction into the calculation
(the strategy has been adapted from the suggestion described in R. A. Young (ed.),
"The Rietveld Method", International Union of Crystallography, Oxford University Press,
New York 1993, p. 32-36.):
You start by refining the intensity scale factors of the phases and maybe the specimen displacement parameter.
Once you have run the corresponding Rietveld refinement and reached convergence, you can add
the unit cell parameters and the first background parameter, and perform the second Rietveld refinement etc.
### Check of refinement result
It is generally always advisable to take a look at the pattern graphics and compare
the profile resulting from the Rietveld refinement (which has light-green color by default)
to the experimental profile. Quite a lot of problems can be identified and/or avoided by doing so:
- Wrong scaling factor(s)
- Incorrect background
- Wrong or unidentified phase(s)
- Missing or surplus peaks
- 2theta error (e.g. zero point and/or specimen displacement)
- One or more unit cell parameters do not match
- Profile shape is not described correctly by the profile function applied, e.g. due to asymmetry
### Preferred orientation
If you observe that the intensities of one (or more) peaks of a certain phase are way off their expected values, this may be an indication that the crystallites in your sample are not oriented completely at random, but that there is a certain "accumulation" of a certain crystallite orientation with regard to the incident beam (a so-called "preferred orientation", also called "texture"). This may happen for example if your crystallites have the shape of needles or plates, so that they prefer to be oriented along the axis of a capillary or the surface of a flat plate sample.
In Rietveld refinement using FullProf, this can be taken into account (at least to a certain degree) by refining the parameters of a corresponding preferred orientation function ("exponential" or "March" function). Please follow these instructions in order to do so:
- Run Rietveld refinement of at least the scaling factors.
- Display the contents of the result file "fpcalc.hkl", by selecting this file in the "Display result file" drop-down box on the "Rietveld" tab and pressing the "Go!" button.
- Examine the list of intensities and locate the preferred orientation, indicated by a series of harmonic reflections with Iobs systematically quite larger than Icalc. If you cannot locate such a clear preferred orientation, you may try some possibilities like 001, 100, 010, 110, etc.
- Press "Run new calculation" (open the "Rietveld Parameter Turn-On"-dialog), then enter the preferred orientation vector just mentioned on the "Stress/strain/pref. orientation" sub-tab of the corresponding phase's page on the "Expert" tab.
- On the same tab, mark "Pref1" for refinement.
- Press "Run FullProf" in order to run the refinement.
- If you have achieved a significant drop of the R-factor, you may have found the preferred orientation. If not (or if the refinement calculation did not even converge at all), you should try another preferred orientation vector as described above.
- By default, Match!/FullProf uses the "Exponential function" for preferred orientation. You could also try the "Modified March's function", by changing the corresponding value of "Nor" on the "Global" sub-tab of the "Expert" tab.
### Convergence problems
If a calculation does not converge, you should go back (run "Edit / Undo") and try to find out which parameter
actually causes the problem. Maybe you can keep it fixed or introduce some constraints for it?
A common source for convergence problems are the background parameters:
While the first background parameter (FullProf: "BACK1") is still pretty "stable", refining the remaining background parameters (BACK2-BACK4) can be quite demanding. Doing so may easily result in an increased probability for convergence issues and false minima. This happens especially if other parameters are refined in parallel!
We recommend to be careful with these parameters and maybe not refine them at all during your ongoing refinement.
To avoid convergence issues with the background, we strongly recommend to check and maybe correct the background manually before diving into Rietveld refinement!
Once your refinement has converged with a pretty good agreement to the experimental profile, you could try to refine one or the other background parameter(s) again for "fine-tuning" it.
If you encounter convergence problems if only the scaling factor(s) are refined,
you should check the crystal structure descriptions of the match list entries, especially the space group,
setting and atomic coordinates. You could e.g. try to use a different entry describing the same phase,
or display and investigate the crystal structure in the "Diamond" software (only available on
Windows platforms).
Please note: If you got stuck with a non-converging Rietveld refinement calculation, please note that you have to go back (run "Undo") two times if you would like to return to the starting point of your previous (maybe still successful) refinement calculation! Otherwise you will just be returned to the result of your previous calculation.
### Refinement of atomic parameters
If your successive Rietveld refinement calculations do no longer converge after activating the
opion/parameter "Atomic coordinates of all phases" on the "Beginner" or "Advanced" tab of the
"Parameter Turn-On" dialog, you should try to activate the atomic coordinates of the atoms
individually one after the other instead. This can be achieved on the separate "Crystal structure"
tabs for each individual selected phase (tab "Expert").
### Correlated parameters
Another typical origin for convergence problems are parameter correlations. Correlated parameters
can e.g. prevent a refinement calculation from converging by switching between two states,
or by endless variations of one or more parameters that do not have any effect on the cost
function (R-factor, chi2). As has already been mentioned above, you can press the
"Display correlated parameters" button on the "FP Rietveld" tab to the right to display
the correlated parameters detected by FullProf.
### Original FullProf output checking
In addition, it might be helpful to take a look at the FullProf output files (e.g. fpcalc.out,
fpcalc.sum and fplog.log), especially at their lower part. Here you can normally locate the
origin of severe problems, like files that cannot be read or space group symbols that cannot be
identified. In order to display one of these files, simply select the corresponding file
from the "Display result file" combobox on the right-hand side of the "FP Rietveld" tab, and/or press "Go!".
Finally, if you really get stuck with your refinement using Match!, you might consider to move
on to using FullProf directly, so that you really have all possibilities this program package
offers. In order to do so, you can press the "Export" button in the
Parameter Turn-On dialog
to export FullProf files (pcr, dat and bac), so that you have a starting point for your
journey into the world of FullProf.