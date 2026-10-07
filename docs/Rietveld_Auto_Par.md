# Configuring Automatic Refinement Calculations

## Configuring Automatic Refinement Calculations
Using the "Define Parameter Sequence for Automatic Refinement" dialog you can select which
parameters shall be refined in which order (cycle) during the automatic refinement procedure for Rietveld refinement or pattern decomposition calculations. You can define parameters for a maximum of 10 subsequent refinement cycles.
The dialog can be opened by pressing the "Configure..." button at the top of the
"Parameter Turn-On" dialog. In the top row of the dialog window, the dialog elements
for the control of the current parameter sequence are placed:
New: By pressing this button, the parameter sets for the 10 refinement cycles are erased, so that you
can start from scratch to create a new parameter sequence. You will be asked if you would really
like to do so after pressing the New button.
In the Preset combo box, you can access all parameter sequence sets that you have already created.
Simply click on the combo box and select the name of the parameter set you would like to open.
The "Standard" parameter set is always present in this combo box. This set contains the default/factory
automatic refinement procedure; it cannot be deleted.
By pressing the Save button you can store the current parameter sequence set using a user-defined name,
so that you can recall this setting later on in the "Preset" combo boxes both of the "Define Parameter Sequence..."
as well as the Parameter Turn-On" dialog. After pressing the button,
you will be asked to enter a reasonable name for the parameter set. Once you have pressed "OK", the new parameter sequence preset will
be added to the "Preset" combo box.
If you press the Default button, the current parameter sequence set will be selected as the new default
parameter sequence for automatic refinement calculations. The current parameter sequence must have been saved
in advance for this purpose; otherwise a corresponding hint/message will be displayed.
Pressing the Delete button removes the current set from the "Preset" list. Hence, if you would like to remove
a parameter set, you have to select it from the "Preset" combo box first, and then press the "Delete" button.
Please note: The parameter set called "Standard" contains the factory parameter set; it cannot be deleted.
In the 10 boxes (parameter lists) (labeled "#1", "#2" etc.) below, you can select which parameters shall be varied separately for each refinement cycle.
Match! runs the refinement calculations in the order as they are indicated at the top of the boxes, i.e. it starts with
"Refinement #1", then runs "Refinement #2" etc. In each refinement cycle, all parameters that are present in the corresponding
list (box) will be varied.
For every refinement cycle parameter box, a set of associated dialog elements is available:
The "->" (arrow right) button at the top right of each parameter box copies the parameters of the corresponding box into the next box.
This may be useful if you would like to add more and more parameters in each subsequent cycle, which is a common strategy in Rietveld refinement (or pattern decomposition).
In order to Add a new parameter to a parameter box, simply select it from the combo
box at the bottom of the corresponding parameter list. It will instantly be added to the list.
By pressing the  button at the bottom right of each
parameter box you can delete the marked
parameters from the corresponding parameter box. If no parameter is currently marked, all parameters
will be removed from the box.
Once you have finished editing the refinement parameter sets, please press the Close button
to return to the "Parameter Turn-On" dialog.