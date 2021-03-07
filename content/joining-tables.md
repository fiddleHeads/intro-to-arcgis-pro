---
layout: default
title: Joining Tables
nav_order: 8
parent: Working with Layers
---

### JOINING TABLES
Joining data using a common attribute is an important and useful function in GIS. There are two ways of joinng data in a GIS, joining via an attribute from a table or joining data spatially based on how it intersects in space. You can also relate data from one table to another in order to understand how they are related. Rather than appending data from one table into another, a relate allows you to interact with the data between the two tables. Find out more about joins and relates in the [ArcGIS Pro documentation](https://pro.arcgis.com/en/pro-app/latest/help/data/tables/joins-and-relates.htm).

We will perform an attribute join between our two spatial data layers in order to have all of the language data for Vancouver in one table.

### Renaming Fields

First we need to rename the generic fieldnames such as **VALUE0** with the appropriate language names. Make sure the attribute tables for **househldPopMotherTong_joinTbl** and **variable_names** are open.

*1*{: .circle .circle-blue} Right-click on the attribute table name for **househldPopMotherTong_joinTbl** and select **New Horizontal Tab Group**.

This will stack the two tables on top of one another to make them easier to view simultaneously.

*2*{: .circle .circle-blue} Right-click on the **VALUE0** fieldname and select **Fields** to open up the **Fields View**.

*3*{: .circle .circle-blue} Referencing the information from the **variable_names** table, double-click in the **VALUE0** field under the **Field Name** column and change it to **aborigLangs** and the **Alias** to **Aboriginal Languages**.

Field names have character limits and cannot have spaces, but Aliases can.

*4*{: .circle .circle-blue} Change the other three field names and alias for values 1, 2, and 3.

| Original  | New Field Name | Alias |
| ------------- | ------------- |
| VALUE1  | Czech | Czech |
| VALUE2  | otherLangs | Other Languages |
| VALUE3  | Somali | Somali |

*5*{: .circle .circle-blue} Click on **Save** under the **Fields** tab at the top of the map.

You should see the changes you made reflected in the **househldPopMotherTong_joinTbl** attribute table. 

### Join Data
The next step is to join this dataset to the **househldPopMotherTong_joinToThis** dataset in order to have all of the language for Vancouver in one table, which will make the data easier to manage.

*1*{: .circle .circle-blue} Examine the fieldnames in the attribute tables of these two datasets and see if you can find a common field to perform the join on.

Joining two tables together requires that they have a field in common, and this is often an identifier field. In our two tables, the **spatial_id** field is the identifier for Census tracts, and this is the field we'll use to join our two datasets.

*2*{: .circle .circle-blue} Close any open tables and save your map in the upper left.

*3*{: .circle .circle-blue} From the **Contents** panel on the lfet, right-click on the **househldPopMotherTong_joinToThis** layer and select **Joins and Relates** and then **Add Join**.

*3*{: .circle .circle-blue}	Select **spatial_id** as the **Input Join Field** (there may be a warning indicated by an exclamation point in a triangle about indexing. We can ignore that for this join).

*4*{: .circle .circle-blue}If it is not selected automatically, select **househldPopMotherTong_joinTbl** as the **Join Table** and **spatial_id* as the **Join Table Field** for this table.

*5*{: .circle .circle-blue} Click **OK** to create the join.

*6*{: .circle .circle-blue} Open the attribute table for the **househldPopMotherTong_joinToThis** layer and scroll all the way to the right to see whether this table has the new fields you added.

### Export Data

Note that this is a temporary join and has not altered the underlying dataset. In order to ensure this join is permanent, we'll create a new [feature class](https://pro.arcgis.com/en/pro-app/latest/help/data/geodatabases/overview/feature-class-basics.htm).

*1*{: .circle .circle-blue} Close the attribute table and right-click on the **househldPopMotherTong_joinToThis** layer in the **Contents** pane and select **Data** > **Export Features**. 

*2*{: .circle .circle-blue} Click the **Browse** button to navigate to the **Intro.gdb**.

*3*{: .circle .circle-blue} Use **househldPopMotherTong** for the **Output Name** and click **OK** to create a new feature class, which should be added to your map when the process is completed.

*4*{: .circle .circle-blue} Unjoin the table from the **househldPopMotherTong_joinToThis** layer by right-clicking on this layer in the **Contents** pane and selecting **Joins and Relates** > **Remove Join**.

*5*{: .circle .circle-blue} Uncheck other layers and open the attribute table for the new feature class you just created.

### Delete Fields

Now that we have a complete dataset for the language data, we can delete extraneous fields, such as all the duplicate **spatial_id** and **name** fields.

*1*{: .circle .circle-blue} Under the **Data** tab at the top of the map, click on **Fields**.

This is another example of how there is more than one way to perform a task in ArcGIS Pro and most GIS software.

*2*{: .circle .circle-blue} From the **Fields View**, right-click on the gray tab on the far left of the first **FID** you come to and select **Delete**. Do the same for the **spatial_id** and **name** fields directly below it. They'll appear with strikethrough text.

*3*{: .circle .circle-blue} Scroll down through the whole table and delete any **FID** and **spatial_id** and name fields, except those at the very top of the table. You can also delete by left-clicking on the gray tab of the far left of the next **FID** field, holding down **SHIFT** and clicking the gray tab on the far left of the **name** field two rows below.

This will select three rows which you can then delete together. 

*4*{: .circle .circle-blue} There may be one **OBJECTID** field toward the bottom which you can also delete, along with extraneous **Shape_length** and **Shape_Area** fields. Any fields which are greyed out you will be unable to delete and are necessary for establishing the geometry of the layer.

*5*{: .circle .circle-blue} Click **Save** at the top of the map under the **Fields** tab and close the **Fields View** and save your map.

*6*{: .circle .circle-blue} If you look at your attribute table now, you'll see that it has been cleaned up and is easier to understand.

### Exercise On Your Own
We want to join one more dataset to our table which contains attributes for the total population by Census tract, also downloaded from SimplyAnalytics accessed through the UBC library. This will allow us to further analyze the language data we have.

*1*{: .circle .circle-blue} Click the **Add Data** dropdown arrow from the **Map** tab and select **Data**, the first option.

*2*{: .circle .circle-blue} Navigate to the **Intro.gdb** and add the **totalPopTract** feature class to your map.

*3*{: .circle .circle-blue} Using the same steps as above, join the **totalPopTract** table to the **househldPopMotherTong** layer using **spatial_id** and then export the data to a new feature class and call it **popMotherTongTractVan**.

Each time I create a new dataset, I want to try and name it something that identifies what it is. Data management in GIS can be unruly, and having a good file naming system is essential.

*4*{: .circle .circle-blue} Delete any extraneous fields that got added toward the bottom of the attribute table in the **Fields View**.

*5*{: .circle .circle-blue} Rename the **VALUE0** Alias field to **Total Pop**, save your edits, and exit the **Fields View**.

In the next section, now that we have a complete dataset, we'll further analyze this data.
