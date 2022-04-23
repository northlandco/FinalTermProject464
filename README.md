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
The PythonConversions.ipynb file attached to this repository outlines and shows various lines of code that were used to manipulate and convert various data forms into the required .geojson file format for use in this web atlas. 

The conversions and maniupulations shown can be very easily reproduced with new data to in order to create new .geojson files for use in the atlas. 

When importing a .csv  file with latitiude and longitude columns, we will want to read it in and store it as a new variable. This will allow us to call it in the following lines of code. Once it has been read in, a line of code is ran to fill in any blank values. This helps clean up the dataset, and minimizes our chance for error when we begin doing analyses on the dataset. When looking at the first lines and dataset imported in the PythonConversions.ipynb file, for Canadian Airports, we created a new dataset and layer that narrowed down the airports to just those that were international. This was done by looking at the datasets column which indicated the airport types (International, Regional, ....etc.) and searching for the string 'International'. Another example of this step and the changes that would be required to reproduce it can be seen in the liens of code for "General Hospitals". Prior to exporting, we a pply a crs="EPSG: 3347" in order to keep it consistent across all layers and for use in the leaflet map. The file is then exported as a .geojson, and can be added to the /src folder in the repo.

When importing a .shp file, it is important to note the that an additional/corresponding .shx file must be uploaded as well. When shapefile are downloaded, they will typically contain additional files, including this .shx. Upload both files into Python. As was done for .csv, we will read in the shapefile and store it as a variable. Next is a very simple conversion on one line of code that will convert the shapefile into the requested file type (in this case .GEOJSON), and the conversion will be completed to the new file indicted in this line with extension .geojson. 

## Conclusion
In conclusion, this repository can be used as a template for anyone looking to map out spatial data from various sources and in various forms, into one interactive web atlas. The process and steps required to add layers and customize the map are made very easy through use of this template, and will allow beginners to spatial data mapping, coding, and other computer processes to very easily create their own interactive web atlas. 

## Current Layers and Metadata (April 21, 2022) ### (Update when new layer added)
### 1. Canadian Airports - "Canadian Airports with Air Navigation Services"

summary/description: 	Canadian airports served by NAV CANADA control towers or flight service station.

spatial data type: 	Map Service

source/source url(s): https://open.canada.ca/data/en/dataset/3a1eb6ef-6054-4f9d-b1f6-c30322cd7abf/resource/d805cd5e-b91c-4598-849f-ca2d89f72ed9

date collected: May 19, 2021

date published: May 19, 2021

an explanation of each attribute:
Fields:
      Shape ( type: esriFieldTypeGeometry, alias: Shape )
      TC_ID ( type: esriFieldTypeDouble, alias: Identifier )
      IATA ( type: esriFieldTypeString, alias: International Air Transport Association Airport (IATA) Code, length: 254 )
      ICAO ( type: esriFieldTypeString, alias: International Civil Aviation Organization (ICAO) Code, length: 254 )
      TYPE ( type: esriFieldTypeString, alias: Airport Type, length: 254 )
      TYPE_CODE ( type: esriFieldTypeDouble, alias: Airport Type Code )
      AIRPORT ( type: esriFieldTypeString, alias: Airport Name, length: 254 )
      CITY ( type: esriFieldTypeString, alias: City, length: 254 )
      PROVINCE ( type: esriFieldTypeString, alias: Province, length: 254 )
      LATTITUDE ( type: esriFieldTypeDouble, alias: Lattitude )
      LONGITUDE ( type: esriFieldTypeDouble, alias: Longitude )
      OBJECTID ( type: esriFieldTypeOID, alias: Unique identifier )

spatial resolution: 

coordinate system: NAD_1983_Canada_Atlas_Lambert

projection: NAD_1983_Canada_Atlas_Lambert

extent: 	[[-146.108061782699,36.4810686346204],[-34.2795533650949,72.4613643971491]]

use limitations/license: 	Open Government Licence - Canada (https://open.canada.ca/en/open-government-licence-canada)


### 2. Canadian General hospitals
summary/description:

spatial data type: 	

source/source url(s):

date collected: May 19, 2021

date published: May 19, 2021

an explanation of each attribute:

spatial resolution: 

coordinate system: 

projection: 

extent:

use limitations/license:

### 3. NHL Arenas
summary/description:

spatial data type: 	

source/source url(s):

date collected: May 19, 2021

date published: May 19, 2021

an explanation of each attribute:

spatial resolution: 

coordinate system: 

projection: 

extent:

use limitations/license:

### 4. NFL Stadiums
summary/description:

spatial data type: 	

source/source url(s):

date collected: May 19, 2021

date published: May 19, 2021

an explanation of each attribute:

spatial resolution: 

coordinate system: 

projection: 

extent:

use limitations/license:

### 5. Canada Census Metropolitan Area Boundaries
summary/description:

spatial data type: 	

source/source url(s):

date collected: May 19, 2021

date published: May 19, 2021

an explanation of each attribute:

spatial resolution: 

coordinate system: 

projection: 

extent:

use limitations/license:

### 6. First Nations in Canada
summary/description:

spatial data type: 	

source/source url(s):

date collected: May 19, 2021

date published: May 19, 2021

an explanation of each attribute:

spatial resolution: 

coordinate system: 

projection: 

extent:

use limitations/license:

### 7. Canadian Major Mining Sites
summary/description:

spatial data type: 	

source/source url(s):

date collected: May 19, 2021

date published: May 19, 2021

an explanation of each attribute:

spatial resolution: 

coordinate system: 

projection: 

extent:

use limitations/license:

### 8. Canadian National Park Boundaries
summary/description:

spatial data type: 	

source/source url(s):

date collected: May 19, 2021

date published: May 19, 2021

an explanation of each attribute:

spatial resolution: 

coordinate system: 

projection: 

extent:

use limitations/license:

### 9. MLB Stadiums
summary/description:

spatial data type: 	

source/source url(s):

date collected: May 19, 2021

date published: May 19, 2021

an explanation of each attribute:

spatial resolution: 

coordinate system: 

projection: 

extent:

use limitations/license:

### 10. Canadian International Airports 
summary/description: 	Canadian airports served by NAV CANADA control towers or flight service station.

spatial data type: 	Map Service

source/source url(s): https://open.canada.ca/data/en/dataset/3a1eb6ef-6054-4f9d-b1f6-c30322cd7abf/resource/d805cd5e-b91c-4598-849f-ca2d89f72ed9

date collected: May 19, 2021

date published: May 19, 2021

an explanation of each attribute:
Fields:
      Shape ( type: esriFieldTypeGeometry, alias: Shape )
      TC_ID ( type: esriFieldTypeDouble, alias: Identifier )
      IATA ( type: esriFieldTypeString, alias: International Air Transport Association Airport (IATA) Code, length: 254 )
      ICAO ( type: esriFieldTypeString, alias: International Civil Aviation Organization (ICAO) Code, length: 254 )
      TYPE ( type: esriFieldTypeString, alias: Airport Type, length: 254 )
      TYPE_CODE ( type: esriFieldTypeDouble, alias: Airport Type Code )
      AIRPORT ( type: esriFieldTypeString, alias: Airport Name, length: 254 )
      CITY ( type: esriFieldTypeString, alias: City, length: 254 )
      PROVINCE ( type: esriFieldTypeString, alias: Province, length: 254 )
      LATTITUDE ( type: esriFieldTypeDouble, alias: Lattitude )
      LONGITUDE ( type: esriFieldTypeDouble, alias: Longitude )
      OBJECTID ( type: esriFieldTypeOID, alias: Unique identifier )

spatial resolution: 

coordinate system: NAD_1983_Canada_Atlas_Lambert

projection: NAD_1983_Canada_Atlas_Lambert

extent: 	[[-146.108061782699,36.4810686346204],[-34.2795533650949,72.4613643971491]]

use limitations/license: 	Open Government Licence - Canada (https://open.canada.ca/en/open-government-licence-canada)

---------------------------------------------------------------------------------------------------------------
