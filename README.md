# CMS-Tutorial-for-High-School-Use
University of Notre Dame Quark Net version of the CMS Root Tutorial

This directory is the central directory for the master files for the CMS Data
Analysis Tutorial (http://ippog.org/resources/2012/cms-hep-tutorial) based on 
top-antitop (frequently refered to as ttbar) decay authored by Jun.-Prof. Dr. 
Christian Sander and Dr. Alexander Schmidt as used by the CMS Data group at the 
University of Notre Dame Quark NET Center starting in the summer of 2015.

This directory contains files that should not be changed while in this directory.
Any changes you need to make should be done in another directory.  This will allow
the original program files to be preserved unchanged.  It is recommended that you
create subdirectories for the various parts of the tutorial exercises.

To work with these files in your own directories, first copy the file
Makefile.dist into your directory as "Makefile" (no extension).  To copy the
necessary files ready for your use, use the command "make setup" at the command
prompt.  This will place the files example.C, MyAnalysis.C, and MyAnalysis.h in
the directory.  Do not attempt to change the names of these files except if you
wish to archive versions of your code.  Each usable version of your code must
have these file names.  This is part of the reason it is recommended to use
separate subdirectories for each part of the tutorial.

Notes on the functionality of this package:

Changes should only be made to example.C, MyAnalysis.C, and MyAnalysis.h.  Changes
to other files should not be necessary, with the exception of doing analysis on
another data set.

To prevent rewriting new pdf output files over old ones, you can change several
lines in example.C to create files with new names.  Near the end of the file you
should see a reference to the Plotter function and two blocks of code that Plot.
At the end of each block, you'll see that the program is saving to files named
inside quotes and parentheses.  You can change the file names in quotes to
whatever you wish to keep your plots separate.

The Plotter function (uneditable) currently has a default setting of creating
plots with the y axis as a log plot.  This cannot be changed from histogram to
histogram within a program run.  It can be changed on a run by run basis.  To
have a run with a non-log plot, you will need to make a change in example.C.  At
the bottom of the file where it calls Plotter, you can put ", false" between the
two end parentheses.

The other functions should not be and do not need to be edited.  Feel free to look at
the functions, but complete understanding and alteration are not necessary.
