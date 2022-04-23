# Universal Spatial Data Mapper
Leaflet Map template to add various geodata layers to. Refer to Python data manipulation, and other documentation for easy data transformation, spatial joins, and more byb following the steps used to add the current data to the map. Data is visualized and sptially positioned on the Interactive Web Atlas. 

## Summary of Project
This interactive web atlas allows for easy data visualization of various spatial data sets. This online tool and the attached code demonstrate how various forms of data, such as .csv and .shp can be imported, manipulated, and converted into a .geojson file. Once a .geojson file has been produced using python, it can be added to the data repository folder /src. A corresponding icon image as a .png will also need to be added to the same folder in order to have a visual icon for that layer. 

Once converted into a .geojson by following the steps outlined, it can be added to the interactive web atlas with its own section on the legend where the layer can be toggled on or off, by following/copying the codes found in the script.js file. Depending on the data types (point, line, or polygon), the user simple has to find the corresponding title and nderneath will find that code to add it to the map. All that needs to be changed is the input file name to the newly created .geojson file, to change the icon image to the newly added/corresponding .png, and finally to give this layer a legend title.

Once the JS code has been edited, the newly added layer should appear in the legend toggled off. It can simply be toggled on, and a spatial representation of the data can be observed on the map. The map offers the ability to switch between the CartoDB Light baselayer, and the Esri World Imagery Sattelite baselayer.

The interactive atlas features additional imported tools, such as a dynamic scale bar, a search bar, a +/- button for zooming as opposed to scrolling to zoom, and a counter in the top right corner showing the current zoom level.

## Rationale for Project
This project was created in order to allow individuals across various fields to be able to easily map out spatial data, regardless of its original data form, at no-cost. The Public Repository functions as a collaborative place where people can add their own .geojson files directly or through various conversion or further data manipulation methods outlined in the termpython.ipynb file. It allows various data spatial data that would likely otherwise not be found together in an interactive atlas, to be combined and added to this map. 

Suppose a real estate agent has a client who is trying to determine which city or neighbourhood they would like to live in. This client has various factors that are important to making their choice. By adding the various spatial data sets to the map, a visual representation of their spatial distribution can be derived, offering an interactive map with their various important factors appearing. This could allow the client to easily visualize where they would like to live.

## Python Coding
The termpython.ipynb file attached to this repository outlines and shows various lines of code that were used to manipulate and convert various data forms into the required .geojson file format for use in this web atlas. 

Conversions:
- .csv to geojson
- shp to geojson
- 

Data Manipulation:
- using csv files --> extracting smaller dataset from larger set
- table join for population, density, and median income statistics for CMA's

## Current Layers and Metadata (April 21, 2022) ### (Update when new layer added)
### 1. Canadian Airports
summary/description:

spatial data type: 

source/source url(s):

date collected:

date published:

an explanation of each attribute:

spatial resolution:

coordinate system:

projection:

extent:

use limitations/license:


### 2. Canadian General hospitals

### 3. NHL Arenas

### 4. NFL Stadiums

### 5. Canada Census Metropolitan Area Boundaries

### 6. First Nations in Canada

### 7. Canadian Major Mining Sites

### 8. Canadian National Park Boundaries

### 9. 

### 10. Canadian International Airports 


## Conclusion


