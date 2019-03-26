# Map Production in GIS with ArcGIS Pro

<p align="center">
  <a href="#introduction">Introduction</a>&nbsp;
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
---
#### Download Workshop Data
To get started with this workshop, you'll need to first download the data and files :exclamation: here :exclamation:.
1.  Save this file (.**zip**) to your Desktop.
2. Right-click on the .zip file you just downloaded and select **Extract All**...
3. Accept all defaults to extract the file.    

Open the new **Intro-to-ArcGIS-Pro** folder. This is your project folder which contains the files:
- Intro.**gdb**: the geodatabase with data for your map
- Intro.**aprx**: the project file with all the maps
- Intro.**tbx**: a toolbox with analytical tools for your project
- Index: folder with background organizing information

## USER INTERFACE
ArcGIS Pro is the latest desktop GIS software from the software company Esri. This software must be purchased, downloaded, installed, and configured on your computer for it to work as intended. Those of you at the University of British Columbia can find more information about the availability of ArcGIS Pro software :exclamation: here :exclamation:.

Open the software and get familiar with the default user interface.
1.  In Windows, go to the Programs menu and find the ArcGIS Program Group, then select ArcGIS Pro.
2. In the dialog window, click on **Create a New Project > Blank**. This will create a new project file (.**aprx**), and open the ArcGIS Pro main user interface.
3. In the new dialog window, click ok to accept the defaults and finish creating your new project.

You should see something like this:
:exclamation:[image showing the main UI components]:exclamation:

### Main UI Components
The ArcGIS Pro user interface (UI) has a few main components:
- The **Map Frame**: This is where your data will be visualized.
- The **Contents Pane**: This will likely be your most used "tabbed" window because it's where you'll interact with your data. As you add data to your project, they'l appear here as **layers**.
- The **Catalogue Pane**: This pane is similar to Windows Explorer, or Mac Finder. You can create connections to data sources (drives, folders, networks, etc.) and perform several data maintenance and management tasks in this pane. The search option is also available here, which is used to search for tools, documents, and data.
- **Menu Tabs**: These are located at the top of the main UI and can be  selected/activated as needed. We will use these later in the tutorial.

#### Insert a New Map
The first step we will want to take is to insert a new map in our UI.
 In the **Main Menu**, select **Insert > New Map**. Notice that a new map tab has been added to the Map Frame and Tools from the Main Menu are now enabled.

#### Interact with Tabbed Menus
 Move your cursor to the **Contents Pane**, and notice the small down arrow on the right side. If clicked, this arrow give you options to **Float**, **Dock**, **Auto-Hide**, and **Close** the pane.    

Using the **Catalog Title Bar**, click and drag the Catalog Pane away from its docked position. Notice the "docking arrows" that appear as you move the window.

#### Explore the Windows (Catalog)
Using the Windows Explorer,  navigate to the **Intro-to-ArcGIS-Pro** directory where you extracted this workshop's files, and click into the **Data** folder.

Note that there are more files in this folder than there are Shapefiles as ArcGIS Pro shows. This is because a Shapefile is not actually _a file_, but instead _a collection of files_.

1. Return to ArcGIS Pro and right-click on the folders item in the **Catalog Pane**, then select **Connect Folder** (or **Go to Insert**) **> Add Folder**
2. Select the **Desktop** icon and click **OK**.
3. Expand the resulting **Folder Connection** in the **Catalog Window** and expand the folder::exclamation: **XXXX.gdb**.:exclamation:

Note that the features are simplified in the **Catalog Window**. Although the Feature Class is made of several files, ArcGIS Pro knows it's better just to show the Shapefile. This allows you to copy, paste, rename, etc. without having to manage several files per dataset.

## STARTING A PROJECT
### Map Projects

So what exactly is an **ArcGIS Pro Project**? When you first add a blank map and begin "_adding_" data and creating different symbologies, labeling schemes, etc., you are modifying a Map Project. The word _adding_ is emphasized because you are not actually adding data. Instead, you are _linking_ data using file paths. The reason for this is because often times GIS data is several megabytes or even gigabytes in filesize. Having all of that data displayed in your map project would be impractical and taxing on your computer. So, the project doesn't actually contain the data, but only links to it. Map Projects are then configured with styles, symbologies, labels, etc.

Go to **Project > Open** and open the map document called :exclamation: . This file will be the only file with the **.aprx** extension. Notice that the home folder in Catalog has changed to the one used for the **.aprx** file.

#### Fixing Broken Links

You'll see that your layers (in your **Contents Pane**) have a small :exclamation: next to them. This means that you're experiencing the **Broken Link** issue - which is VERY common when working in GIS with layers and the paths pointing to them. You'll need to fix them to continue.

1. Click on the :exclamation: of one of the layers.
2. Navigate to the XXXX.gdb of the tutorial dataset and select the Shapefile that corresponds to the layer you clicked and select **OK**.

Since all your layers are in the same directory, all of your layers should now be repaired. It's generally good practice to have your data organized logically, which will help to fix the inevitable broken link issue.


## MAPS AND MAP PROPERTIES

### Projections and Coordinate Reference Systems

#### Change a Coordinate Reference System

### Explore Navigation and Tools in Data Frames

#### Zoom to layer

#### Bookmarks

## WORKING WITH LAYERS

#### Layer Visibility

#### Display order

#### Feature Layer Tab

### Layer Attributes

#### Select by Attributes

### Symbology

### Labels

### Adding Data

### Joining Tables

### Definition Queries

### Symbology - Graduated Colours

## EXPORTING AND SAVING

### Layout Mode

### The Map Frame

### Layout Navigation

#### Resizing the Data Frame

#### Adding Map Elements

### Export Your Map

## What's Next?
### Thanks - Stanford Geospatial Center
