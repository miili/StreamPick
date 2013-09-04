StreamPick
==========

A leightweight PyQt frontend to pick seismic wave arrival times in traces contained in an [ObsPy](http://www.obspy.org) [Stream](http://docs.obspy.org/master/packages/autogen/obspy.core.stream.Stream.html#obspy.core.stream.Stream) object. For further processing the picks can be treated in ObsPy or exported to QuakeML format (see [obspy.core.event](http://docs.obspy.org/master/packages/autogen/obspy.core.event.html) and https://quake.ethz.ch/quakeml/).

Running the Program
-------------------
A Stream object is created and passed to streamPick.

```python
from obspy import read
from streamPick import *

st = read('test.mseed')
new_picks = streamPick(st)

new_picks.getPicks()
>>> List of obspy.core.event.Pick objects
```

You can save the picks as a **QuakeML** catalog. And handle the catalog through ObsPy:

```python
from obspy.core import event

cat = event.readEvents('myPicks.xml')
```

Usage
-----
StreamPick Gui. Navigate through the timeseries with the Mouse wheel: Click and Drag the plot to move in time, use the mouse wheel to zoom in and out.

![streamPick-gui](https://raw.github.com/miili/StreamPick/master/img/streamPick-gui.png)

Mouse click and **q** sets P-Wave arrival, **w** S-Wave pick. Click and push **t** for custom wave phase, hit **r** to remove picks from trace.

Check ``About`` for more useful hotkeys:

![streamPick-about](https://raw.github.com/miili/StreamPick/master/img/streamPick-about.png)

Installation
------------

There sure are numerous methods add a module to Python. Check these out:

Clone from the GitHub repository

```bash
git clone https://github.com/miili/StreamPick.git
```

```python
from streamPick import *
```
see above

Through Python PIP

```bash
pip install https://github.com/miili/StreamPick/archive/master.zip
```

Dependencies
------------
streamPick relies on:

* PyQt4
* ObsPy (tested v0.8.4)
* NumPy (tested v1.7.1)
* SciPy (tested v0.12.0)
* Matplotlib (tested v1.1.1rc)


Development
-----------

Things to be missed

- Wadati Diagram
- Manageable list of Picks


Contributing
------------
Everybody is welcome to contribute! :)

Please follow ObsPy's styles https://github.com/obspy/obspy/wiki#developer-corner 
