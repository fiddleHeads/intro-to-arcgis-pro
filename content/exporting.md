---
layout: default
title: Exporting and Saving
nav_order: 14
---

### EXPORTING AND SAVING
It's possible to export a map from ArcGIS Pro as a JPEG, PNG, or PDF. The steps below outline how to do this.

### Layout Mode
*1*{: .circle .circle-blue} On the **Insert** Tab > **Project** Toolbar, click **New Layout**.

*2*{: .circle .circle-blue} In the resulting window, select **Letter Landscape**. 

_Note that a new Layout ‘window’ tab has opened next to the Map tab. You can switch back and forth._

### The Map Frame
Note that the Layout Toolbar (Insert Tab) is now active and that many of the tools on this toolbar look similar to those on the **Tools** Toolbar, with one very important difference.  Now that you are in Layout Mode, you need to add a Map Frame.

*1*{: .circle .circle-blue} On the **Insert** Tab > **Map Frames** Toolbar, click **Map Frame**.

*2*{: .circle .circle-blue} In the resulting window, select **Default** and then drag your cursor into a rectangle across the white part of the Layout window.   

The last view from your map should appear.

### Layout Navigation
Using the Layout Tab that now activates, take a moment to explore the Layout Toolbar.
Notice how the Navigate options behavior differ from the Navigate on Map Mode.

### Resizing the Data Frame
Because the map is not the same proportions as the page, the border is larger than the frame; we will want to alter the size of the Map Frame (not the Page Size) to the size we desire for our final image.

*1*{: .circle .circle-blue} Click on the **Format** tab.

*2*{: .circle .circle-blue} From on the **Size and Position** section, set the **Frame Size  Width** to 10 inches and the **Height** to 7.5 inches.

*3*{: .circle .circle-blue} From the **Arrange** section, select **Align Center** and **Align Middle**, to center the map on the page. (If not active, make sure the **Align to Page** is checked)

*4*{: .circle .circle-blue} Still under the **Format** tab, from the far left **Current Selection**, select **Border** from the dropdown menu.

*5*{: .circle .circle-blue} Change the border **Width** to 4 points.  

*6*{: .circle .circle-blue} Expand the **Current Selection** by clicking the arrow in the lower right and under the **Display** section in the new window, assign a Gap of 10 in for both the X and Y tabs.

*7*{: .circle .circle-blue} From the **Contents** pane, right-click on one of the language layers and select **Zoom to layer**. 

*8*{: .circle .circle-blue} Click on the **Activate** tool (Layout Tab >Map section) or right-click  on the map itself and select “Activate”

Now you can move the map around, pan and zoom in and out until you get the map the way you want to see it.

*9*{: .circle .circle-blue} Click on the **Layout** tab at the top of the map and select **Close Activation**.

*10*{: .circle .circle-blue}	Then, at the top of the page, under the **Map Frame** set, click on **Layout**. Now the Navigation tools show a different set of options and if you zoom, you’ll zoom in and out of the page itself.

### Adding Map Elements

### Map Legend
*1*{: .circle .circle-blue} Go to **Insert>Legend** and click on the Map Layout to set the legend.

*2*{: .circle .circle-blue} In the **Contents** pane, list the Map Elements by **Drawing Order**.

*3*{: .circle .circle-blue} Expand the **Legend** in the **Contents** pane and see that the legend is enabled for all of your layers, even though the only legend appearing on the map is what corresponds to what layer you have checked on.

*4*{: .circle .circle-blue} Select the **Legend** for **Mandarin and Cantonese Languages** and under the **Format** Set, go to **Format** tab.

*5*{: .circle .circle-blue} Change the Current Selection from Legend to Border and add a Border.

6.	Repeat the same procedure to set a Background (white is a good choice).
7.	Return to the Map Tab
8.	Click once on the Major_Cities Layer, wait a few seconds, and then click again to highlight the Layer Name for Editing.  Rename the Layer “Major Cities” removing the underscore, and hit the Enter key to commit the change.
_Note that the change you have made to the name of the Layer is also reflected in the Legend (Layout)._
9.	Make changes to the other Text Elements of your Layers so that your Legend contains properly formatted and reasonable text descriptions and labels.

### Scale Bar
1.	Go back to the Layout View and go to to Insert>Scale Bar
2.	On the Scale Bar Format > Symbol, Select Scale Line 1
3.	Go to the Design Tab and set the Number of Divisions to 1 and the Subdivisions to 1.
4.	Set the Division Units to Miles.
5.	Click on the Numbers and Marks Tab.
6.	Set the Number Frequencies to “Divisions”
7.	Use the Handles to resize and reposition the Scale Bar.

### Export Your Map
1.	Save your Work.
2.	On the Share Tab, go to the Export Tool and click the Layout button…
3.	Browse to the Intro to ArcGIS Pro folder and save the file as: World_Population
4.	Change the Save as type to PNG(*.png)
5.	Change the Resolution to 200 dpi
6.	Click Export.
7.	Browse to the Workshop Folder and double click on the EX01_World.png file to view it in the default image viewer.
