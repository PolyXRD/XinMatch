# Create Combined Combined Reference Database From User Data

## Create Combined Reference Database
It is possible to create a reference database that contains entries from more than one source. For example, you could create a reference database that consists of both the PDF-4 Minerals and the COD database that comes along with Match!. This is how to do it:
First of all, please make sure to display the  Reference Database Library dialog,
then click on the "Create" button at its bottom, in order to display the "Create Reference Database" dialog.
You now have to tell Match! that you would
like to use an ICDD PDF database, by marking the checkbox "ICDD PDF" in the upper
part of the "Create Reference Database" dialog.
Afterwards, you must select which PDF database you would like
to use. In our case, we would like to use the PDF-4 Minerals 2021, so please mark (click on)
the corresponding line in the list below "ICDD PDF". (Please note that you must have installed the PDF-4/Minerals on your computer, of course; otherwise this database won't be available in the list!)
In the next step, please click on (mark) the checkbox "COD database included in Match! program package" as well.
By default, Match! will try to find a reasonable name for your combined reference database, like "PDF-4 Minerals 2021 and COD-Inorg REV254652 2020.07.29". If you like, you can change this name at the bottom of the
dialog (deactivate the corresponding "Automatic" checkbox first!), and/or change
the location (directory) in which the index files for the new reference database shall be stored.
(Normally, Match! will automatically select an appropriate directory.)
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
-
It is perfectly possible to create a combined reference database that also contains your own data, in addition to the PDF and/or the COD. To do so, simply mark the checkbox "User data" as well, and select the corresponding Match! user database file (*.mtu), by pressing the "Select user database file" button on the right-hand side.
- If you would like to create a combined reference database from more than a single user database file, you first have
to combine the corresponding mtu-files into a single new mtu-file. Afterwards, you can select this combined mtu-file as "User database" in the
"Create Reference Database" dialog as usual.