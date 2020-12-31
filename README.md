# Reachability-Web-App
**Aim**:
To develop indigenous web-based application for real time decision planning at any location.

**Objectives**:
The main objective of this study is to create a Web GIS application using open source tools. Leaflet, GeoServer and PostgreSQL/PostGIS have been used to create the application. The following objectives:
1. To understand Web-GIS technologies, use of libraries & frameworks for building web application.
2. To develop & deploy web-based application using open source standards.
3. To build tools with multiple functions that provide real-time visualization & interaction experience.
4. To provide benefits of free online services for more accurate results.
5. To understand & analyse final results for real-time decision planning in the future.

**Proposed Project**:
Location based services are meant to be provided and reached within certain limit of time & distance. Current scenario shows lacking of real-time spatial data with accurate information. Location based services are meant to be reached within distance & time limit. 

Current project is proposed to give users accessibility to the real time geo-spatial data. Using this web application, users can interact with data or use map tools to get appropriate results about knowing where the service area should be available to up to what limit it should be given and so on. This web app contains multiple tools that can be used to experience the real-time interaction with geo-spatial data provided with it. The collected geospatial data was only for Chennai City but users can use this application at any location and use other location (geospatial) information for real-time experience. The application is especially provided with reachability tool to find out service area at any location point.

**Data**:
The data for this project was obtained from ‘Google Earth Pro’ open source software. The KML files downloaded, cleaned using ‘Google Sheets’ & converted to shapefile using ‘ArcMap 10.4’ software. The data contains location information like ‘Address, Name of location, City, State & Country with Latitudes and Longitudes’ as well. The following location data have been used for the project:
1. Emergency Care Hospitals (Point Data)
2. Ambulance Stations (Point Data)
3. Police Stations (Point Data)
4. Fire Stations (Point Data)
5. Blood Banks (Point Data)

**Software Used**:
1. Google Earth Pro
2. Google Sheets
3. QGIS 3

**Open-Source Frameworks Used**:
1. PostgreSQL/PostGIS
2. GeoServer
3. Leaflet Mapping Library
4. Bootstrap
5. Google Firebase
6. Node.js

**Methodology**:
1. Cleaning the dataset
2. Converting data into geocoded information
3. Converting it into ‘Shapefile’ & ‘GeoJSON’ format
4. Configuring PostgreSQL Database.
5. Importing database using PostGIS Shapefile Import/Export Manager
6. Uploading & Publishing data on GeoServer
7. Creating basic web application using QGIS2Web Plugin
8. Customizing it with ‘‘Leaflet’ tools (HTML, CSS & JAVASCRIPT FILES)
9. Deploying it with Google Firebase Service
10.Interaction, Visualization & Analyzation of final results

**Results & Discussions**:
The developed web application consists of various useful GIS tools for spatial data visualisation, analysis, querying and finally interaction for final results. The use of and effective database management system allows for effective storage, management and retrieval of spatial data. The adopted approach and its implementation using PostgreSQL, PostGIS, GeoServer to develop a web-based application provides public users data sharing and mapping services. It shares the information and geospatial datasets allowing users with limited knowledge to access the information customized for specific application that will reduce operation cost management and assist people in their decision- making process. The GIS and various web technologies can be efficiently combined as a mechanism to share spatial information freely, openly and easily.

**System Implementation**
The research produced an online web GIS application with a hybrid architecture where, spatial functions are conducted on the client side to minimize data traffic between the web server and browser thus smooth operation without processing lag. On the server side of the system, ‘GeoServer’ which serves the application files to browsers and queries the database in response to the requests made within the web application. PostgreSQL uses a client-server model where the client and server can reside on different files, accepts connections to the database from client applications. It executes database requests from clients and sends the results back to the clients. Remote clients can connect over the network or internet to the server.
The system architecture is shown below in figure:
'image'
PostgreSQL provides and supports many client applications for database administration such as the psql interactive command-line utility and ‘pgAdmin’, a PHP-based web interface for database administration. To use PostgreSQL databases to store data for your applications, you can connect your applications using any of the supported libraries or drivers, available for most popular programming languages. PostGIS is spatial database extender for PostgreSQL object-relational database. It adds support for geographic objects allowing location queries to be run in SQL. GeoJSON, which is a lightweight data-interchange format, less verbose than XML and ultimately results in lower data file size alternatives such as Geography Markup Language (GML) or Keyhole Markup Language (KML) both of which are XML based. GeoJSON’s lower file sizes results in faster system load time and its simplicity enables easy parsing of the geometry and fields led to its selection for use in the different facilities. The web based app requests for map tiles from the Open Street Map tile service that form the base map for the system showing regional boundaries, roads and other points of interest. Other web map tile services such as Google maps and Bing maps can be integrated into the system to provide base maps but they have restrictions in the number of calls for tiles that can be made and require a license keys for use. Open Street Map tile service was selected for use because it has no restrictions and is free with an open license.

**User Interface Design**
'image'
The research endeavoured to produce a ‘Web GIS App’ with a simple and intuitive interface that would enable first time GIS users to use the system with minimal instruction. The interface page includes ‘Title bar’ showing name of the web app which was created using ‘Navbar’, one of the Bootstrap-4 JavaScript libraries. ‘About page’ describes the basic information about the web application, added below the ‘Title bar’ and created using ‘Jumbotron’, Bootstrap-4 JavaScript library. The rest of the page includes ‘Sign-Up’ & ‘Sign-In’ forms which were created by using ‘Forms’ form Bootstrap-4 JavaScript library as well. Entire web page was built using Bootstrap-4 JavaScript Libraries. Later, this interface was connected and functioned with ‘Google Firebase Authentication’ service for user’s log in/out activities.
'image'
The interface is a part of second web page when user will get logged in and then ‘logout’ option will start appearing on title bar. It includes a map window showing various GIS tools for user interface, also it displays location of all emergency facilities in Chennai city. Attribution tool is added in the bottom-right corner of the map window. All tools are specially built for reachability analysis only. The interface has zoom in/out buttons so that user can get all the map features with detailed information in real-time.  It has layer control that enables users to toggle layers from the display as well as ‘Geocode and ‘Search’ button. The main tool panel is appearing in left side of the map window, and has different options for user interaction with real-time experience using ‘OpenStreetMap’ (OSM) API service. The system was built in such a way that it is responsive and thus the interface maintains its display integrity and appears the same across screen sizes. Following figure shows how the system renders on a mobile device.
'image'

**GIS Functionalities within Web Application**

1. **Geocode Search**
This tool transforms an address or the name of a place into latitude and longitude. The geocoding tool within all the facilities, web GIS leverages the Open Street Map geocoding engine to enable users to search for locations using the name of the place. This tool will aid both planners, engineers and the public to quickly find service areas of interest to them within the system.

2. **Facility Search**
This tool enables the user to search for the nearest facilities in emergency from any one of the following:
•	The user’s current location: The system uses IP (Internet Protocol) geo-location on a desktop computer and GPS on mobile devices. Permission for the system to access location has to be granted within the web browser settings.
•	A user defined point: The user can define a point by clicking on any location on the map.
•	Another facilities: The user selects a facility from a list of available facilities and the search is then run from the selected facilities.
This special tool will aid in emergency facility location planning where planners can determine the closest facility and ultimately the distance to it. It also enables users to search for any facility by name within the system and then identifying the facility on the map. Once a search is done clicking a result will zoom onto the selected facility and highlights it.

3. **Layer Overlay**
The application has the ability to switch the map layers. User can select all layers together or can switch to one layer also.

4. **System Security**
Progressive Web Apps must be served over HTTPS. Firebase Hosting, by default serves the app contents over HTTPS. FirebaseUI provides a drop-in-responsive authentication flow based on Firebase Authentication, allowing the application to integrate a sophisticated and secure sign-in flow with low effort. FirebaseUI automatically adapts to the screen size of a user’s devices and follows best practices for auth flows.

5. **Reachability Analysis**
Reachability analysis has done using the Leaflet plugin ‘Reachability’, is one of the JavaScript library to show areas of reachability based on time or distance for different modes of travel using ‘OpenRouteService’ (OSM) isochrones API.

**Conclusion**
The web GIS development process faces new challenges such as lack of information during or before any emergency. This research has endeavoured to overcome these challenges by innovating on the conventional web GIS architecture and adding client side processing to minimise the volume of the data transferred between the browser and the web server. The research has also developed a system with an intuitive and streamlined user interface to enable non-specialist or the ones not familiar with GIS, to operate the system without any additional training. The research has managed to meet the set out goals of developing a tool for monitoring and evaluation of facilities used in emergency situations, also managed to develop for public interaction to collect, visualise and analyse spatial information.
This web map application was built to analyse the reachability index between facility and user’s location or any incident point which can be reached within given distance and time limit in the respective web map.  The purpose behind building this application was to represent the possibility of facility or service location points to be reached to the user’s location in a less time with respect to distance.  After analysing, it is concluded that all the results with different parameters or attribute information determined the accuracy level of OSM’s API services as well as the functionality of leaflet map with multiple tool options.
The system developed in this research is web based and will work in any browser and on any device, regardless of screen size. This will enable local facility search and geocoding service to access, use and visualise spatial data in a timely manner.
