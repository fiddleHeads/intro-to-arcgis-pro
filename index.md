---
layout: default
title: Map Production in GIS with ArcGIS Pro
nav_order: 1
---

# Map Production in GIS with ArcGIS Pro

<p align="center">
  <a href="master/index.">Introduction</a>&nbsp;|
  <a href="content/user-interface">User Interface</a>&nbsp;|
  <a href="content/start-a-project">Starting a Project</a>&nbsp;|
  <a href="content/maps">Maps and Map Properties</a>&nbsp;|
  <a href="content/layers">Working with Layers </a>&nbsp;|
  <a href="content/exporting">Exporting and Saving</a>&nbsp;|
  <a href="content/what-next">What Next?</a>
</p>

## INTRODUCTION

This is an introductory workshop focusing on the fundamental concepts and skills needed to begin using **ArcGIS Pro** for exploring and analyzing spatial data.

---
#### GIS Resources at UBC:
- General Informational website for all things UBC GIS: [gis.ubc.ca](http://gis.ubc.ca/)    
- UBC Library's guide for finding and working with GIS resources: [guides.library.ubc.ca/gis](http://guides.library.ubc.ca/gis)
- UBC's GIS email list (participate or lurk!): [UBC GIS ListServ](https://lists.ubc.ca/scripts/wa.exe?SUBED1=GIS-LIST&A=1)  
- UBC's GIS Slack (create your own channel or lurk!): [ubcgis.slack.com](https://ubcgis.slack.com/)
- Evan Thornberry, GIS Librarian @ UBC Library: evan.thornberry AT ubc.ca

### Setup
This workshop requires the installation of Esri ArcGIS available from the [UBC Webstore](http://gis.ubc.ca/software/).
Students are eligible to download the ArcGIS suite for a fixed amount. As of 2019, this was $30/year.
For faculty and staff the annual license is more expensive. 

If you do not want to purchase a license, you can sign up for a [free 21-day trial](https://www.esri.com/en-us/arcgis/trial?rmedium=esri_com_redirects01&rsource=https://links.esri.com/pro/trial).

Make sure you have ArcGIS Desktop installed on your machine prior to the workshop.
If you need assistance, contact [UBC Geospatial Resources](http://gis.ubc.ca/connect/).
Note: virtual access to the GIS lab at the Research Commons will be another option for accessing ArcGIS software in the future. Stay tuned.

There will be three applications that come with your download of ArcGIS Desktop.

- **ArcCatalog**: file browser for managing and organizing your data
- **ArcMap**: program to view, edit, and analyze data and create maps
- **ArcGIS Pro**: newer program that has similar functionality to ArcMap but more 3D capability and better communication with ArcGIS Online

For the purposes of this workshop, we will only be using **ArcGIS Pro**.

#### Download Workshop Data
To get started with this workshop, you'll need to first download a [GeoJSOn](https://geojson.org/) of street tree data from the City of Vancouver [Open Data Portal.](https://opendata.vancouver.ca/pages/home/). 
You can explore other file formats available for [street tree data](https://opendata.vancouver.ca/explore/dataset/street-trees/export/?disjunctive.species_name&disjunctive.common_name&disjunctive.height_range_id). 
You'll notice that the shapefile format is not available, which would have been the preferred format for working within ArcGIS Pro. 
Instead, we'll download the GeoJSON format and convert it to a shapefile later.

Included in your download is a project folder containing the following files:
- Intro.**gdb**: the geodatabase with data for your map
- Intro.**aprx**: the project file with all the maps
- Intro.**tbx**: a toolbox with analytical tools for your project
- Index: folder with background organizing information

Download [Data](https://opendata.vancouver.ca/explore/dataset/street-trees/download/?format=geojson&timezone=America/Los_Angeles&lang=en){: .btn .btn-blue }
1. Save this file (.**zip**) to your Desktop.
2. Right-click on the .zip file you just downloaded and select **Extract All**...
3. Accept all defaults to extract the file.    

## Need to add Pro project to download still...
