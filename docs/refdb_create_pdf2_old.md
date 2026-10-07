# Use Old Format PDF-2 as Reference Database

## Use Old Format PDF-2 as Reference Database
If you would like to apply a ICDD PDF-2 database in the
old format (i.e. release before 2005) as reference database, you can do so as follows:
Similar to current PDF-5+, PDF-2 or PDF-4 versions, you first
have to tell Match! that you would like to use an ICDD PDF database, by
marking the checkbox "ICDD PDF" in the upper part of the "Create Reference Database" dialog. Afterwards, please
select "PDF-2 Release 2004 (or earlier versions)" in the drop-down box below
"ICDD PDF".
You now have to give the directory in which the PDF-2 database (to be exact: the file
"pdf2.dat") is stored in the input box below "Location of PDF-2 / NBS*AIDS83
database". The easiest way to do so is to click on the "..." button to the right
of this input line. A "File Open" dialog will be displayed in which you have to select the file "pdf2.dat"
in the directory where your PDF-2 database is stored. Afterwards, press "Open" to
select the file/directory and return to the "Create Reference Database" dialog. The location
of the PDF-2 database file will now be displayed in the corresponding input box.
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
Due to the large amount of data which have to be read and sorted, the creation of index files
is a rather time consuming process. The
procedure may take between a few minutes to an hour or even more, depending especially
on the drive access and processing speed of your computer.
When the indexation has finished, a corresponding message will be displayed.
Afterwards, the new reference database will appear in the Reference
Database Library.
If the new reference database is the only one available in the Reference Database
Library, it is selected for being used automatically. Otherwise, you have to
select
the new reference database manually.