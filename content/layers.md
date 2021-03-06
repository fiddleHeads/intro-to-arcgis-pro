---
layout: default
title: Working with Layers
nav_order: 7
has_children: true
---

### WORKING WITH LAYERS

### Layer Visibility
The **Table of Contents** also controls Layer Visibility.  You can toggle the Layer Visibility using the checkbox next to each Layer in the Table of Contents.
- Use the Visibility Checkbox next to the **househldPopMotherTong_joinToThis** layer to turn on and off the visibility of the layer and any other layers in the map.

### Feature Layer Tab
Almost everything you might want to do with a layer can be done under the **Feature Layer** tabs.  There are often short-cuts to do these tasks also, but the **Feature Layer** tab can help you first find ways to work with layers.  

_(Note: Almost every sub-command can be found 2 ways; as an icon on the feature tab, or by right-click and ‘properties’ options in the contents.)_

The data we'll be working with represents [Household Population by Mother Tongue](https://www12.statcan.gc.ca/census-recensement/2016/ref/dict/pop095-eng.cfm) from the 2016 Census. It was retrieved from SimplyAnalytics, one of the [databases](https://resources.library.ubc.ca/?action=resources&rpaction=select&search=simplyanalytics&searchtype=keywords&format=) available from the UBC library. A mother tongue language is a person's first language. We will use data on household population by mother tongue language aggregated by [census subdivision](https://www150.statcan.gc.ca/n1/pub/92-195-x/2011001/geo/csd-sdr/csd-sdr-eng.htm).

In this workshop, we will analyze this data to understand the spatial distribution of linguistic diversity in Vancouver. Although another Census variable, language spoken at home, could also be used, for the purposes of our analysis, we'll use houshold population by mother tongue to visualize where languages are spoken across the city.


*1*{: .circle .circle-blue} Click on the **househldPopMotherTong_joinToThis** layer. The **Feature Layer** set (orange) appears at the top of the screen. There are 3 tabs under the **Feature Layer** set: **Appearance**, **Labeling**, and **Data**.

*2*{: .circle .circle-blue} Go to the **Data** tab. The first block has a **Definition Query Tool**. The second block has a **Table Tool** with a button to open the ‘_Attribute Table_’. Click on this to open the attribute table.

You can also open the attribute table of a layer by right-clicking on that layer in the **Contents** panel and selecting **Attribute Table** to open it.

*3*{: .circle .circle-blue} Scroll all the way to right of the attribute table and notice the fieldnames and data present.

Do you see any replication? What do you think the numbers represent?

Every feature you see in a map has a backend database associated with it where information is stored, called the [attribute table](http://wiki.gis.com/wiki/index.php/Attribute_table), which appears much as a spreadsheet. The most basic method of analysis in GIS is selection and sub-setting of data by attribute values.

This dataset had to be downloaded as multiple datasets. All but one remaining dataset have already been joined together.

*4*{: .circle .circle-blue} **Right-Click** on the **househldPopMotherTong_joinTbl** layer and select **Attribute Table** to open it.

Do you recognize any fieldnames from the attribute table of the first layer we opened? What do you think **VALUE0, VALUE1**, etc. represent? 

Notice there is another layer listed under **Standalone Tables** called **variable_names**.

*5*{: .circle .circle-blue} **Right-Click** on the **variable_names** layer and select **Attribute Table** to open it.

Notice there is no way to view **variable_names**. It only exists as a table. Each data download for the language data came with both a spatial feature layer and an accompanying table. The information in the table was used to rename the **VALUE** fields in the spatial feature layer with meaningful information. When bringing Census data into a GIS, it often requires additional manipulation before it can be used or understood.

*6*{: .circle .circle-blue} Expand the width of **Field1** to view all of the information. 

You'll notice that these values represent four additional languages which are not yet present in the **househldPopMotherTong_joinToThis** layer.

In the next section, we'll rename the **VALUE** fields in the **househldPopMotherTong_joinTbl** layer and then join this to the **househldPopMotherTong_joinToThis** layer.
