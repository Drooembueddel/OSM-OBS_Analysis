Scripts to analyse data from OpenBikeSensors (https://www.openbikesensor.org/) in combination with OpenStreetMap.

Built on top of this: https://nbviewer.org/github/radverkehr/OpenBikeSensor_Analysis/tree/gh-pages/


* _1-0: Let's you download OSM-Data from https://download.geofabrik.de/ (replace URL for area of interest, large areas might lead to long processing times), extracts needed information and converts to *.gpkg
* _1-1: Downloads OBS-Data from a list of websites where users can upload their data. List might not be complete - adjust as needed. Also exports as *.gpkg
* _1-2: Merges the two data-sets from above using OSM-ID and checks for duplicats (might appear if people upload their dara to more than one website). Again exports as *.gpkg
* _1-3: Uses merged Data and classifies bike-lanes to the german classes of: Schutzstreifen, Radfahrstreifen, Seitenstreifen. Also Protected Bike Lanes, bus lanes, bicycle streets and a few more. Also (if possible) computes road and
lane widths while considering parking and simplyfies parts of the OSM data structure (:left, :right, :both are checked for place of interest).
* _2-1: descriptive statistics.
* _2-5:
  1) Let's you create groups of overtaking events based on types of infrastructure and a couple other aspects. Description of possible ways in the comments.
  2) Creates plots that visually compare the groups
  3) Statistically compares the groups to see if they show significant differences in the overtaking distances.
