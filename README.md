# Intro to ArcGIS Pro
### UBC Library Research Commons
   
Link to workshop: https://fiddleheads.github.io/intro-to-arcgis-pro/

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
1. **Right-Click** on the **Street Trees** layer and select **Open Attribute Table** to open the **Attribute Table** of the layer.
2. **Click**, **drag** and **move** around the resulting table window. You can dock it again using the **Docking Square**.
3. **Scroll** to the right until you can see the **POP**, **POP_RANK** and **POP_CLASS** :exclamation: attribute fields.
4. **Right-click** on the **POP** field header and select Sort Descending.
5. **Scroll** down through the attribute table to examine the relationship between these three variables.

#### Select by Attributes
What we would like to do is select all of the trees in this dataset that of a specific type. This can be accomplished using either of two variables, but we will use the **NAME** :exclamation: variable because most people know trees by this name.  
1. On the **Map Tab**, go to the **Selection Tool**.
2. Find and click on the **Select by Attributes** button.

Pin the Geoprocessing Pane and set the following parameters:

-	Layer Name: Cities
- Selection type: New Selection
- Click: Add Clause

On the Expression:

-	Field: Pop_Rank
- is Less Than or Equal
- Value: 2

1. Click **Add**.
2. Click on the “**Run**” button at the bottom of geoprocessing window to apply the selection to your **Street Trees** layer.
3. Scroll through the attribute table and note the records that are selected.
4. You can observe that the selection from the attribute table is also reflected in the map.

Notice that the selection looks more manageable that the full dataset.  Now you will export this selection as a new Shapefile, and bring it back into the map as a new layer. As you do this, you will take advantage of a sort of “universal task" in ArcGIS Pro. Anytime you have selected a subset of one of your data layers ArcGIS Pro will only act on that subset while it is active. This means that geoprocessing, attribute calculations, data exports, etc., act as if the active selection is the whole of the dataset. This can come in quite handy.

1. Right-click on the **Street Trees** layer in the **Contents** and select **Data > Export Features** …
(_The option is also available under the **Feature Layer** set **> Data Tab > Export** block_).
2. In the **Copy Features** window click on the **Browse** button to save the feature class into the XXXX:exclamation:.gdb to save as Trees_XXXX:exclamation:. _Note that the default is to save the new feature into the ***same*** database as the previous feature_.
3. Click **Run**.
4. Right-click on the original Street_Trees layer and select **Remove**.

### Symbology
Now we have two classes of STREET_TREES :exclamation: to work with, and would like to distinguish them from one another visually.

1. Right-Click on the new Trees_XXXX :exclamation: layer and on the **Menu Bar** go to **Appearance > Symbology**.
2. Click on the **Symbology** option and select **Unique Values**.
3. Change the **Value Field** to **XXXX** :exclamation:.
4. Click on the **More** option and uncheck the **Show all other values** item.
5. Click **Symbols (Circles)** to open the **Format Point Symbol**.
6. On the resulting **Symbol Selector Gallery** select **Circle 1**.
7. Beside the **Gallery** options, click **Properties** and set its size to **4 points**. Click apply and use the **Go Back** arrow to return to the **Symbology Tab**.
8. Using the same method, change the symbol for the “XXXX” :exclamation: item to **Circle 1** with a size of **10 points**.
9. Go Back to the **Contents Panel** (Tabbed at the bottom).
10.	Click **Save**.

### Labels
Another property of the layers in our **Map Document** that we might want to enable is the labeling of features.  This can be accomplished, based upon an attribute value for each of the features. In many cases, this might be the name, or some other identifying attribute of the feature, but in some cases it might be a quantitative value associated with the features. It is even possible to use Visual Basic scripting to assemble labels from several attributes and text elements. In this example, we will label only the trees with a XXXX value of XXXX :exclamation:.

1.	_Right-Click on the XXXX :exclamation: layer and select **Label**, or go to **Feature Layer > Labeling > Layer** and click on the **Label** icon. Note that this turns on labels for all features and that ArcGIS selects a field containing names, by default. Because there are so many visible features in this layer, this creates an unreadable labeling scheme. To remedy this, we will limit labeling to the largest cities in the Major Cities Layer._
2. _Right-click on the XXXX Layer and select Labeling Properties or on the Label Class, select the SQL button._
3. In the **Label Class** window, click on the **SQL Query…** button.
4. Click on **Add Clause**.
5. :exclamation:Click Apply a SELECT argument as where the Field POP_RANK “is Equal” Values: 1.
6. Click **Add**.
7. Go to the **Symbol Tab** and click on the **General** button (and “A” with the Paintbrush) **> Expand Appearance** and change the **Label Size** to 12 points, then click **Apply**.

### Adding Data
***can I add some data here that would show douglas firs per capita?***

Now lets add some additional data to our **Map Document**.
1. In the **Catalog Window**, navigate to the **Intro:exclamation:.gdb**.
2.	Find  the **XXXX Table** and click and drag it to the Map Document.
3.	Now look on the **Contents Pane**, you should see the table under the **Standalone Tables** tab.

### Joining Tables

***Data will need to have population per neighbourhood***
Now we will turn our attention to the XXXX:exclamation: Layer. Ultimately, we would like to visualize the layer based upon population density. However, the attribute table for this layer does not contain data on population.  Fortunately, we added the World Population table in our Map Document with the necessary population attribute.

1. Right-click on the **NeighborhoodPop Table** and select **Open**.
2. Scroll through the attributes and note the **NAME** and **POP** attribute fields. Close the table.
3. Open the attribute table for the **VanNeighborhoods** layer and note that it also has a **NAME** attribute field, but not a **POP** attribute field.  

Since the **NAME** attribute exists in both of these attribute tables, and its values are identical across the two datasets, we can use this attribute as the “**Key Field**” for our table join.

4.	Close the attribute table for the **VanNeighborhoods** Layer.
5.	Right-click on the **NeighborhoodPop** layer and select **Joins and Relates > Add Join…**
6.	Select **NAME** as the **Join Field** for the **XXXX:exclamation:** layer.
7.	If it is not selected automatically, select **NeighborhoodPop** as the table to join to the **VanNeighborhoods** layer, and **NAME** as the join field for this table.
8.	Click **Run** to create the join.
9.	Open the attribute table for the **VanNeighborhoods** layer and note the **POP** attribute (along with all other attributes from the **NeighborhoodPop** table).

### Definition Queries
***need to edit this entire section***

You may have noticed that many of the features in the World_Countries Layer had values of -99999 for the POP2007 attribute.  This normally indicates NODATA for the particular feature in demographic datasets.  In this case, we would like to exclude this value from our Map Document.  We could use the method used to subset the Cities layer earlier in the tutorial, but this time we will use another method called Definition Query.  Definition Queries “define” a dataset, based upon a SQL Query, like the ones we have used to create the selection by attributes and the labeling class.  In this case, the Definition Query “defines” a subset of the data layer that ArcMap treats as the entirety of the dataset.  It does not, however, require creating a new dataset (preventing redundancy in data storage) and does not alter the dataset being referenced, only our view of it in ArcGIS.

1. Right-click the World_Countries layer and open its Properties.
2. Click on the Definition Query tab.
3. Click on the Add Clause Button and create a SELECT Argument as follows:
**POP2007 does Not include the -99999**
4. Click Add
5. Click OK to apply the Definition Query.
6. Re-open the Attribute Table for the World_Countries Layer and note that the POP2007 Field no longer contains records with -99999 as a value.  

Because most of the features with this value are lesser countries (in terms of area), it may not be apparent that the corresponding geographic features have also been removed from the Layer, as well.

### Symbology - Graduated Colours
***need to edit entire section***

We can now use the POP2007 attribute to visualize population density. Even though the POP2007 variable is a raw counts variable, we can use the Symbology Tabs Normalization capability to divide the POP2007 variable by the area of the features to create the density value on-the-fly.

1.	Open the Properties for the World_Countries Layer and click on the Symbology Tab.
2.	Select Graduated Colors and set the FIELD to the POP2007 variable.
3.	Set the Normalization Field to the SQMI field.
4.	Set the Classification Method to Quantiles with 5 Classes.
5.	Select a Color Ramp.
6.	Go Back to your Contents Panel (No need to click apply)

_Note: When selecting your color ramp, be careful about selecting anything other than monochrome color ramps. This is because you want your map to “read well” in grayscale. In some of the 2-3 color ramps, the Intensity value of the colors at each end of the spectrum is the same, so that they produce identical grayscale values when converted, Xeroxed or printed in black & white._

### Adding "Cloud" Data
***need to edit entire section***

Often, you will want to provide a cartographic basemap for your data in order to give it geographic context.  Cartographic design can be quite time consuming.  Fortunately, ArcGIS Pro  leverages “Cloud” technologies to make a wide variety of pre-designed cartographic basemap layer available over the internet for use in your Map document.
1.	On the **Map Menu > Layer** tools, go Basemap.
2.	In the resulting window, select the “XXXX:exclamation:” basemap.
3.	Uncheck the **Reference Layer** that is added to the top of the **Table of Contents**.
4.	Wait for the basemap to render and save your work.


## EXPORTING AND SAVING
***Add some content about this is what you do once you want to export your map as an image***
### Layout Mode
1. On the Insert Tab > Project Toolbar, click New Layout.
2. In the resulting window, select Letter Landscape.  

_Note that a new Layout ‘window’ tab has opened next to the Map tab. You can switch back and forth._

### The Map Frame
Note that the Layout Toolbar (Insert Tab) is now active and that many of the tools on this toolbar look similar to those on the Tools Toolbar, with one very important difference.  Now that you are in Layout Mode, your need to add a Map Frame to a piece of paper.

1.	On the Insert Tab > Map Frames Toolbar, click Map Frame.
2.	In the resulting window, select Default, but notice the Europe and Asia Bookmark is there.   

### Layout Navigation
Using the Layout Tab that now activates, take a moment to explore the Layout Toolbar.
Notice how the Navigate options behavior differ from the Navigate on Map Mode.

#### Resizing the Data Frame
Because the map is not the same proportions as the page, the border is larger than the frame; we will want to alter the size of the Map Frame (not the Page Size) to the size we desire for our final image.

1. Click on the Map Frame and notice that a Map Frame Format tab activates
2.	Click on the Size and Position Toolbar and set the Frame Size as Width to 8.3 inches and the Height to 5 inches.
3.	Press Align Center and Align Middle, to center the map on the page. (If not active, make sure the Align to Page is checked)
4.	On the Frame Tab, go to Current Selection and change the Map Frame to Border
5.	Change the border weight to 4 points.  
6.	Assign a Gap of 10 pts for both the X and Y tabs.
7.	On the Layout Toolbar, go to Bookmarks and select your Europe & Asia bookmark
8.	Click on the Activate Tool (Layout Tab >Map Toolbars) or   right-click  on the map itself and select “Activate”
Now you can move the map around, pan and zoom in and out until you get the map the way you want to see it.
9.	Go back to the  Layout Tab, under Activated Map Frame  and select Close Activation
10.	Then, at the top of the page, under the Map Frame set, go to Layout. Now the Navigation tools show a different set of options and if you zoom, you’ll zoom in and out of the page itself.


#### Adding Map Elements

### Map Legend
1.	Go to Insert>Legend and click on the Map Layout
2.	On Contents, list the Map Elements by Drawing
3.	Expand the Legend, and select Major_Cities and drag it to the top.
4.	With the Legend selected, on the Format Set, go to Format Tab,
5.	Change the Current Selection from Legend to Border and add a Border.
6.	Repeat the same procedure to set a Background (white is a good choice).
7.	Return to the Map Tab
8.	Click once on the Major_Cities Layer, wait a few seconds, and then click again to highlight the Layer Name for Editing.  Rename the Layer “Major Cities” removing the underscore, and hit the Enter key to commit the change.
_Note that the change you have made to the name of the Layer is also reflected in the Legend (Layout)._
9.	Make changes to the other Text Elements of your Layers so that your Legend contains properly formatted and reasonable text descriptions and labels.

### Scale Bar
1.	Go back to the Layout View and go to to Insert>Scale Bar
2.	On the Scale Bar Format > Symbol, Select Scale Line 1
3.	Go to the Design Tab and set the Number of Divisions to 1 and the Subdivisions to 1.
4.	Set the Division Units to Miles.
5.	Click on the Numbers and Marks Tab.
6.	Set the Number Frequencies to “Divisions”
7.	Use the Handles to resize and reposition the Scale Bar.

### Export Your Map
1.	Save your Work.
2.	On the Share Tab, go to the Export Tool and click the Layout button…
3.	Browse to the Intro to ArcGIS Pro folder and save the file as: World_Population
4.	Change the Save as type to PNG(*.png)
5.	Change the Resolution to 200 dpi
6.	Click Export.
7.	Browse to the Workshop Folder and double click on the EX01_World.png file to view it in the default image viewer.

## What's Next?
### Thanks - Stanford Geospatial Center
