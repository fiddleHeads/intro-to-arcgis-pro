---
layout: default
title: Map Production in GIS with ArcGIS Pro
nav_order: 1
---

# Map Production in GIS with ArcGIS Pro

<p align="center">
  <a href="#introduction">Introduction</a>&nbsp;|
  <a href="#user-interface">User Interface</a>&nbsp;|
  <a href="#starting-a-project">Starting a Project</a>&nbsp;|
  <a href="#maps-and-map-properties">Maps and Map Properties</a>&nbsp;|
  <a href="#working-with-layers">Working with Layers </a>&nbsp;|
  <a href="#exporting-and-saving">Exporting and Saving</a>&nbsp;|
  <a href="#what-next?">What Next?</a>
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

Make sure you have ArcGIS, including ArcGIS Pro, installed on your machine prior to the workshop.
Give yourself several days to ensure it is properly installed.
If you need assistance, contact [UBC Geospatial Resources](http://gis.ubc.ca/connect/).

#### Download Workshop Data
To get started with this workshop, you'll need to first download a spreadsheet of street tree data from the City of Vancouver [Open Data Portal.](https://opendata.vancouver.ca/pages/home/)

Download [Data](https://opendata.vancouver.ca/explore/dataset/street-trees/download/?format=csv&timezone=America/Los_Angeles&lang=en&use_labels_for_header=true&csv_separator=%3B){: .btn .btn-blue }
1. Save this file (.**zip**) to your Desktop.
2. Right-click on the .zip file you just downloaded and select **Extract All**...
3. Accept all defaults to extract the file.    

Open the new **Intro-to-ArcGIS-Pro** folder. This is your project folder which contains the files:
- Intro.**gdb**: the geodatabase with data for your map
- Intro.**aprx**: the project file with all the maps
- Intro.**tbx**: a toolbox with analytical tools for your project
- Index: folder with background organizing information
