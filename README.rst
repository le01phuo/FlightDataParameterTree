Introduction
============

FlightDataParameterTree is a web application which runs on your computer to graphically display the dependency tree diagram used during processing of derived parameters by the FlightDataAnalyzer.

Using the dependency tree stored within the HDF file after analysis, the FlightDataParameterTree is able to display each derived parameter’s dependencies in an interactive graph. The dependency tree is the central component of the FlightDataAnalyzer, using graph theory to establish relationships between all the derived algorithms (derived phases, flight phases, key point values, etc.). A breadth first search algorithm is used to establish the processing order of the algorithms, ensuring the optimal number of dependencies are available for analysis. The FlightDataParameterTree helps one to understand which dependencies where determined as unavailable during analysis of a data file.

Project sponsored by `Flight Data Services`_ and released under the Open 
Software License (`OSL-3.0`_).

Source Code
-----------

Source code is available from `GitHub`_:

* https://github.com/organizations/FlightDataServices/FlightDataParameterTree

Usage
-----

Download source code and run server.py from source.
::

    python FlightDataParameterTree/server.py

Documentation
-------------

.. _Flight Data Services: http://www.flightdataservices.com/
.. _Flight Data Community: http://www.flightdatacommunity.com/
.. _OSL-3.0: http://www.opensource.org/licenses/osl-3.0.php
.. _GitHub: https://github.com/
.. _Python Package Index: http://pypi.python.org/

.. image:: https://cruel-carlota.pagodabox.com/9932acf5231d508d118026b0e621d296
    :alt: githalytics.com
    :target: http://githalytics.com/FlightDataServices/FlightDataParameterTree
