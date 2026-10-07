# Import Entries from CIF file(s)

## Import Entries from CIF file(s)
The most convenient way to add entries to a user database
is probably the import of crystal structure data from cif-files, whereupon the corresponding
powder diffraction patterns (as well as the I/Ic values required for the
semi-quantitative analysis and the
density) are calculated automatically.
In order to do so, please click on the "Import" button at the top of the User
Database Manager. A dialog will be displayed in which you can select if you would like to import
entry data either from cif (crystallographic information files), from some other
Match! user database file (*.mtu), or from ICSD/Retrieve.
Please mark the "cif" option, then press "OK". A new dialog is displayed in which
you have to select the directory from which you would like to import
cif-files. Please mark the corresponding directory, then press "OK".
Another dialog will open, presenting a list of all cif-files present in the selected
directory (as well as all cif-files from all subdirectories if present). Here, you can
actually select the cif-files you would like to import. Please mark the file(s) you would
like to import, then press "OK".
Again, a new dialog is displayed in which you can select the origin (e.g. source database)
from which the cif-files has been taken, e.g. the COD, the AMCSD, or probably some
IUCr journal. This information
is used to add some reference data to the created/imported entry(s), as well as to create an
appropriate entry number.
Besides this, you can select if you would like to import crystal structure data from
inorganic and/or organic compounds, by marking the corresponding checkboxes. Inorganic
compounds are defined by the fact that no bonds between carbon and hydrogen atoms are present.
Match! assumes C-H-bonds to be present if corresponding interatomic distances of 0.6 up to 1.3
Angstroms are found.
In addition, you can adjust some settings concerning the calculation of diffraction patterns: the radiation
type (X-rays or neutron), the maximum 2theta angle (optionally=160º for face-centered
cubic structures), and the maximum number of peaks
that shall be included in the database to be created.
Note that this is a convenient method to create a reference database for neutron diffraction data!
Please mark your selection, then press "OK".
That's it! Everything else will be handled automatically: A new entry will be created; the
data from the cif-file will be imported into the corresponding data fields, and the
diffraction pattern, the density and the I/Ic value will be
calculated from the imported crystal structure data. The new entry will be automatically added to the user
database, so it will appear in the entry list a few seconds later (of course depending on the size of
the unit cell...).
It is of course possible to select more than a single cif-file
for being imported at a time, by keeping the <Shift> or <Ctrl> button pressed while you
click on the individual file names. In this case, all selected files will be imported automatically one after the
other. If you import more than a single cif-file at a time, a report of
warnings and errors is displayed when the last file has been imported, compared to the import
of a single cif-file in which case any warnings and errors are reported
directly.
The "import of multiple cif-files" functionality is rather powerful:
It is frequently used by Crystal Impact to create or update the COD reference database
from cif-files, containing hundreds of thousand entries.
### Copyright Issues
With Match!, it is perfectly possible to use cif-files from various sources (e.g.
downloaded from the internet) as sources for creating an own reference pattern database.
However, please note that before doing so, you have to check if this does not violate
the copyright of the original data! Crystal Impact shall not be liable for any copyright
violations of Match! users!
If you know about potential sources of reference data that might be
interesting for other users, please contact Crystal Impact!
Please note:
- For neutron radiation, absorption is neglected in the I/Ic-value calculation.
- If Match! is not able to identify the space group beyond all doubt, a corresponding message will be displayed or
added to the error/warnings report. If the space group could not be identified at all, you should first
select the corresponding space group on the "Crystal
structure" tabsheet, calculate the diffraction pattern afterwards on the "Diffraction pattern" tabsheet and
finally save the entry. You can get additional information about the
space group currently selected in the combobox by placing the mouse cursor over the combobox.
- If the cif-file contains more than a single "data_" section, a new entry will be created for each single section.
There is only one exception to this rule: If the section title is "data_global", the information in this
section may be copied into the remaining sections of the file and not imported into a new entry itself, depending
on the corresponding option at the bottom of the "Select Source Database" dialog.
- The normal "File-Open" dialog cannot be used for the selection of the cif-files to be imported due to
a well-known Windows bug when a large number of files is selected.