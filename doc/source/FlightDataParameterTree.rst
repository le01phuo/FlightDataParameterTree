=======================
FlightDataParameterTree
=======================

The `FlightDataParameterTree` is an web-based application which displays the dependency tree used in the generation of an HDF file. It also displays a table containing parameter information for completing and correcting logical frame layouts.

.. image:: flight_data_parameter_tree.png

-------------------
Starting the server
-------------------

The `FlightDataParameterTree` server is started by running the `flightdataparametertree.server` module. An instance of a web browser will load the application automatically.

.. code-block:: bash
   
   $ python server.py
   FlightDataParameterTree (c) Copyright 2013 Flight Data Services, Ltd.
    - Powered by POLARIS
    - http://www.flightdatacommunity.com
   
   Spacetree server is running at http://localhost:8080/
   Quit the server with CONTROL-C.
   Registering additional web browsers...
   Launching viewer in a web browser...

The URL of the application is `http://localhost:8080/spacetree`.

--------------------
Loading the HDF file
--------------------

An HDF file created by the `FlightDataAnalyzer` is required to use the `FlightDataParameterTree` tool.

.. image:: load_hdf_file.png

Click on the `Browse` button, select an HDF file and finally click on the `Submit Query` button to process the file.

--------------
Parameter Tree
--------------

The parameter tree visualises the dependency tree created during the processing of the HDF file. Each node of the tree is one of the following:

* `LFL Parameter`
* `Derived Parameter`
* `Flight Attribute`
* `Flight Phase`
* `Key Point Value`
* `Key Time Instance`
* `Missing Dependency`

Clicking and dragging the background of the tree will change the view position.

Clicking on a node will rearrange the tree to show the node's dependencies and any nodes which depend upon it.

Nodes may be searched for by entering a partial name into the `Search` text input field. A list of matching parameter names will appear. Click on an entry within the list to rearrange the tree.

----------------------
LFL Parameter Analysis
----------------------

This section includes a table of information regarding the parameters stored within the HDF file.

.. image:: lfl_parameter_analysis.png

Columns:

* `LFL Parameter` - Whether or not the parameter is defined in the LFL.
* `Key Parameter` - Whether or not the parameter is a considered to be a key parameter for flight data monitoring.
* `Database` - Whether or not the parameter exists within the POLARIS database.
* `Limits` - Whether or not the parameter has validation limits defined within the POLARIS database.

The table columns can be searched by entering a partial match into the text fields below the column headers. For searching on boolean columns enter either `tick` or `cross`.

----------------------
Missing LFL Parameters
----------------------

A list of missing LFL parameters is displayed at the bottom of the page. This is a list of common parameters which have not been found within the HDF file, but are expected to exist in the majority of LFLs.

.. image:: missing_lfl_parameters.png

Some parameters included in this list may not be appropriate for all aircraft such as engine parameters for engines numbered 3 and 4.