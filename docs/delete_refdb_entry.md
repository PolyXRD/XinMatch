# Delete entry from reference database

## Delete entry from reference database
You can delete one or more entries that is/are currently marked in the candidate list from the reference database under the following conditions:
- You must have write access to the directory in which
the current reference database is stored. If this does not apply, a corresponding error message will be displayed.
- You cannot delete ICDD PDF database entries.
- Once you have deleted one or more entries from a reference database, it can no longer be used by Match! version 1. However, you can copy the actual user database file (user_database.mtu) from the reference database
directory and create a new reference database from it in Match! version 1.
In order to delete on or more entries, please mark them in the candidate list first, e.g. by keeping the <Ctrl> button pressed while clicking on them. Afterwards, you can either run
the "Delete reference database entry" from the "Database" menu, or select the corresponding command from
the context menu of the candidate list (which can be opened by right-clicking on the corresponding line/entry
to be deleted).
You will be asked for confirmation. After a few seconds, a message will be displayed
indicating that the entry has been deleted from the current reference database.
### Cleaning of database files
When one or more entries are deleted from the database, Match! in fact only updates the index files. The original entries are still kept within the database file, in order to avoid shifting/copying a lot of data while the software is still in use.
When the user closes Match!, the program checks if entries have been edited or deleted, and removes the surplus entry data from the database file before finally closing. This procedure may take a few seconds.