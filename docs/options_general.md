# General Options

## General Options
On the "General" page of the "Options" dialog, some very basic settings can be adjusted:
### Check for available updates of the Match! software at program startup
Once this option has been activated (which is actually the default state), Match! will automatically check for a more recent version
on the Crystal Impact webserver each time it is executed. In order to achieve
this, a working connection to the internet is required, of course. If you are not
connected to the internet, Match! will ask you to do so before continuing.
You might want to disable this option if you are not permanently connected to the internet. Please note that the box "Save as
defaults" in the corner on the lower left-hand side of the dialog must also be checked
in order for the change to be effective!
### Check for new or unused PDF databases at program startup
If this option is activate (which is the default state), Match! will automatically check for
newly installed PDF database products at program startup and
ask if you would like to index one of them straight away. If you agree by clicking "Yes", the
database indexing will be performed immediately. You will then be asked if you would like to
use the new reference database straight away. You can do so by clicking "Yes" again.
### Automatically save information for restore
If this option is active (which is default), Match! will automatically save the current contents of the
Match! document every N minutes, where N can be adjusted using the "Interval (minutes)" slider. The default
value of N is 10 (minutes).
If Match! is restarted after it has been accidentally closed, it will automatically restore the previously
saved contents.
Please note that the contents of the User database manager is not saved by this option, because
it is not included in the Match! document format!
### Default selection preset
Once you have created a so-called "selection criteria preset" using the corresponding buttons at the bottom of the "Restraints" or "Additional entries" tabs on the right-hand side of the screen, you can define one of these presets to be active right away when you create a new document/session (or when you run the Match! program). This is e.g. useful if you are normally working on rather similar samples for which the same set of selection criteria should be applied, e.g. certain elements that must or must not be present etc.
Please note that you have to mark the checkbox "Save as defaults" at the bottom to make this setting permanent!
### External program paths
In this section you can set the paths to external programs like FullProf, Endeavour or Diamond.
#### Diamond program path (Windows version only)
Here you can define the directory in which the Diamond software for crystal and molecular structure visualization
is installed. This may be useful
if you have not installed Diamond in the default directory and/or Match! has not been able to determine the path to Diamond automatically.
In order to define the path of your Diamond installation, simply press the "Modify..." button and select the corresponding directory. If a valid path to Diamond is available, you can simply display
the crystal structure of a marked entry by running the menu command "Entries/View in Diamond", or
by pressing the corresponding button  in the toolbar.
#### Endeavour program path (Windows version only)
Here you can define the directory in which the Endeavour software for crystal structure solution from powder diffraction data.
This may be useful
if you have not installed Endeavour in the default directory and/or Match! has not been able to determine the path to Endeavour automatically.
In order to define the path of your Endeavour installation, simply press the "Modify..." button and select the corresponding directory. If a valid path to Endeavour is available, you can simply run a crystal structure calculation of a marked entry by running
the menu command "Tools/Structure solution (Endeavour)", or
by pressing the corresponding button  in the toolbar.
#### FullProf program path
Here you can define the directory in which the FullProf Suite is installed. This may be useful
if you have skipped the corresponding step when Match! was run for the first time, or if you
have moved your FullProf installation to a new directory.
In order to define the path of your FullProf installation, simply press the "Modify..." button and select the corresponding directory.
#### Treor90 program executable
Here you can define the path and file name of the Treor90 indexing program that shall be used by Match!. By default, Match!
will use the Treor90 program included in the FullProf Suite (if it is installed).
You can select a different Treor90 program to be used by pressing the "Modify..." button and selecting the corresponding Treor90 executable.
#### Dicvol program executable
Here you can define the path and file name of the Dicvol indexing program that shall be used by Match!. By
default, Match! will use the Dicvol program included in the FullProf Suite (if it is installed).
You can select a different Dicvol program to be used by pressing the "Modify..." button and selecting the corresponding Dicvol executable.
### Default settings
If you enable the checkbox "Save as defaults" in the left bottom corner of the "Options" dialog, the setting of all options will be the same next time you execute Match! or create a new document.