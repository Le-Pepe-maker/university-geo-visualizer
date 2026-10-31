# Opengeoapi
A tool that uses the free OpenStreetMap API (Nominatim service) to convert university names into geographical locations and visualizes them on an interactive map.
Prerequisites: Python 3 and DB Browser for SQLite (to view or modify the database). Note that Windows users should use the PowerShell terminal to avoid problems displaying UTF-8 characters.

Step 1: Data Loading: Run python3 geoload.py to read locations from the where.data file. This script checks the opengeo.sqlite database first to avoid redundant API queries, then fetches missing coordinates from the API and stores them.

Step 2: Data Processing: Run python3 geodump.py to read the SQLite database and generate a where.js file, which formats the locations, latitudes, and longitudes into an executable JavaScript array. 

Step 3: Visualization: Open where.html in a web browser to view the interactive map. The map uses the OpenLayers library and draws background tiles from the OpenStreetMap Germany tile server.

Supported by py4e

