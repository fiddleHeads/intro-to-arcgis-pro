---
layout: default
title: Add Data
nav_order: 8
parent: Working with Layers
---

## NEEDS REWORKING

### Adding Data
Let's see if we can find population data for Vancouver that will help us analyze how many trees per capita there are in each neighbourhood in the city.
The City of Vancouver [Open Data Portal](https://opendata.vancouver.ca/pages/home/) provides [2016 Census Area Profile](https://opendata.vancouver.ca/explore/dataset/census-local-area-profiles-2016/information/) data from [Statistics Canada](https://www.statcan.gc.ca/eng/start).

Unfortunately, the data is not in GIS format but provided as a spreadsheet with much more information than we need formatted in a way that is not friendly to a GIS. 

So the spreadsheet has been culled and reformatted to only represent total population per neighbourhood.

***can I add some data here that would show douglas firs per capita?***

Now lets add some additional data to our **Map Document**. 
1.  From the **Add Data** dropdown, click on **Data**. 
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

