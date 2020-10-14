---
layout: default
title: Symbology
nav_order: 6
parent: Working with Layers
---

### Symbology
Now we have two tree layers to work with, and would like to distinguish them from one another visually.

1. Highlight the new **largeDiameter** layer in the **Contents** pane and on the **Menu Bar** at the top of the screen, click on **Appearance**.
2. Click on the dropdown arrow under the **Symbology** option and select **Graduated Colors**.

[Graduated color](https://pro.arcgis.com/en/pro-app/help/mapping/layer-properties/graduated-colors.htm) symbology is used to show a quantitative difference between mapped features by varying the color of symbols.

3. Select **diameter** for the **Field**.
4. Choose **Geometric Interval** as the **Method** and accept the default 5 **Classes**.

**Geometric Interval** is one [data classification method](https://pro.arcgis.com/en/pro-app/help/mapping/layer-properties/data-classification-methods.htm)

We chose this classification method because it accomodates the the extremities of our dataset.

5. Select the **Oranges (Continuous) Color scheme**.
6. Using the same method, change the symbol for the original **Street Trees** layer to **Unique Values** using the **Neighbourhood** field.
7. Use the **Circle 1** symbol with a size of **2 points** and choose a different **Color Scheme**.
8. Save the map by clicking on the save icon in the upper left of the map.

In the example below, using the symbology settings specified above, the neighbourhoods are clearly delineated.
![treesNeigh.jpg](https://raw.githubusercontent.com/fiddleHeads/intro-to-arcgis-pro/master/content/images/treesNeighb.jpg)

In the next section, we'll learn how to apply labels to certain features.
