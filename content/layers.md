---
layout: default
title: Working with Layers
nav_order: 5
has_children: true
---

## WORKING WITH LAYERS

#### Layer Visibility
The **Table of Contents** also controls Layer Visibility.  You can toggle the Layer Visibility using the checkbox next to each Layer in the Table of Contents.
- Use the Visibility Checkbox next to the **streetTrees** layer to turn off the visibility of the layer and reveal the other layers again.

#### Feature Layer Tab
Almost everything you might want to do with a layer can be done under the **Feature Layer** tabs.  There are often short-cuts to do these tasks also, but the **Feature Layer** tab can help you first find ways to work with layers.  

_(Note: Almost every sub-command can be found 2 ways; as an icon on the feature tab, or by right-click and ‘properties’ options in the contents.)_

1. Click on the Street Trees layer. The **Feature Layer** set (orange) appears at the top of the screen. There are 3 tabs under the **Feature Layer** set: **Appearance**, **Labeling**, and **Data**.
2. Go to the **Data** tab. The first block has a **Definition Query Tool**. The second block has a **Table Tool** with a button to open the ‘_Attribute Table_’.  

### Layer Attributes
The most basic method of analysis in GIS is selection and sub-setting of data by attribute values. Now that the Street Trees layer is visible again, we can begin to address the fact that this layer is a bit overpopulated for our purposes. Let us say we are interested in visualizing trees by the date they were planted and the neighbourhood they were planted in. First, we need to see if the data necessary to do this exists in our dataset.
1. **Right-Click** on the **Street Trees** layer and select **Attribute Table** to open the **Attribute Table** of the layer.
2. **Click**, **drag** and **move** around the resulting table window. You can dock it again using the **Docking Square**.
3. **Right-click** on the column name **diameter** and select Sort Descending.
6. **Scroll** down through the attribute table to examine the relationship among the **diameter**, **genus_name**, and **neighbourh** variables.

#### Select by Attributes
It's difficult to understand the range of dates by scrolling down in such a large dataset, so we'll use the Select by Attributes tool to first explore the dates available and then to select a subset of trees with larger diameters.
1. On the **Map Tab**, go to the **Selection Tool**.
2. Find and click on the **Select by Attributes** button.

Pin the Geoprocessing Pane and set the following parameters:

-	Input Rows: Street Trees
- Selection type: New Selection
- Click: New Expression

For the Expression, Where:

-	Field: diameter
- is equal to (this is the default)
- click the dropdown in the third box of the clause to see the range of values

This is a good example of how you can use the Select by Attributes tool to better view the data before you even make a selection.

![dropdown.jpg](https://raw.githubusercontent.com/fiddleHeads/intro-to-arcgis-pro/master/content/images/dropdown.jpg)

In this dropdown, the dates are sorted by default in order of smallest to largest.

<details>
<summary>What is the largest diameter value in the dataset?</summary>

435
</details>
<br>

Let's return to the **Select by Attributes** query we were building.
For the Expression, Where:

-	Field: diameter
- is greater than or equal to
- '40'

1. Click on the “**Run**” button at the bottom of geoprocessing window to apply the selection to your **Street Trees** layer.
2. Scroll through the attribute table and note the records that are selected.
3. You can observe that the selection from the attribute table is also reflected in the map.

Notice that the selection looks more manageable that the full dataset.  Now you will export this selection as a new Shapefile, and bring it back into the map as a new layer. As you do this, you will take advantage of a sort of “universal task" in ArcGIS Pro. Anytime you have selected a subset of one of your data layers ArcGIS Pro will only act on that subset while it is active. This means that geoprocessing, attribute calculations, data exports, etc., act as if the active selection is the whole of the dataset. This can come in quite handy.

1. Right-click on the **Street Trees** layer in the **Contents** and select **Data > Export Features** …
(_The option is also available under the **Feature Layer** set **> Data Tab > Export** block_).
2. In the **Export Features** window click on the **Browse** button to save the feature class into the **workshop.gdb** to save as **largeDiameter**. _Note that the default is to save the new feature into the ***same*** database as the previous feature_.
3. Click **Run**.
![exportData.jpg](https://raw.githubusercontent.com/fiddleHeads/intro-to-arcgis-pro/master/content/images/exportData.jpg)
4. Uncheck the original Street_Trees layer and close the attribute table.

Next we'll symbolize these two layers.


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
