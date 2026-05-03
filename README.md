# Reachability Analysis Web GIS Application  

## Overview

This project implements a full-stack Web GIS application designed for real-time reachability analysis of emergency services. It enables users to identify accessible facilities within defined time and distance thresholds using interactive spatial tools.

The system integrates spatial databases, web mapping services, and client-side visualization to deliver a responsive and scalable geospatial application.

---

## Core Capabilities

- Interactive Web GIS interface for spatial visualization and querying  
- Real-time reachability analysis using isochrone-based services  
- Integration of multiple emergency facility datasets  
- Geocoding and location-based search  
- Layer-based visualization and spatial filtering  
- Responsive UI with authentication support  

---

## System Architecture

The application follows a three-tier geospatial architecture:

**Client Layer**
- Leaflet-based interactive map
- JavaScript tools for visualization and user interaction
- Bootstrap-based responsive UI

**Application Layer**
- GeoServer for serving spatial data (WMS/WFS)
- Firebase for hosting and authentication
- Node.js-based integration components

**Data Layer**
- PostgreSQL with PostGIS extension
- Spatial indexing and query execution
- GeoJSON-based data exchange

---

## Spatial Data Engineering Workflow

- Data acquisition from Google Earth Pro (KML format)  
- Data cleaning and normalization using spreadsheets  
- Conversion to Shapefile and GeoJSON formats  
- Import into PostgreSQL/PostGIS using spatial ETL tools  
- Publishing spatial layers via GeoServer services  
- Integration with Leaflet for client-side rendering  

---

## Key GIS Functionalities

### Reachability Analysis
- Isochrone-based service area generation using OpenRouteService API  
- Supports time-based and distance-based accessibility queries  

### Geocoding and Search
- Address-to-coordinate conversion using OSM geocoding services  
- Enables dynamic location-based querying  

### Facility Proximity Analysis
- Identification of nearest emergency services from:
  - User location (GPS/IP-based)
  - User-defined points
  - Existing facilities  

### Layer Management
- Dynamic toggling of spatial layers  
- Multi-layer overlay support for comparative analysis  

---

## Technology Stack

**Geospatial Technologies**
- PostGIS (spatial database design and querying)  
- GeoServer (OGC-compliant map services: WMS/WFS)  
- Leaflet.js (web mapping and visualization)  

**Backend & Integration**
- PostgreSQL (relational database management)  
- Node.js (application logic integration)  

**Frontend**
- HTML, CSS, JavaScript  
- Bootstrap (UI framework)  

**Deployment & Services**
- Google Firebase (hosting and authentication)  
- OpenStreetMap (base maps and geocoding)  
- OpenRouteService API (isochrone analysis)  

---

## Spatial Database Design

- Structured storage of point-based emergency facilities  
- Attribute schema includes:
  - Name, Address, Category, Coordinates  
- Spatial indexing for optimized query performance  
- Use of GeoJSON for efficient client-server data transfer  

---

## Implementation Highlights

- Hybrid processing architecture:
  - Client-side rendering to reduce server load  
  - Server-side querying for spatial operations  
- Efficient data delivery using GeoServer services  
- Lightweight GeoJSON format for faster map loading  
- Secure authentication using Firebase  

---

## Application Interface

### Authentication Module
![Authentication](https://user-images.githubusercontent.com/60979131/103412137-babd9c00-4b99-11eb-8f61-bc1f54da5111.PNG)

### Main Web GIS Interface
![Web App](https://user-images.githubusercontent.com/60979131/103412257-3881a780-4b9a-11eb-8b5c-872095f9663a.png)

---

## Deployment

The application is deployed using Firebase Hosting and is accessible via:

https://findservicearea.web.app/

---

## Limitations

- Dependency on external APIs (OpenRouteService, OSM)  
- Static dataset for Chennai limits real-time updates  
- Limited backend automation for dynamic data ingestion  

---

## Technical Takeaways

- Demonstrates full-stack Web GIS development  
- Combines spatial databases, OGC services, and frontend mapping  
- Implements real-time spatial querying and analysis  
