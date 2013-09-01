StreamPick
==========

A leightweight PyQt frontend to pick seismic wave arrival times in traces contained in an [ObsPy](http://www.obspy.org) [Stream](http://docs.obspy.org/master/packages/autogen/obspy.core.stream.Stream.html#obspy.core.stream.Stream) object. For further processing the picks can be exported to QuakeML format (see [obspy.core.event](http://docs.obspy.org/master/packages/autogen/obspy.core.event.html) and https://quake.ethz.ch/quakeml/).

Running the Program
-------------------
A Stream object is created and passed to streamPick.

```python
from obspy import read
from streamPick import *

st = read('test.mseed')
new_picks = streamPick(st)

new_picks.picks
>>> List of obspy.core.event.Pick objects
```

Usage
-----

[Screenshots]

Installation
------------

The sure are numerous methods add a module to Python. Here are the most comman ones.

Clone from the GitHub repository

```bash
git clone https://github.com/miili/StreamPick.git
```

Through Python PIP

```bash
pip install https://github.com/miili/StreamPick/archive/master.zip
```

Dependencies
------------
streamPick relies on:

* PyQt
* ObsPy
* Matplotlib


Development
-----------

Things I miss

- Wadati Diagram
- Manageable list of Picks


Contributing
------------
Everybody is welcome to contribute! :)

Please follow ObsPy's styles https://github.com/obspy/obspy/wiki#developer-corner 
