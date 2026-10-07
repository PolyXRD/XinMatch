# Import Entries from ICSD/Retrieve

## ICSD/Retrieve Import
If you still have a valid licence for an old ICSD/Retrieve version released between 1993 and 2002, you can create a powerful
reference database without additional costs, simply by importing the crystal structure
data from the ICSD. During the import procedure, the corresponding
powder diffraction patterns (as well as the I/Ic values required for the
semi-quantitative analysis and the
density) are calculated automatically.
In order to do so, please click on the "Import" button at the top of the User
Database Manager. A dialog will be displayed in which you can select if you would like to import entry data either
from cif (crystallographic information files), from some other
Match! user database file (*.mtu), or from the ICSD.
Please mark the "ICSD/Retrieve" option, then press "OK".
You now have to give the directory in which the ICSD/Retrieve database (to be exact:
the file "ICSD.NEW") is stored. A "File Open" dialog will be displayed in which you have to select the file "ICSD.NEW".
Normally, this file is located in the "INDEX" subdirectory of your ICSD/Retrieve program
directory. Once you have found and marked the file "ICSD.NEW", please press "Open".
A new dialog is displayed in which you have to confirm that you have a valid licence for
the ICSD/Retrieve version you are about to import.
If you have confirmed that you have a valid licence, a new dialog is displayed in which
you can adjust some settings concerning the calculation of diffraction patterns: the radiation
type (X-rays or neutron), the maximum 2theta angle (optionally=160º for face-centered
cubic structures), and the maximum number of peaks
that shall be included in the database to be created.
Note that this is a convenient method to create a reference database for neutron diffraction data!
When you have made your selections (if any), please press "OK". That's it! The import of
the entries from the selected ICSD/Retrieve database will now begin.
The progress will be displayed in a small window. Depending both on the number of entries in the ICSD/Retrieve database as well as the
processing speed of your PC, the import procedure may take several hours or even longer!
When the import has finished, the new entries will be automatically added to the current user
database, so they will appear in the Entry list a few seconds later. Any errors that might
have occured during the import will be displayed in your text editor.
Once the import has finished, please don't forget to press the "Save" button at the top
of the user database manager, in order to save the entries imported from the ICSD/Retrieve to a so-called
"user database file" (file extension *.mtu). As has already been mentioned, this user
database file can then be selected
in the "Create Reference Database" dialog to create a new "ICSD/Retrieve" reference database,
probably in combination with the "COD" reference database that is shipped along
with Match!.
### Copyright Issues
Please make sure that you have a valid licence for the ICSD/Retrieve version you would like to import!
If you are in doubt whether your licence is still valid, please contact FIZ Karlsruhe (Germany) (e-mail:
crysdata@fiz-karlsruhe.de).
You are allowed to forward/copy the user database file you have created from ICSD/Retrieve to any person that
has the right to use your ICSD/Retrieve licence, but not to other people. Crystal Impact shall not be liable for any copyright
violations of Match! users!
Please note:
- For neutron radiation, absorption is neglected in the I/Ic-value calculation.
- If Match! is not able to identify the space group beyond all doubt, a corresponding message will be displayed or
added to the error/warnings report. If the space group could not be identified at all, you should first
select the corresponding space group on the "Crystal
structure" tabsheet, calculate the diffraction pattern afterwards on the "Diffraction pattern" tabsheet and
finally save the entry. You can get additional information about the
space group currently selected in the combobox by placing the mouse cursor over the combobox.