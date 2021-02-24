---
layout: default
title: Working with Layers
nav_order: 7
has_children: true
---

## WORKING WITH LAYERS

#### Layer Visibility
The **Table of Contents** also controls Layer Visibility.  You can toggle the Layer Visibility using the checkbox next to each Layer in the Table of Contents.
- Use the Visibility Checkbox next to the **streetTrees** layer to turn off the visibility of the layer and reveal the other layers again.

#### Feature Layer Tab
Almost everything you might want to do with a layer can be done under the **Feature Layer** tabs.  There are often short-cuts to do these tasks also, but the **Feature Layer** tab can help you first find ways to work with layers.  

_(Note: Almost every sub-command can be found 2 ways; as an icon on the feature tab, or by right-click and ‘properties’ options in the contents.)_

*1*{: .circle .circle-blue} Click on the Street Trees layer. The **Feature Layer** set (orange) appears at the top of the screen. There are 3 tabs under the **Feature Layer** set: **Appearance**, **Labeling**, and **Data**.

*2*{: .circle .circle-blue} Go to the **Data** tab. The first block has a **Definition Query Tool**. The second block has a **Table Tool** with a button to open the ‘_Attribute Table_’. 

### Field Names
There are certain [rules](https://support.esri.com/en/technical-article/000005588) associated with field names, but the alias for a field name has more flexibility. Before we start exploring the attributes of the data, we'll add aliases to the field names to make them easier to understand and work with.

*1*{: .circle .circle-blue} **Right-click** on the **Street Trees** layer and select **Attribute Table** to open it.

*2*{: .circle .circle-blue} There are two ways to change field aliases. Under the **View** tab, select **Fields**. Alternatively, right-click on one of the column names in the attribute table and select **Fields**.

*3*{: .circle .circle-blue} From the newly opened table containing only Field Name information, click on **std_street** under the **Alias** column. You can see that by clicking in that field it becomes editable. 

We can learn more about what the fields stand for by examining the [data schema](https://opendata.vancouver.ca/explore/dataset/street-trees/information/?disjunctive.species_name&disjunctive.common_name&disjunctive.height_range_id) provided on the City of Vancouver Open Data Portal. 
Scroll down and then expand the data schema to see what the different fields represent.

*4*{: .circle .circle-blue} Change the aliases according to the following table.

| Original  | Change to |
| ------------- | ------------- |
| std_street  | Street site |
| on_street  | Street name |
| species_na  | Species name |
| diameter  | Diameter |
| date_plant  | Date planted |
| root_barri  | Root barrier |
| street_sid  | Street side |
| genus_name  | Genus name |
| neighbourh  | Neighbourhood |
| assigned  | Assigned |
| civic_numb  | Street address |
| plant_area  | Plant area |
| curb  | Curb |
| tree_id  | Tree ID |
| common_nam  | Common name |
| height_ran  | Height range |
| on_street_  | Block |
| cultivar_n  | Cultivar name |

*5*{: .circle .circle-blue} Save your edits by clicking on **Save** under the Fields tab at the top of the map.

### Layer Attributes
The most basic method of analysis in GIS is selection and sub-setting of data by attribute values. Now that the Street Trees layer is visible again, we can begin to address the fact that this layer is a bit overpopulated for our purposes. Let us say we are interested in visualizing trees by the diameter of the treet and the neighbourhood they were planted in. First, we need to see if the data necessary to do this exists in our dataset.

*1*{: .circle .circle-blue} **Right-Click** on the **Street Trees** layer and select **Attribute Table** to open the **Attribute Table** of the layer.

*2*{: .circle .circle-blue} **Click**, **drag** and **move** around the resulting table window. You can dock it again using the **Docking Square**.

*3*{: .circle .circle-blue} **Right-click** on the column name **diameter** and select Sort Descending.

*4*{: .circle .circle-blue} **Scroll** down through the attribute table to examine the relationship among the **diameter**, **genus_name**, and **neighbourh** variables.

#### Select by Attributes
It's difficult to understand the range of dates by scrolling down in such a large dataset, so we'll use the Select by Attributes tool to first explore the dates available and then to select a subset of trees with larger diameters.

*1*{: .circle .circle-blue} On the **Map Tab**, go to the **Selection Tool**.

*2*{: .circle .circle-blue} Find and click on the **Select by Attributes** button.

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

*1*{: .circle .circle-blue} Click on the “**Run**” button at the bottom of geoprocessing window to apply the selection to your **Street Trees** layer.

*2*{: .circle .circle-blue} Scroll through the attribute table and note the records that are selected.

*3*{: .circle .circle-blue} You can observe that the selection from the attribute table is also reflected in the map.

Notice that the selection looks more manageable that the full dataset.  Now you will export this selection as a new Shapefile, and bring it back into the map as a new layer. As you do this, you will take advantage of a sort of “universal task" in ArcGIS Pro. Anytime you have selected a subset of one of your data layers ArcGIS Pro will only act on that subset while it is active. This means that geoprocessing, attribute calculations, data exports, etc., act as if the active selection is the whole of the dataset. This can come in quite handy.

*1*{: .circle .circle-blue} Right-click on the **Street Trees** layer in the **Contents** and select **Data > Export Features** …
(_The option is also available under the **Feature Layer** set **> Data Tab > Export** block_).

*2*{: .circle .circle-blue} In the **Export Features** window click on the **Browse** button to save the feature class into the **workshop.gdb** to save as **largeDiameter**. _Note that the default is to save the new feature into the ***same*** database as the previous feature_.

*3*{: .circle .circle-blue} Click **Run**.

![exportData.jpg](https://raw.githubusercontent.com/fiddleHeads/intro-to-arcgis-pro/master/content/images/exportData.jpg)

Uncheck the original Street_Trees layer and close the attribute table.

Next we'll symbolize these two layers.
