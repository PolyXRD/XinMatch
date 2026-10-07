# Reference Database Library

## Reference Database Library
Match! is capable of handling more than a single reference pattern database at a time:
You can switch between all reference databases you have created (i.e. created index files for) while keeping your diffraction data in memory,
thus enabling you to compare
phase analysis results from various reference databases. Of course, it is not necessary
to perform a re-indexation of a reference database when switching between them!
The reference databases are handled in the so-called "Reference Database Library" dialog. You can
display it by selecting the "Select/create reference database" command from the "Database" menu, or by
pressing the corresponding button  in the
toolbar.
The "Reference Database Library" contains a list (in fact two lists) of all reference databases that are
available for the current user (see below). For each available reference database,
the name, the number of entries, and the directory in which it is stored are displayed.
There are two lists of reference databases, one for reference databases that are
available to all users (the upper list), and
another one that can only be accessed by the current user below.
The database you are currently using is identified by an ">>>" arrow to its left.
On a multi-user machine (e.g. using Windows XP, Vista or Windows 7/8), each user may have individual reference database(s). It is perfectly possible to create a new reference
database as a normal (standard) user, i.e. it is not necessary to have administrator
privileges for this task. However, please note that a standard user can create
reference databases only for himself, while an administrator can create databases
for all users. If a database is available to all users, this is indicated by a '*'
sign in the column "All". Note that databases with this mark cannot be modified or
deleted by normal (standard) users!
You can manage your reference databases using the six buttons at the bottom of the
"Reference Database Library" dialog:
- Select another reference database for search-match or database retrieval
purposes (of course without the need to perform a complete new indexation!). Please
note that the current contents of the candidate list and the Restraints buffer will be erased
if you select a new reference database!
- Create a new reference database (e.g. from an existing PDF or user database, or
by importing entry data from cif files)
- Add a reference database that is stored "ready for usage" in a certain directory
- Rename an existing reference database
- Shift (move) an existing PDF-2 reference database to a new location/directory
- Delete an existing reference database