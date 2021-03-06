---
layout: default
title: Maps and Map Properties
nav_order: 6
---


### MAPS AND MAP PROPERTIES
In the **Contents Panel** you should see an item named **Drawing Order**, below which will be a **Map** item, followed by the  2 layers corresponding to the feature classes in your geodatabase. The **Map** item at the top of the Contents Panel represents the **data frame** which contains all of your layers. Click **List By Source** near the top left of the **Contents Panel**.

Note that the layers are organized underneath the path where they are located. If this map document contained links to datasets in other locations, they would be listed under that path or network address.

### Projections and Coordinate Reference Systems
Coordinate systems tell your map how to project the geography of our spherical world, onto a flat screen. The datasets used in this map are actually all in the same projection (UTM Zone 10) though it is not the one currently being used to display the data. In GIS, datasets have their own explicitly defined Projection/Coordinate Systems, while the Map Frame can also have a different Projection/Coordinate System.  

This allows you to add geographic data with different native Coordinate Systems to your map. ArcGIS Pro will treat the Data Frame’s Coordinate System as the Map’s Lingua Franca, projecting (on the fly) all of the new datasets to the Data Frame Projection. While convenient, it comes at a cost: Map Documents that make use of this type of on-the-fly projection render the data in the Data Frame at a much slower rate.  

In addition, disparate Projection/Coordinate Systems can cause major issues and errors when analyzing across layers (i.e. when geoprocessing that requires transfer of attributes across layers).

### Change a Coordinate Reference System
Because of the issues with working with data in different projections in the same data frame, **it is good practice to select a Projection/Coordinate system that is suitable for your particular analysis and scale, and project all of your data to the same**. The [UTM Zone 10 projection](https://www.nrcan.gc.ca/earth-sciences/geography/topographic-information/maps/utm-grid-map-projections/utm-grid-universal-transverse-mercator-projection/9779) is an appropriate one to use for the City of Vancouver. To change the coordinate system of the underlying map:

*1*{: .circle .circle-blue}	**Right-click** on the **Map Item** at the top of the **Contents** and select **Properties**…

*2*{: .circle .circle-blue}	**Click** on the **Coordinate System Tab** and expand the **Layers Folder** in the “**Select a Coordinate System:**” panel.

*3*{: .circle .circle-blue}	**Expand** the **Layers Folder** and **select** the **NAD 1983 (2011) UTM Zone 10N Projection** file. **Click OK**.

*4*{: .circle .circle-blue}	**Click Save**

(Auto-save option is available under Project > Options > Editing > Session)

What you have just done is reassigned the coordinate system of the **Map Frame** to that of the **Street Trees Layer**. The result of this change should be a substantial change to the view on the Map.

### Explore Navigation and Tools in Data Frames
Before we begin to explore the properties of _individual layers_ in the **Map Document**, we will first spend some time getting familiar with the _navigation tools_ in the **Map Document**.  Most of these tools can be found on the **Map Tab: Navigation** toolbar, though some of the more useful ones involve right-clicking context menus of the layers, or using the mouse and mouse wheel (press to Pan, role to zoom).

### Zoom to layer
Sometimes it is very helpful to see the entirety of a layer's extent. To fit the :exclamation:Language Spoken at Home layer into the **Map Frame**:
- Right-click on the :exclamation:Language Spoken at Home layer, in the Contents Panel, and select Zoom to Layer.

### Tools Toolbar
In addition to the **Zoom to Layer** option, the **Tools Toolbar** provides the bulk of the tools for navigation in the **Data Frame**. Most of them are fairly explanatory. Take a moment to explore each of these tools, and how it works.
- The **Full Extent Button** zooms you to the full extent of the layer in your **Contents** with the largest spatial extent.  This can sometimes be problematic if you are working at a local level, but using one or more layers that are global in extent.
- The **Fixed Zoom In** button :exclamation:.
- The **Fixed Zoom Out** button :exclamation:.
- The **Previous Extent** works much like its analogous tool in your web browser, allowing you to step back through previous changes in scale/extent. This tool is particularly useful if you change your **Data Frame** extent inadvertently.

### Basemap
As mentioned earlier, ArcGIS Pro makes it easy to interact with data available on ArcGIS Online, including basemaps. Since we don't have any reference map for the language data we brought into the map, a basemap can help situate where in the world this data is located. 

*1*{: .circle .circle-blue} From the **Map** tab at the top of the map, click the **Basemap** dropdown menu and select the **Light Gray Canvas** basemap, or another one if you prefer. 

You can see that our data covers the city of Vancouver but excludes the UBC campus.

*2*{: .circle .circle-blue} Save your map by clicking the third icon from the left in the upper left of your screen.

### Display Order
The **Layer Order** in the **Table of Contents** determines the order of display in your **Data Frame**, when it is in the "List by Drawing Order" mode. Note that you can also display your **Contents** as “List by Source”.

*1*{: .circle .circle-blue} If you haven’t already, change your **Table of Contents** view from “List by Source” to “List by Drawing Order” using the **View** buttons at the top of the **Table of Contents**.
