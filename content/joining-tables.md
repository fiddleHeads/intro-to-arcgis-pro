---
layout: default
title: Joining Tables
nav_order: 8
parent: Working with Layers
---

# Joining Tables
Joining data using a common attribute is an important and useful function in GIS. There are two ways of joinng data in a GIS, joining via an attribute from a table or joining data spatially based on how it intersects in space. You can also relate data from one table to another in order to understand how they are related. Rather than appending data from one table into another, a relate allows you to interact with the data between the two tables. Find out more about joins and relates in the [ArcGIS Pro documentation](https://pro.arcgis.com/en/pro-app/latest/help/data/tables/joins-and-relates.htm).

We will perform an attribute join between our two spatial data layers in order to have all of the language data for Vancouver in one table.

### Renaming Fields

First we need to rename the generic fieldnames such as **VALUE0** with the appropriate language names. Make sure the attribute tables for **househldPopMotherTong_joinTbl** and **variable_names** are open.

1{: .circle .circle-blue} Right-click on the attribute table name for **househldPopMotherTong_joinTbl** and select **New Horizontal Tab Group**.

This will stack the two tables on top of one another to make them easier to view simultaneously.

2{: .circle .circle-blue} Right-click on the **VALUE0** fieldname and select **Fields** to open up the **Fields View**.

3{: .circle .circle-blue} Referencing the information from the **variable_names** table, double-click in the **VALUE0** field under the **Field Name** column and change it to **aborigLangs** and the **Alias** to **Aboriginal Languages**.

Field names have character limits and cannot have spaces, but Aliases can.

4{: .circle .circle-blue} Change the other three field names and alias for values 1, 2, and 3.

| Original  | New Field Name | Alias |
| ------------- | ------------- |
| VALUE1  | Czech | Czech |
| VALUE2  | otherLangs | Other Languages |
| VALUE3  | Somali | Somali |

5{: .circle .circle-blue} Click on **Save** under the **Fields** tab at the top of the map.

You should see the changes you made reflected in the **househldPopMotherTong_joinTbl** attribute table. 

6{: .circle .circle-blue} Close any open tables and save your map in the upper left.

### Join Data
The next step is to join this dataset to the **househldPopMotherTong_joinToThis** dataset in order to have all of the language for Vancouver in one table, which will make the data easier to manage.

1{: .circle .circle-blue} From the **Contents** panel on the lfet, right-click on the **househldPopMotherTong_joinToThis** layer and select **Joins and Relates** and then **Add Join**.


2. Scroll through the attributes and note the **Neighbourhood** and **Population** attribute fields. Close the table.
3. Open the attribute table for the **streetTrees** layer and note that it also has a **Neighbourhood** attribute field, but not a **Population** attribute field. Close the table.

Since the **Neighbourhood** attribute exists in both of these attribute tables, and its values are identical across the two datasets, we can use this attribute as the “**Key Field**” for our table join.

4.	Right-click on the attribute table for the **streetTrees** layer in the Table of Contents and select **Joins and Relates > Add Join…**
5.	Select **Neighbourhood** as the **Input Join Field** (there may be a warning indicated by an exclamation point in a triangle about indexing. We can ignore that for this join).
6.	If it is not selected automatically, select **NeighborhoodPop** as the **Join Table** and **Neighbourhood** as the **Join Table Field** for this table.
7.	Click **OK** to create the join.
8.	Open the attribute table for the **streetTrees** layer and note the new **Population** and **Neighbourhood** fields.
