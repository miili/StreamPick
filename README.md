StreamPick
==========

A leightweight Qt frontend to pick seismic wave arrival times in an ObsPy Stream object (see obspy/obspy). For further processing the picks can be exported to QuakeML format (see obspy.core.event and https://quake.ethz.ch/quakeml/).

Example
-------
A Stream oject is created and passed to streamPick.

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

Screenshots

Installation
------------

Clone from the GitHub repository

```bash
git clone 
```

Through Python PIP

```bash
pip install 
```
