# The User Database

## The User Database
Phase analysis using powder diffraction data typically requires the availabilty of a
so-called "reference pattern database". In many cases, this is one of the PDF database products provided
by the ICDD. However, there are also
alternative sources of reference patterns, like the COD database delivered
with Match!, your own diffraction data, or even data from the literature.
While the COD reference database can be
downloaded "ready-to-use" from the Crystal Impact web page free-of-charge,  your own diffraction patterns (or
other suitable data) must first be imported into a so-called user database (file with extension "*.mtu").
Once you have created this user database file, you can select it in the "Create Reference Database" dialog.
User databases are typically created and maintained in the so-called User Database Manager
which can e.g. be opened using the "User database manager" command in the "Database" menu, or simply by pressing the corresponding
button  in the toolbar.
Once the User Database Manager is displayed, the way to create the mtu-file depends on the kind of data source you would like to use:
- Own diffraction patterns
- Crystal structure data (typically CIF-files)
- Data published in the literature
- Your colleague's user database file (*.mtu)
- ICSD/Retrieve database (released 1993-2002)
Once you have created your user database file (*.mtu), the procedure to use it
as reference database is pretty similar to the one using an old PDF-2 version:
First, you have to
tell Match! that you would like to apply a user database, by marking the
corresponding option in the middle of the Create Reference Database dialog.
Afterwards, you have to select the location of the *.mtu file, by pressing the button "Select user database file (*.mtu)"
to the right of the corresponding input line "Location:".
A "File Open" dialog will be displayed in which you have to select the mtu-file
in which your user data are stored. Afterwards, press "Open" to
select the file/directory and return to the "Create Reference Database" dialog. The location
of the mtu-file will now be displayed in the corresponding input box.
If you like, you can now change the name of the new reference database at the bottom of the
dialog (deactivate the corresponding "Automatic" checkbox first!), and/or change
the location (directory) in which the index files for the new reference database shall be stored.
Normally, Match! will automatically create a suitable name and select an appropriate directory.
In case you have administrator privileges, you can also select if you would like to make
the new reference database available to all users (or only to you), and if you would like
to make it the default Match! reference database for new users on your PC.
Once you have made your selections, press the "OK" button at the bottom to start
the creation of the index files. A small window will display the progress of the indexation.
The procedure will take a few minutes, depending especially on the number of entries as well as
the drive access and processing speed of your computer. When the indexation has
finished, a corresponding message will be displayed.
Afterwards, the new reference database will appear in the list of the
Reference Database Library, ready for being selected.
If the new reference database is the only one available in the Reference Database
Library, it is selected for being used automatically. Otherwise, you have to select
the new reference database manually: Simply mark (click) on the corresponding line
in the table, then press "Select". The new reference database will be marked as
selected, indicated by the ">>>" arrow on the left-hand side of the corresponding line.
You can now leave the Reference Database Library by pressing "Quit" and apply
the new reference database in phase analysis and database retrievals.
Please note::
- It is also possible to add (copy) entries from the current reference database to
a user database file: In order to do so, please mark one or more entries in the candidate list first, then run the command "Add entry(s) to user database" in
the "Database" or the "Entries" menu, or the corresponding command in the candidate list context menu.
- If you create a new reference database for an existing user database (mtu-file), the
selected mtu-file will be copied to the directory in which also the index files are stored.
Hence, it does not matter if you change or delete the original user database file
later on; this will not affect the reference database.
- You can select more than a single *.mtu-file in the
Create Reference Database or "File/Open" dialog, resp. In this
case, these mtu-files will be automatically united in a single mtu-file.
- For phase analysis as well as database retrieval, the ICDD PDF, the COD
and/or the user database are handled like a single large database. However, technically
the databases of course remain separate; your PDF and ICSD/Retrieve databases are not changed by Match!
in any way.