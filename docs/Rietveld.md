# Rietveld Refinement

## Rietveld Refinement
### Basics
Before we start: An excellent, quick introduction to Rietveld refinement suitable even for absolute beginners is the very clearly structured
document Lesson 5: Rietveld Refinement
of Nicola D"belin's Lecture Handouts.
Rietveld refinement is a tool that tries to model a full powder diffraction profile based on
crystal structure data, specimen and instrument effects. This is achieved by introducing
certain functions that describe typical phenomena in powder diffraction experiments, like
2theta errors or peak broadening, and by fitting the corresponding parameters afterwards.
The parameters are
varied using a least-squares procedure, in order to minimize the difference between the calculated
and the experimental powder diffraction pattern.
The Rietveld method was first introduced by Hugo Rietveld in 1967 and 1969. Details of the method are available in the literature:
- H.M. Rietveld, Acta Cryst. 22, 151-2 (1967).
- H.M. Rietveld, J. Appl. Cryst. 2, 65-71 (1969).
- R.A. Young (ed.), "The Rietveld Method", International Union of Crystallography, Oxford University Press, New York 1993.
One of the key issues of Rietveld refinement is that the method is rather sensitive to problems and
errors in the model, resulting in non-convergence and other issues. Hence, it has become a common
agreement for many scientists that a successful phase analysis should be proven by a successful
Rietveld refinement converging at low R- and chi2-factors.
In addition, running Rietveld refinements on your diffraction pattern will give you an opportunity to think and learn more about your sample, your experiment
and your model. Please take a look at the chapter Some Hints, Tips and Tricks for
Rietveld Refinement. Here we give you some advice which important facts you should always keep in
mind when running Rietveld refinement calculations, as well as some tips what you can do in case of problems.
### Rietveld refinement in Match! using FullProf
Today a variety of excellent programs for Rietveld refinement are available, so there is little need to invent
the wheel again and again. Match! uses the well-known Rietveld program
FullProf
(J. Rodriguez-Carvajal, Physica B 192, 55 (1993)) to actually perform the calculations.
You do not have to interact with FullProf directly though; instead, you can use the
Match! user interface to define ("turn-on") the parameters, setup the calculations and evaluate the results.
### Defining the Match!/FullProf connection/path
When you run Match! for the first time, the program tries to automatically determine
the path to the FullProf software. If this is not possible, you will be asked if you would like to manually
select this path. Finally, if this is not successful (e.g. if you pressed the "Cancel" button), you
will be asked if you would like to download
and install FullProf from the Crystal Impact web site.
This "checking for FullProf" procedure is carried out only once. If there is no valid path to FullProf available
at its end (e.g. because you have pressed the "Cancel" buttons), you won"t be asked again until you
try to run a Rietveld refinement calculation. However, you can
download and install FullProf
manually later on by selecting the "FullProf download" command from the "Tools" menu. As an alternative, you can
define or modify the path to FullProf any time on the "Rietveld" tab
of the "Options" window (which can be opened e.g. from the "Options" menu).
### Setting up and running Rietveld refinement calculations
Once you have defined the path to FullProf, you are ready to setup and run Rietveld refinement calculations
from within Match!. This is
achieved by opening the so-called "Parameter Turn-On" dialog.
### Results viewing
When the FullProf calculation has finished there are several facilities to view and evaluate the results of
a refinement calculation:
First of all, the convergence, the weighted average Bragg R-factor, the final reduced chi2
and the
FullProf comment are displayed at the top of the "FP Rietveld" tab on the upper right-hand side
of the screen. Below, there are several buttons using which more detailed information is available:
- The View results button displays a table in which you can compare the parameter values
before and after the refinement calculation.
- If FullProf has detected correlated parameters during the calculation, you can
display them by pressing the "Display correlated parameters" button below.
- To the right, you can display the original FullProf files resulting from the calculation,
simply by selecting the file you would like to view in the Display result file combobox.
A window will open where you can view and maybe copy the contents of the selected file.
This facility is especially useful if the result of a calculation is not to your satisfaction
and you would like to view more details of the calculation.
- Finally, you can copy the original FullProf result files to a user-defined directory by pressing
the Save resulting files button. Note that if you do not save the FullProf files using
this button, they will be deleted when you open or create a new Match! document!
### Quantitative analysis
Rietveld refinement can also be used to obtain the amounts of the microcrystalline phases in your sample, i.e. to perform a quantitative analysis.
To do so, you first have to finish the qualitative analysis of the phases in your sample. Afterwards, simply run the "Rietveld (FullProf)" command in the "Quantify" menu (or press the combination <Ctrl+Alt+R> on your keyboard). Match! will run an automatic Rietveld refinement calculation using the parameter sequence defined in the currently selected preset for automatic Rietveld refinement.
If the refinement was successful, the amounts in the match list will be replaced by the ones obtained from the Rietveld refinement, and the pie chart graphics will be displayed. The corresponding information will also be included in the report.
In general, each time a Rietveld refinement calculation using FullProf has converged, the amounts of the individual phases
resulting from the calculation are copied back into the match list column "Quant. (%)", so that the results of the
quantitative Rietveld analysis are available there.