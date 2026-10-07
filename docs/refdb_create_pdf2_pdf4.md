# Use ICDD PDF-5+, PDF-4 or PDF-2 as Reference Database

## Use ICDD PDF-5+, PDF-4 or PDF-2 as Reference Database
Using the ICDD PDF database products with Match! is pretty easy: Simply install the PDF database on your
Windows PC according to the instructions given by ICDD, then launch Match!.
Match! will automatically
detect newly installed PDF database products at program startup (at least if the
corresponding option is set) and
ask if you would like to index one of them straight away. If you agree by clicking "Yes", the
database indexing will be performed immediately. You will then be asked if you would like to
use the new reference database straight away. You can do so by clicking "Yes" again. That's it!
Please note::
- Even if you click "No" in the last step, you can switch over to the new PDF reference database later on in the
Reference Database Library.
- You can also check for new/updated PDF database products from within Match!, by running the
"Database/Check for new PDF databases..." menu command.
You can also perform the indexing of a PDF database manually, of course. In the following, we will demonstrate how to apply an existing ICDD PDF-5+, PDF-4 or PDF-2 database as
a Match! reference database:
Let us assume that you would like to add the ICDD PDF-2 Release 2025
database (which must of course have been installed already) (the procedure for using
the corresponding PDF-5+ or PDF-4 is the same):
First, please open the Reference Database Library,
and press the "Create" button at the bottom. You now have to tell Match! that you would
like to use an ICDD PDF database, by marking the checkbox "ICDD PDF" in the upper
part of the "Create Reference Database" dialog.
Afterwards, you must select which PDF database you would like
to use. In our case, we would like to use the PDF-2/Release 2025, so please mark (click on)
the corresponding line in the list below "ICDD PDF".
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
Due to the large amount of data which have to be read and sorted, the creation of index files is a rather time consuming process. The
procedure may take between a few minutes to an hour or even more, depending especially
on the drive access and processing speed of your computer.
When the indexation has finished, a corresponding message will be displayed.
Afterwards, the new reference database will appear in the Reference
Database Library.
If the new reference database is the only one available in the Reference Database
Library, it is selected for being used automatically. Otherwise, you have to
select
the new reference database manually.
Please note:
- If you would like to use the PDF-5+, PDF-4 or any other current ICDD PDF database product,
this can be done in a similar way than the procedure just described for the PDF-2.
- The ICDD PDF relational database products (like PDF-5+, PDF-4, PDF-2 starting with release 2005 etc.)
are currently only available for the Windows platform. Hence, you cannot use these databases
if you are running Match! on a Mac or Linux machine!
-
If you would like to use an older PDF relational database that is only available as 32-bit application (e.g.
the PDF-2 2010) on a Windows 64-bit operating system, please make sure to also use the 32-bit
version of Match!.
The background is that when using the 64-bit version of Match!, the software is unable to access the
32-bit database access library that is installed along with the PDF, so Match! cannot detect
its presence and ignores it.
More recent versions of the PDF are installed as 64-bit applications on 64-bit Windows system, so
the problem does no longer occur.
- Starting with version 4.2, Match! is able not only to use local (fixed) PDF licenses but also supports floating PDF server licenses.