---
layout: default
title: Labels
nav_order: 7
parent: Working with Layers
---

### Labels
Another property of the layers in our **Map Document** that we might want to enable is the labeling of features.  This can be accomplished, based upon an attribute value for each of the features. In many cases, this might be the name, or some other identifying attribute of the feature, but in some cases it might be a quantitative value associated with the features. It is even possible to use Arcade or SQL scripting to assemble labels from several attributes and text elements. In this example, we will label only the trees from the **largeDiameter** layer which also have a tree height greater than or equal to 8. In order to label only selected features, we'll create another layer based on a selection.

1. Under the **Map** tab at the top of the screen, click on **Select by Attributes** to create an expression.
Set the following parameters:

-	Input Rows: largeDiameter
- Selection type: New Selection
- Click: New Expression

For the Expression, Where:

-	Field: diameter
- is equal to (this is the default)
- click the dropdown in the third box of the clause to see the range of values

1. Right-Click on the **largeDiameter** layer and select **Label**, or go to **Feature Layer > Labeling > Layer** and click on the **Label** icon. Note that this turns on labels for all features and that ArcGIS selects a field containing names, by default. Because there are so many visible features in this layer, this creates an unreadable labeling scheme. To remedy this, we will limit labeling to the largest cities in the Major Cities Layer._
2. _Right-click on the XXXX Layer and select Labeling Properties or on the Label Class, select the SQL button._
3. In the **Label Class** window, click on the **SQL Query…** button.
4. Click on **Add Clause**.
5. :exclamation:Click Apply a SELECT argument as where the Field POP_RANK “is Equal” Values: 1.
6. Click **Add**.
7. Go to the **Symbol Tab** and click on the **General** button (and “A” with the Paintbrush) **> Expand Appearance** and change the **Label Size** to 12 points, then click **Apply**.
