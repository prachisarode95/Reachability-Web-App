# Reachability-Web-App

Aim:
To develop indigenous web-based application for real time decision planning at any location.

Objectives:
The main objective of this study is to create a Web GIS application using open source tools. Leaflet, GeoServer and PostgreSQL/PostGIS have been used to create the application. The following objectives:
–	To understand Web-GIS technologies, use of libraries & frameworks for building web application.
–	To develop & deploy web-based application using open source standards.
–	To build tools with multiple functions that provide real-time visualization & interaction experience.
–	To provide benefits of free online services for more accurate results.
–	To understand & analyse final results for real-time decision planning in the future.

Data:
The data for this project was obtained from ‘Google Earth Pro’ open source software. The KML files downloaded, cleaned using ‘Google Sheets’ & converted to shapefile using ‘ArcMap 10.4’ software. The data contains location information like ‘Address, Name of location, City, State & Country with Latitudes and Longitudes’ as well. The following location data have been used for the project:
•	Emergency Care Hospitals (Point Data)
•	Ambulance Stations (Point Data)
•	Police Stations (Point Data)
•	Fire Stations (Point Data)
•	Blood Banks (Point Data)

Software:
•	Google Earth Pro
•	Google Sheets
•	QGIS 3

Methodology:
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


Location based services are meant to be provided and reached within certain limit of time & distance. Current scenario shows lacking of real-time spatial data with accurate information. Location based services are meant to be reached within distance & time limit. 

Current project is proposed to give users accessibility to the real time geo-spatial data. Using this web application, users can interact with data or use map tools to get appropriate results about knowing where the service area should be available to up to what limit it should be given and so on. This web app contains multiple tools that can be used to experience the real-time interaction with geo-spatial data provided with it. The collected geospatial data was only for Chennai City but users can use this application at any location and use other location (geospatial) information for real-time experience. The application is especially provided with reachability tool to find out service area at any location point.

