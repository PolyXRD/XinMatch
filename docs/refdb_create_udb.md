# Create Deference Database From User Data

## Create Reference Database From User Data
In addition (or as an alternative) to using the "classical" reference databases like ICDD PDF or COD,
it is also possible to use own diffraction patterns
in phase analysis. Before you can do so, you have to store your corresponding
diffraction patterns and/or crystal structure data sets in a so-called
"user database" file (file extension *.mtu), e.g. using the so-called "User Database
Manager" dialog. If you have not already done so, please follow these instructions
first, in order to create the mtu-file from your data. Afterwards, please return to this point and continue reading.
First of all, please make sure to display the  Reference Database Library dialog,
then click on the "Create" button at its bottom, in order to display the "Create Reference Database" dialog.
In order to use an existing user database file (*.mtu) as reference
database, you first have to
tell Match! that you would like to apply a user database, by marking the
corresponding option in the middle of the "Create Reference Database" dialog.
Afterwards, you have to select the location of the *.mtu file, by pressing the
button "Select user database file (*.mtu)" to the right of the corresponding
input line "Location:".
A "File Open" dialog will be displayed in which you have to select the mtu-file
in which your user data are stored. Afterwards, press "Open" to
select the file/directory and return to the "Create Reference Database" dialog. The location
of the mtu-file will now be displayed in the corresponding input box.
If you like, you can change the name of the new reference database at the bottom of the
dialog (deactivate the corresponding "Automatic" checkbox first!), and/or change
the location (directory) in which the index files for the new reference database shall be stored.
Normally, Match! will automatically create a suitable name and select an appropriate
directory.
In case you have administrator privileges, you can also select if you would like to make
the new reference database available to all users (or only to you), and if you would like
to make it the default Match! reference database for new users on your PC.
Please note that on Windows it
is not sufficient to run Match! from an administrator account; you have to explicitly use the command "Run as
administrator" (which is available e.g. in the context-menu (click right mouse button))
in order to enable the two options "Create for all users" and
"Select as default for all users without own selection"!
On Linux, you have to use "su" or "sudo" in order to run Match! with "root" privileges and
enable these two options.
Once you have made your selections, press the "OK" button at the bottom to start
the creation of the index files. A small window will display the progress of the indexation.
Depending on the amount of data which have to be read and sorted, the creation of index files
may be a rather time consuming process. The procedure may take between a few minutes to an hour
or even more, depending especially on the drive access and processing speed of your computer.
When the indexation has finished, a corresponding message will be displayed.
Afterwards, the new reference database will appear in the Reference
Database Library.
If the new reference database is the only one available in the Reference Database
Library, it is selected for being used automatically. Otherwise, you have to
select
the new reference database manually.
Please note:
- You can open the "User Database Manager" directly from
the "Create Reference Database" dialog by pressing the "Create/modify user database..."
button. Alternatively, the "User Database Manager" can also be invoked from the "Database"
menu.
-
It is perfectly possible to create a combined reference database based on e.g. the COD database AND/OR your own (user) reference data, simply by marking
the corresponding options in the "Create Reference Database" dialog.
- If you would like to use both the ICSD/Retrieve database and your own data (user database) as reference database, you first have
to combine the mtu-files created from the ICSD/Retrieve and your
own user data into a single new mtu-file. Afterwards, you can select this combined mtu-file as "User database" in the
"Create Reference Database" dialog as usual.