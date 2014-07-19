Reading and writing SEG-Y files
===============================

The idea is to adapt Thomas Majer Hansen and Robert Smallshire's [SegyPY code](https://code.google.com/p/segpy/source/browse/), which doesn't quite work, it seems.

So far, it is reading data - but incorrectly - for some byte types, and failing completely for IBM floats. 

Best thing is probably to start with [the IPython Notebook](http://nbviewer.org/github/kwinkunks/notebooks/blob/master/segy/Loading%20and%20saving%20SEGY.ipynb).

Note that this directory contains files modified by me. All this stuff, including this notebook, is licensed under LGPL. The data are public domain, as far as I can tell. 

Seismic data
============

The data are all from the US and Canadian governments and therefore public domain.

- `ld0057_file_00095.sgy` is a Lithoprobe line from NRCan. [Available online](http://apps1.gdr.nrcan.gc.ca/lithoprobe/ksz/ld0057_file_00095.sgy). This is the file Hansen used in his original SegyPY code.
- `31_81` is a USGS file from the North Slope of Alaska. [Read all about it](http://wiki.seg.org/wiki/ALASKA_2D_LAND_LINE_31-81). I've seen it used in Madagascar examples, and it's available online in [Part 1](http://certmapper.cr.usgs.gov/nersl/NPRA/SEISMIC/1981/31_81/DMUX/L23535.SGY), [Part 2](http://certmapper.cr.usgs.gov/nersl/NPRA/SEISMIC/1981/31_81/DMUX/L23536.SGY), [Part 3](http://certmapper.cr.usgs.gov/nersl/NPRA/SEISMIC/1981/31_81/DMUX/L23537.SGY), . Here's [an image of it](http://certmapper.cr.usgs.gov/nersl/NPRA/SEISMIC/1981/31_81/IMAGES/31_81_IM.JPG). [Survey notes](http://certmapper.cr.usgs.gov/nersl/NPRA/SEISMIC/1981/31_81/DOCUMENTS/31_81_S.PDF) and [observer notes](http://certmapper.cr.usgs.gov/nersl/NPRA/SEISMIC/1981/31_81/DOCUMENTS/31_81_O.PDF).
