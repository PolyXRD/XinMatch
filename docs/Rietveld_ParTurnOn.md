# Running FullProf calculations using the "Parameter Turn-On" dialog

## Running FullProf calculations using the "Parameter Turn-On" dialog
The so-called "Parameter Turn-On" dialog is used to setup and run Rietveld refinement and pattern decomposition calculations.
It can be opened either by selecting the "Rietveld (FullProf)..." or "Pattern decomposition" commands
in the "Tools" menu, by pressing the corresponding buttons   or  in the center of the toolbar,
by pressing  �Ctrl + Shift + R� on your keyboard, or
by pressing the "Run new calculation" on the "Rietveld"-tab on the right-hand side of the Match! window.
### Prerequisites
Before you use the Parameter Turn-On dialog, you first
have to perform the normal qualitative phase analysis procedure, i.e. import (raw/profile!) diffraction data,
find the peaks, run a search-match and select one or
more �matching phases�.
In case of Rietveld refinement, Match! will check
if any of the entries you have selected as �matching phases� does not contain a full crystal
structure data set (e.g. if the atomic coordinates are missing). In this case you will be prompted
to either import suitable crystal structure data from cif-files, or to switch over to pattern decomposition for this phase.
The background is that it is not possible to run Rietveld refinements without complete structural models.
Once complete crystal structure data sets are available for all matching phases, the �Parameter Turn-On�
dialog will be displayed.
Please note:
- You can eliminate all entries that do not contain a full crystal structure description from
the candidate list using the menu command
Entries/Delete incomplete entries.
- Match! will also switch to the �Rietveld� tab on the upper right-hand side
of the Match! window automatically where the results and viewing options will be available
after the refinement calculation.
### Concept/layout of the Parameter Turn-On dialog
In order to introduce users that are new to Rietveld refinement or pattern decomposition, we have
implemented four different approaches to define ("turn-on") the options and parameters for
the calculation. The method that is easiest to use ("Automatic Refinement") is
available simply by marking the corresponding checkbox at the top of the Parameter Turn-On
dialog, while the three remaining facilities "Beginner", "Advanced" and "Expert" are present
as tabs in the main part of the dialog. The parameters on the three tabs are linked to each
other, so that you can start turning on parameters e.g. on the "Beginner" tab and finish as an "Expert".
We will now discuss the four approaches of using the �Parameter Turn-On� dialog in more detail:
#### Automatic Refinement
The "normal" way to setup a Rietveld (or pattern decomposition) refinement calculation is to activate the �Automatic
refinement� option at the top of the �Parameter Turn-On�-dialog. If this option is active, all
remaining options are disabled. Afterwards, you can run the automatic refinement calculation by
pressing the �Run FullProf� button on the lower left-hand side. The calculation(s) will be run
automatically; at the end, the result will be displayed on the �Rietveld�-tab on the upper
right-hand side of the Match! window.
For the automatic refinement it is possible to apply user-defined refinement sequences
other than the factory one. In order to do so, please press the
Configure... button at the top of the "Parameter Turn-On" dialog. This will open the
Define Parameter Sequence for Automatic Refinement dialog
in which you can select which
parameters shall be refined in which order (cycle) during the automatic refinement procedure.
The user-defined refinement sequences can be stored in this dialog and recalled later on in the Parameter Turn-On
dialog using the Preset combo box at the top.
By default, either the "Standard" (factory) parameter sequence set or the one that has been selected as "default"
in the Define Parameter Sequence for Automatic Rietveld Refinement dialog
is run during automatic refinement. If you would like to run a different user-defined parameter set,
please select it from the Preset combo box.
The automatic Rietveld refinement (here with the purpose of quantitative phase analysis) may also be run using the "Rietveld (FullProf)" command in the "Quantify" menu.
#### Beginner
The next step for learning how to do Rietveld refinement (or pattern decomposition) is to deactivate the �Automatic
refinement� option, and to use the options (checkboxes) on the �Beginner� tab. On this tab, a
selection of Rietveld parameters is available, along with a suggested order in which they shall
be turned on in successive calculations.
For example, in the first calculation only the scale factors and specimen displacement parameters
are recommended for refinement. If this first refinement calculation is successful, the unit cell
and first background parameters can be activated in addition to the first parameters, and another
refinement calculation is performed. If this is successful, the W and atomic coordinate parameters
are added etc.
In fact, this is just the order in which the calculations are carried out during the automatic
refinement. However, you now have more control and can stop at certain points or repeat steps
if you like. This order is taken from the excellent book "The Rietveld Method" edited by R. A. Young (1993).
Please note:: The refinement of the scale factor is not available for entries for which pattern decomposition is performed! The background is that the Le Bail method includes an iterative partitioning of the experimental intensities according to the intensities calculated from the model, in order to derive the reflection (peak) intensities I(hkl) automatically.
#### Advanced
Once you are familiar with the principal procedure and main parameters, you are ready for more
detailed options and parameters. Hence, we have introduced the �Advanced� tab, on
which a reasonable amount of parameters is grouped according to their effect: �Peak positions�,
�Peak intensities� and �Profile shape�.
You can e.g. address specific problems e.g. concerning the positions of the peaks by marking
one or the other parameter on the �Peak positions� tab for refinement.
Another feature on the �Advanced� tab (that is also available on the �Expert� tab) is the
possibility to define constraints for a certain parameter. In order to do so please press
the �...� button to the right of the corresponding parameter (e.g. �Shift on 2theta-axis�).
A new dialog window will open (Fig. 18) in which you cannot only modify the parameter value
or mark the parameter for being optimized, but also define contraints by entering the limiting
numerical values in the �Minimum value� and/or �Maximum value� fields.
At this stage you should also note the table of �Active parameters� on the right-hand
side of the Parameter Turn-On dialog: Here you can get an overview over the parameters that
are currently marked for being varied in the next refinement calculation. Please note that
the parameter names given in the left-most column are the original full parameter identifiers
used in FullProf. If you double-click on a certain line of the table, the parameter modification
dialog just mentioned will be opened, so that you can modify parameter settings directly without
having to search for the corresponding �...� button or tab.
#### Expert
This is the most comprehensive but also the most demanding option for setting up the
refinement calculation parameters. All FullProf parameters that are currently supported by Match! are
available here. You can adjust global settings like �Zero� or �Lambda� on the �Global� tab,
as well as select or modify parameters for individual phases (e.g. unit cell parameters or
atomic coordinates). For each phase of the Match list, a separate tab is available. All
parameters belonging to a certain phase are distributed to subtabs like �Quant.�, �Profile�
or �Crystal structure�.
#### Pattern calculation
In case of Rietveld refinement, if you do not mark any of the �vary� checkboxes in the "Parameter Turn-On" dialog (i.e. if the table of �Active parameters� on the right-hand side is empty), you can instruct FullProf to calculate the
powder diffraction pattern (based on the current settings and parameter values) simply by
pressing the �Run FullProf� button. When the calculation has finished, you can e.g. export
the calculated pattern using the menu command File/Export/Profile data (Rietveld).
In case of pattern decomposition, if you do not mark any of the �vary� checkboxes in the "Parameter Turn-On" dialog, this will instruct FullProf to just refine the I(hkl) values.
### Running the calculation
When you have selected all parameters you would like to refine, the Rietveld refinement
calculation is started by pressing the Run FullProf button at the bottom left of the
Parameter Turn-On dialog. When the calculation has finished, the results (e.g. R-factor,
chi2, FullProf comment) will be displayed in the �Refine� tab to the right of the Match!
window. You will also be informed if the calculation was successful (reached convergence) or not.
### Buttons in �Parameter Turn-On� dialog
There are a couple of buttons located at the bottom of the �Parameter Turn-On�-dialog:
- Run FullProf: Once you have selected the parameters you would like to optimize,
the Rietveld refinement calculation is started by pressing this button.
- Clear: By pressing this button you can turn off all parameters, i.e. uncheck the
�vary� checkboxes of all parameters. This will also erase the �Active parameters� table.
- Reset: You can reset all parameters to their original values (the ones before the
first refinement) by pressing this button.
- Export: Match! offers a large variety of FullProf variables and options. Nevertheless,
it may be useful in special situations to use FullProf directly (without Match!). For this
purpose you can export the input files required (*.pcr, *.dat and *.bac) as a starting
point for the FullProf calculation by pressing this button. You will be asked to provide
the path where the FullProf input files shall be stored. Afterwards, the files will
be created in the specified directory.