# Introduction to GIS {-}



GIS is the abbreviation for *geographic information system*. It is a computer-based tool designed to collect,
store, process, analyse, visualise and interpret spatially referenced data. 

<center><img src="https://raw.githubusercontent.com/ThamesEstuaryPartnership/booklet/main/Figures/GIS2.jpg" width = "100%" height = "auto"></center>
<center>Components of Geographic Information System</center>
<br>

GIS is a useful tool to help answer geographic questions and make decisions. 

For example, GIS can be used by climatologists to understand the causes and consequences of climate change, by political consultants to develop campaign strategies for elections or by epidemiologists to locate ground zero of a disease outbreak. 

<center><img src="https://raw.githubusercontent.com/ThamesEstuaryPartnership/thameseels/main/workshops/GIS/img/gis1.png" width = "100%" height = "auto"></center>
<center>COVID-19 Dashboard (Source: John Hopkins University)</center>
<br>

## Geographic Information {-}

In GIS geographic information is made up of spatial location data and attribute data. 

- Spatial location data is data with geographic component. It answers the question *where something is*.

- Attribute data answers the question *what something is*.

The database that contains these geographic information is called an **attribute table** and it can be used to symbolise features, make queries and to analyse the data. 

The example below shows a choropleth map of Internet users (per 100 people) in 2016 and its associated attribute table. 

<center><img src="https://raw.githubusercontent.com/ThamesEstuaryPartnership/thames-learn/main/Figures/figure1.jpg" width = "100%" height = "auto"></center>
<center>World map of Internet users (per 100 people) in 2016</center>
<br>

<center><img src="https://raw.githubusercontent.com/ThamesEstuaryPartnership/thames-learn/main/Figures/figure2.jpg" width = "100%" height = "auto"></center>
<center>Screenshot of the associated attribute table</center>
<br>

## System {-}

Made up of hardware and software, e.g. satellites, ArcGIS, QGIS. 

## GIS capabilities {-}

GIS has many capabilities. These are: 

- Data processing: GIS can be used to view, create, edit, transform and display geospatial data. 

- Spatial analysis: Different tools are used within GIS to identify trends, patterns and relationships in data. For example spatial analysis can be creating buffers, clipping features, network analysis, performing spatial statistics and so on. 

- Map making: Map making helps spatially represent data from multiple sources (e.g. spreadsheets). This is the most common use of GIS.

- Imagery and remote sensing: This is used to extract information from imagery and remotely sensed data (e.g. satellites).

- Data collection and management: This can help to access, use, integrate and store data in a GIS.

## GIS data {-}

### Types {-}

Geographic information can be stored either as a vector data or a raster data. 

**Vector data**

Vector (or feature) data is categorical data stored as geometrical shapes such as:

- Points: Points are single x,y coordinate locations. 

- Lines: Lines are defined by two or more points that are connected with lines. 

- Polygons: Polygons are defined by multiple points that are connected with lines and are closed. 

For example, geospatial data that show the location of buildings, rivers or ponds. 

<center><img src="https://raw.githubusercontent.com/ThamesEstuaryPartnership/thames-learn/main/Figures/figure3.jpg" width = "350" height = "auto"><img src="https://raw.githubusercontent.com/ThamesEstuaryPartnership/thames-learn/main/Figures/figure3a.jpg" width = "350" height = "auto"></center>
<center>Vector types and vector data drawn on a map</center>
<br>

**Raster data**

Raster data is made up of a matrix of pixels, called cells, with each being the same size and containing a value that represents the conditions for the area covered by that cell. Raster data formats include JPEG (Joint Photographic Experts Group), BMP (Bitmap Image), PNG (Portable Network Graphics) and TIFF (Tagged Image File Format) files. 

<center><img src="https://raw.githubusercontent.com/ThamesEstuaryPartnership/thames-learn/main/Figures/figure4.jpg" width = "100%" height = "auto"></center>
<center>Raster data</center>
<br>

Raster data represents continuous data (integer or real values) like temperature or elevation.

The example map below shows the average sea surface temperature on the 1st April in 2008. 

<center><img src="https://raw.githubusercontent.com/ThamesEstuaryPartnership/thames-learn/main/Figures/figure5.jpg" width = "100%" height = "auto"></center>
<center>Sea surface temperature on 01/04/2008 (Source: Naval Oceanographic Office)</center>
<br>

**Metadata**

Here it also worth mentioning metadata which is essentially data about data. It provides additional information about the (geographic) data such purpose, who created it, scale, projection, attributes, its usage constraints and so on. The more detailed the metadata is, the easier for the user to interpret it and implement it. 

### Capture {-}

Primary data capture is a direct data acquisition methodology. Directly captured data can come from a global positioning system (GPS) or from remote sensing and surveying technologies. For example, data collected during field surveys, using satellite imaginary or Lidar. 

**Lidar**

Lidar (Light Detection and Ranging) is a remote sensing method that uses light in the form of a pulsed laser to measure ranges to the Earth. These light pulses—combined with other data recorded can generate precise, three-dimensional information about the shape of the Earth and its surface characteristics. A lidar instrument principally consists of a laser, a scanner and a specialised GPS receiver. 

The two types of Lidar are: 

- Topographic uses a near-infrared laser to map the land.

- Bathymetric uses water-penetrating green light to also measure seafloor and riverbed elevations.

Secondary data capture is an indirect data acquisition methodology. For example, the use of existing geospatial data (e.g. through sites like [NASA](https://nasa.github.io/data-nasa-gov-frontpage/){target="_blank"} or [NOAA](https://www.ncdc.noaa.gov/data-access){target="_blank"}) available in both digital and hardcopy formats. 

A third way of data capture is digitization. This is used to create digital files from the original paper copy.

### Format {-}

Vector and raster data can be stored and distributed in different formats. 

**Shapefile**

Shapefile was first developed by Esri and it is the most widely known format for distributing geospatial vector data. A shapefile will always come in a .zip format containing the following files: 

- .shp: Contains the geometry of each feature.

- .dbf: Contains the attribute data for all of the features in the dataset.

- .shx: Spatial index, it allows GIS systems to find features within the .shp file.

- .prj: Contains information about the projection and coordinate system the data uses.

- .cpg: This is an optional plain text file that describes the encoding applied to create the shapefile.

- .sbn and .sbx: These are also optional files that store the spatial index of the features.

- .qmd: Metadata stored by QGIS. 

**GeoJSON**

GeoJSON is a JavaScript format used to store geospatial vector data. It consists from the following different parts:

- Geometry object: This is either the point, line, or polygon described earlier.

- Feature object: This is the geometry object and the associated random data.

- FeatureCollection: A list of feature objects.

GeoJSON is widely used in web-based mapping (e.g. Leaflet or CartoDB) as this format is easy to handle and also "lighter" than a shapefile. 

**TopoJSON**

TopoJSON is simply an extension of the GeoJSON format that encodes topology.

**CSV, TXT, and GPX files**

Spreadsheet data can be stored and used in different GIS software in a comma-separated values text file (.csv), a delimited text file (.txt) or GPS Exchange Format file (.gpx) format.

**KML**

KML (Keyhole Markup Language) is a file format used to display geographic data in an Earth browser such as Google Earth or ArcGIS Earth. KMZ files are the zipped versions KML files. 

**GeoTiff**

GeoTiff has georeferenced information embedded within an image file. 

**NetCDF**

NetCDF (Network Common Data Form) files are a standard for the exchange of scientific data in binary format. This is used for storing raster data in GIS. 

**API**

It is also worth mentioning API (Application Programming Interface). API is a software intermediary that allows two applications to talk to each other. For example, a data layer stored on ArcGIS can be directly plugged into a map made in QGIS or other web-mapping software.
In GIS, a data layer through API can be accessed via Web Mapping Service (WMS), Web Feature Service (WFS) or GeoJSON. 

:::note
**<i class="fa fa-lightbulb-o" aria-hidden="true"></i> Tip**: 

Useful sites: 

- [Build custom geojson](https://geojson-maps.ash.ms/){target="_blank"} website for the creation of simplified GeoJSON regions. 

- [geojson.io](https://geojson.io/#map=2/20.0/0.0){target="_blank"} is a quick, simple tool for creating and viewing vector data. 

- [Mapshaper](https://mapshaper.org/){target="_blank"} can be used to edit Shapefile, GeoJSON, TopoJSON, CSV and several other data formats, written in JavaScript.

- [MyGeodata Converter](https://mygeodata.cloud/converter/){target="_blank"} is an online GIS data conversion and transformation tool. 

- [Ogre](https://ogre.adc4gis.com/){target="_blank"} translates spatial files into GeoJSON. 
:::

### Quality {-}

Due to how geospatial data is collected, analysed and represented, uncertainties with data quality may arise. These errors are in fact expected as almost all representations of the world are incomplete.

Two primary attributes that characterise data quality are precision and accuracy. 

**Precision** refers to the fineness and exactness of the measurements, whilst **accuracy** is the difference between the recorded value and the true value. 

To understand the difference between precision and accuracy, consider the illustration below: 

<center><img src="https://raw.githubusercontent.com/ThamesEstuaryPartnership/thames-learn/main/Figures/figure6.jpg" width = "500" height = "auto"></center>
<br>

When it comes to data quality in GIS, here are some of the things look out for: 

- The completeness of the attribute table (Is there any data missing?)

- Temporal consistency (Is it up-to-date?)

- Location accuracy (Is the position of the feature correct?)

- Logical consistency (Is the data topologically correct?)

Unfortunately, the more accurate and precise a geospatial data is, the higher cost is to obtain it and store it. This is because of the time and equipment used to collect the data. Larger data will also always require constant maintenance.  

### Finding data {-}

In the age of information, the world wide web has large amount of data available. A quick Google search can normally help to find geospatial data. However, it is best to acquire data from trusted sources.

- [ArcGIS Living Atlas of the World](https://livingatlas.arcgis.com/en/home/){target="_blank"}: This is a collection of geographic information from around the globe.

- [Cathcment Based Approach Data Hub](https://data.catchmentbasedapproach.org/){target="_blank"}: GIS data package is a set of over 150 data layers, which is provided to CaBA catchment hosts in the UK. 

- [Copernicus](https://scihub.copernicus.eu/dhus/#/home){target="_blank"}: Copernicus is the European Union's Earth observation programme. 

- [Defra UK](https://environment.data.gov.uk/){target="_blank"}: Defra Data Services Platform

- [EmodNet](https://emodnet.eu/en){target="_blank"}: EmodNet is the gateway to marine data in Europe. 

- [Esri Data Hub](https://hub.arcgis.com/search){target="_blank"}: Esri houses over 250,000 open data sets from 5,000 organisations worldwide. 

- [JNCC Marine Protected Area (MPA) mapper](https://jncc.gov.uk/mpa-mapper/){target="_blank"}: This is an interactive resource containing information on the MPAs designated in UK and Crown Dependency waters.

- [Koordinates](https://koordinates.com/){target="_blank"}: This is a geospatial data management platform.

- [MAGIC](https://magic.defra.gov.uk/home.htm){target="_blank"}: The MAGIC website provides authoritative geographic information about the natural environment from across government.

- [Marine Regions](https://www.marineregions.org/){target="_blank"}: This is a standard list of marine georeferenced place names and areas.

- [Natural Earth Data](http://www.naturalearthdata.com/downloads/){target="_blank"}: This site houses key cultural and physical vector GIS datasets.

- [Public Datasets](https://github.com/awesomedata/awesome-public-datasets){target="_blank"}: These are datasets collected and tidied from blogs, answers, and user responses. 

- [Terra Populus](https://terra.ipums.org/){target="_blank"}: Terra Populus holds population and environmental data. 

- [Open Geospatial Datasets](https://github.com/andrea-ballatore/open-geo-data-education){target="_blank"}: This is a repository of open geospatial datasets to be used in an educational context.

- [OpenStreetMap](https://www.openstreetmap.org/#map=5/54.910/-3.432){target="_blank"}: OSM has some of the most detailed information on our planet.

Apart from these, there are many governmental and non-profit platforms that offer free access to geospatial data. 

## GIS software {-}

There are a number of open-source (software that is freely available for use) and commercial GIS software available. Here are some of the most well-known (both desktop and web-based): 

- [Carto](https://carto.com/){target="_blank"}

- [Esri](https://www.esri.com/en-us/arcgis/products/index){target="_blank"}

- [D3.js](https://d3js.org/){target="_blank"}

- [Flowmap.blue](https://flowmap.blue/){target="_blank"}

- [Flourish](https://flourish.studio/){target="_blank"}

- [GoogleEarth](https://earth.google.com/web/){target="_blank"}

- [Leafletjs](https://leafletjs.com/){target="_blank"}

- [Mango](https://mangomap.com/){target="_blank"}

- [Mapbox](https://www.mapbox.com/){target="_blank"}

- [MapInfo Pro](https://www.precisely.com/product/precisely-mapinfo/mapinfo-pro){target="_blank"}

- [Mapnik](https://mapnik.org/){target="_blank"}

- [QGIS](https://www.qgis.org/en/site/){target="_blank"}

- [R Studio](https://rstudio.com/){target="_blank"}

- [Tableau](https://www.tableau.com/en-gb){target="_blank"}

## Summary {-}

:::note
**<i class="fa fa-edit fa-2x"></i>**

- GIS is the abbreviation for geographic information system. It is a computer system used to create, manage, visualise, analyse and interpret spatially referenced data.

- GIS is used to answer geographic questions and make decisions based on geospatial data.

- Geographic information is made up of spatial location data *(where something is)* and attribute data *(what something is)*.

- GIS can be used for geospatial data processing, spatial analysis, map making, imagery and remote sensing, and data collection and management. 

- GIS data can either be vector or raster data. 

- The quality of geospatial data will depend on the time spent and the equipment used to collect it. However, almost all representations of the world are incomplete. 

- Nowadays there are many Internet platforms that offer open-access geospatial data. 
:::

<hr>

## Reference resources {-}

### Books {-}

- [An Introduction To Using GIS In Marine Biology (2nd Edition)](http://gisinecology.com/an-introduction-to-using-gis-in-marine-biology-2nd-edition/){target="_blank"}
- [Essentials of Geographic Information Systems](https://resources.saylor.org/wwwresources/archived/site/textbooks/Essentials%20of%20Geographic%20Information%20Systems.pdf){target="_blank"}
- [Geographic Information Systems Demystified](https://books.google.co.uk/books/about/Geographic_Information_Systems_Demystifi.html?id=TPgsAQAAMAAJ&redir_esc=y){target="_blank"}
- [Geographic Information Science and Systems](https://www.wiley.com/en-gb/Geographic+Information+Science+and+Systems%2C+4th+Edition-p-9781119031307){target="_blank"}
- [Principles of Geographic Information Systems](https://webapps.itc.utwente.nl/librarywww/papers_2009/general/principlesgis.pdf){target="_blank"}

### Free courses and tutorials {-}

- [A Gentle Introduction to GIS](https://docs.qgis.org/3.16/en/docs/gentle_gis_introduction/index.html){target="_blank"}
- [EcoSpatial e-Learning](http://ecospatial.info/){target="_blank"}
- [Getting started with GIS](https://www.esri.com/training/catalog/57630434851d31e02a43ef28/getting-started-with-gis/){target="_blank"}
- [GIS Basics](https://www.esri.com/training/catalog/5d9cd7de5edc347a71611ccc/gis-basics/){target="_blank"}
- [Introduction to GIS](https://ocw.mit.edu/resources/res-str-001-geographic-information-system-gis-tutorial-january-iap-2016/introduction-to-gis/){target="_blank"}
- [Marine Spatial Planning](https://classroom.oceanteacher.org/tag/index.php?tc=1&tag=Marine%20Spatial%20Planning&ta=2&excl=1){target="_blank"}
- [The Nature of Geographic Information](https://www.e-education.psu.edu/natureofgeoinfo/node/1672){target="_blank"}

### Paid courses and tutorials {-}

- [Geographic Information Systems (GIS) Specialization](https://www.coursera.org/specializations/gis){target="_blank"}
- [GIS, Mapping, and Spatial Analysis Specialization](https://www.coursera.org/specializations/gis-mapping-spatial-analysis){target="_blank"}
- [Introducing Mapping, Spatial Data and GIS](https://www.conted.ox.ac.uk/courses/introducing-mapping-spatial-data-and-gis-online/){target="_blank"}

### Other {-}

- [Geospatial Revolution](https://www.geospatialrevolution.psu.edu/){target="_blank"}
- [GIS Dictionary](https://support.esri.com/en/other-resources/gis-dictionary){target="_blank"}
- [What is lidar?](https://oceanservice.noaa.gov/facts/lidar.html#:~:text=Lidar%2C%20which%20stands%20for%20Light,variable%20distances%20to%20the%20Earth){target="_blank"}
