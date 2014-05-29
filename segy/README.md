Reading and writing SEG-Y files
===============================

The idea is to adapt Thomas Majer Hansen and Robert Smallshire's [SegyPY code](https://code.google.com/p/segpy/source/browse/), which doesn't quite work, it seems.

So far, it is reading data - but incorrectly - for some byte types, and failing completely for IBM floats. 

Best thing is probably to start with [the IPython Notebook](http://nbviewer.org/github/kwinkunks/notebooks/blob/master/segy/Loading%20and%20saving%20SEGY.ipynb).

Note that this directory contains files modified by me. All this stuff, including this notebook, is licensed under LGPL. The data are public domain, as far as I can tell. 
