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
---
#### Download Workshop Data
To get started with this workshop, you'll need to first download the data and files :exclamation: here :exclamation:.
1. Save this file (.**zip**) to your Desktop.
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
In the **Contents Panel** you should see an item named **Layers**, followed by 3 layers corresponding to the Feature Classes in your Geodatabase. The “Map” item at the top of the Contents Panel represents the Data Frame which contains all of your layers. Click **List By Source** near the top left of the **Contents Panel**.

Note that the layers are organized underneath the path at which they are located. If this Map Document contained links to datasets in other locations, they would be listed under that path or network address.

### Projections and Coordinate Reference Systems
Coordinate systems tell your map how to project the geography of our spherical world, onto a flat screen. The datasets used in this map are actually all in the same projection (XXX :exclamation:) though it is not the one currently being used to display the data. In GIS, datasets have their own explicitly defined Projection/Coordinate Systems, while the Map Frame can also have a different Projection/Coordinate System.  

This allows you to add geographic data with different native Coordinate Systems to your map. ArcGIS Pro will treat the Data Frame’s Coordinate System as the Map’s Lingua Franca, projecting (on the fly) all of the new datasets to the Data Frame Projection. While convenient, it comes at a cost: Map Documents that make use of this type of on-the-fly projection render the data in the Data Frame at a much slower rate.  

In addition, disparate Projection/Coordinate Systems can cause major issues and errors when analyzing across layers (i.e. when geoprocessing that requires transfer of attributes across layers).

#### Change a Coordinate Reference System
Because of the issues with working with data in different projections in the same data frame, **it is good practice to select a Projection/Coordinate system that is suitable for your particular analysis and scale, and project all of your data to the same**. Do do that:

1.	**Right-click** on the **Map Item** at the top of the **Table of Contents** and select **Properties**…
2.	**Click** on the **Coordinate System Tab** and expand the **Layers Folder** in the “**Select a Coordinate System:**” panel.
3.	**Expand** the **Layers Folder** and **select** the **GCS_WGS_1984 Projection** file. **Click OK**.
4.	**Click Save**
(Auto-save option is available under Project > Options > Editing > Session)

What you have just done is reassigned the coordinate system of the **Map Frame** to that of the **Street Trees Layer**:exclamation:. This (XXXX:exclamation:) is actually the coordinate system of all of the layers in your **Contents**, so you should experience an increase in drawing performance, since ArcGIS Pro is no longer projecting these layers on-the-fly to the :exclamation:World from Space projection (which was chosen for its extremity, in this case):exclamation:. The result of this change should be a substantial change to the view on the Map.

### Explore Navigation and Tools in Data Frames
Before we begin to explore the properties of _individual layers_ in the **Map Document**, we will first spend some time getting familiar with the _navigation tools_ in the **Map Document**.  Most of these tools can be found on the **Map Tab: Navigation** toolbar, though some of the more useful ones involve right-clicking context menus of the layers, or using the mouse and mouse wheel (press to Pan, role to zoom).

#### Zoom to layer
Sometimes it is very helpful to see the entirety of a layer's extent. To fit the :exclamation:Street Trees layer into the **Map Frame**:
- Right-click on the :exclamation:Street Trees layer, in the Contents Panel, and select Zoom to Layer.

#### Tools Toolbar
In addition to the **Zoom to Layer** option, the **Tools Toolbar** provides the bulk of the tools for navigation in the **Data Frame**. Most of them are fairly explanatory. Take a moment to explore each of these tools, and how it works.
- The **Full Extent Button** zooms you to the full extent of the layer in your **Contents** with the largest spatial extent.  This can sometimes be problematic if you are working at a local level, but using one or more layers that are global in extent.
- The **Fixed Zoom In** button :exclamation:.
- The **Fixed Zoom Out** button :exclamation:.
- The **Previous Extent** works much like its analogous tool in your web browser, allowing you to step back through previous changes in scale/extent. This tool is particularly useful if you change your **Data Frame** extent inadvertently.

#### Bookmarks
Another useful navigation tool is the ability to create spatial **Bookmarks** that allow you to return to specific scales/extents that you define.

1. Using the **Zoom Tools** on the **Tools Toolbar**, zoom your map view to the area around **Downtown Vancouver**.
2. **Select Bookmarks > Create Bookmark**.
3. Name your Bookmark “***Downtown Vancouver***” and **click OK**.
4. **Click** on the **Full Extent** button in the **Tools Toolbar**.
5. Return to **Bookmarks** and **select** your new **Downtown Vancouver** bookmark.

#### Display Order
The **Layer Order** in the **Table of Contents** determines the order of display in your **Data Frame**, when it is in the "List by Drawing Order" mode. Note that you can also display your **Contents** as “List by Source”.
1. If you haven’t already, change your **Table of Contents** view from “List by Source” to “List by Drawing Order” using the **View** buttons at the top of the **Table of Contents**.
2. **Click and Drag** the :exclamation:XXXX layer to the top of the **Table of Contents**. Note that the other layers in your **Map Document** are now obscured.

## WORKING WITH LAYERS

#### Layer Visibility
The **Table of Contents** also controls Layer Visibility.  You can toggle the Layer Visibility using the checkbox next to each Layer in the Table of Contents.
- Use the Visibility Checkbox next to the XXXX:exclamation: Layer to turn off the visibility of the layer and reveal the other layers again.

#### Feature Layer Tab
Almost everything you might want to do with a layer can be done under the **Feature Layer** tabs.  There are often short-cuts to do these tasks also, but the **Feature Layer** tab can help you first find ways to work with layers.  

_(Note: Almost every sub-command can be found 2 ways; as an icon on the feature tab, or by right-click and ‘properties’ options in the contents.)_

1. Click onto the Street Trees layer. The **Feature Layer** set (orange) appears at the top of the screen. There are 3 tabs under the **Feature Layer** set: **Appearance**, **Labeling**, and **Data**.
2. Go to the **Data** tab. The first block has a **Definition Query Tool**. The second block has a **Table Tool** with a button to open the ‘_Attribute Table_’.  

### Layer Attributes
The most basic method of analysis in GIS is selection and sub-setting of data by attribute values. Now that the Street Trees layer is visible again, we can begin to address the fact that this layer is a bit overpopulated for our purposes. Let us say we are interested in visualizing a specific subset of trees. First, we need to see if the data necessary to do this exists in our dataset.

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
