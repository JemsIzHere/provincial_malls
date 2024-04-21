List_of_Malls_except_MM
=======================

This script scrapes data about shopping malls in the Philippines from Wikipedia, excluding those under constructio and malls in NCR. It categorizes malls based on their developer and whether they are major developers.

Dependencies
------------
- requests
- BeautifulSoup
- re

Usage
-----
python List_of_Malls_except_MM.ipynb

Functions
---------
- `extract_data(table)`: Extracts mall data from a given table.

------------------------------------------------------------------------------------------------------------

provincial_malls_polygon
=========================

This script scrapes data about shopping malls in the Philippines from Wikipedia, excluding those under construction and malls in NCR. It then uses OpenStreetMap to retrieve polygon points for each mall within the Philippines boundary, and finally, it categorizes malls based on their developer and whether they are major developers.

Dependencies
------------
- requests
- BeautifulSoup
- re
- pandas
- numpy
- osmnx
- geopandas

Usage
-----
python provincial_malls_polygon.ipynb

Functions
---------
- `format_polygon_points(polygon_points)`: Formats polygon points as a string in the required format.
- `get_polygon_points(place_name)`: Retrieves polygon points from OpenStreetMap within the Philippines boundary.
- `extract_data(table)`: Extracts mall data from a given table.

------------------------------------------------------------------------------------------------------------

provincial_malls_polygon_alt
=========================

This script reads the csv data produced by `python provincial_malls_polygon.ipynb` and fills in empty polygons. It is used when there is an issue with specific `mall_names`.

Dependencies
------------
- requests
- BeautifulSoup
- re
- pandas
- numpy
- osmnx
- geopandas

Usage
-----
python provincial_malls_polygon.ipynb

Functions
---------
- `format_polygon_points(polygon_points)` and `format_polygon_points2(polygon_points)`: Formats polygon points as a string in the required format.
- `get_polygon_points(place_name)`: Retrieves polygon points from OpenStreetMap using an **API request** within the Philippines boundary.
- `get_polygon_points2(place_name)`: Retrieves polygon points **directly** from OpenStreetMap within the Philippines boundary.