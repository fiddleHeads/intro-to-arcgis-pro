---
layout: default
title: Starting a Project
nav_order: 3
---

## STARTING A PROJECT
### Map Projects

So what exactly is an **ArcGIS Pro Project**? When you first add a blank map and begin "_adding_" data and creating different symbologies, labeling schemes, etc., you are modifying a Map Project. The word _adding_ is emphasized because you are not actually adding data. Instead, you are _linking_ data using file paths. The reason for this is because often times GIS data is several megabytes or even gigabytes in filesize. Having all of that data displayed in your map project would be impractical and taxing on your computer. So, the project doesn't actually contain the data, but only links to it. Map Projects are then configured with styles, symbologies, labels, etc.

Go to **Project > Open** and open the map document called **Intro**. This file will be the only file with the **.aprx** extension. Notice that the home folder in Catalog has changed to the one used for the **.aprx** file.

#### Fixing Broken Links

You'll see that your layers (in your **Contents Pane**) have a small :exclamation: next to them. This means that you're experiencing the **Broken Link** issue - which is VERY common when working in GIS with layers and the paths pointing to them. You'll need to fix them to continue.

![brokenLink.jpg](https://raw.githubusercontent.com/fiddleHeads/intro-to-arcgis-pro/master/content/images/brokenLink.jpg)

1. Click on the red :exclamation: next to the street trees layer in the **Contents** pane.
2. Navigate to the Intro.gdb of the tutorial dataset and select the Shapefile that corresponds to the layer you clicked and select **OK**.

Since all your layers are in the same directory, all of your layers should now be repaired. It's generally good practice to have your data organized logically, which will help to fix the inevitable broken link issue.
