---
layout: default
title: Mapping Distribution
nav_order: 11
parent: Working with Layers
---

### MAPPING DISTRIBUTION

In the previous section, we used chloropleth mapping to visualize the distribution of one set of speakers provided in the dataset we're using. Next we'll use something called [Dot Density](https://pro.arcgis.com/en/pro-app/latest/help/mapping/layer-properties/dot-density.htm), which is another way to represent quantities on a map.

*1*{: .circle .circle-blue} Uncheck the layer we were working with in the last section and make visible the copy we made in the **Contents** pane.

*2*{: .circle .circle-blue} From the **Symbology** pane on the far right (open it back up if it's closed), select **Dot Density** from the dropdown menu under **Primary symbology**.

*3*{: .circle .circle-blue} Select the **Basic Random** color scheme.

Let's create a few different layers using this symbology for the languages we identified has having larger numbers of speakers. First let's create a map showing the distribution of Cantonese and Mandarin mother tongue language speakers.

*4*{: .circle .circle-blue} Select these languages from the dropdown arrows under **Fields**.

*5*{: .circle .circle-blue} Select the **Background** symbol below **Dot Value** and change the symbology color to black. Leave the default outline color and click **Apply**.

*6*{: .circle .circle-blue} Highlight the **popMotherTongTractVan** copy layer in the **Contents** pane and reduce the **Dot Size** to 1.3 pt.

*7*{: .circle .circle-blue} Change the color of the dots if need be to make sure they're visible. It should look something like the image below.

![mandCant.jpg](https://raw.githubusercontent.com/ubc-library-rc/intro-to-arcgis-pro/master/content/images/mandCant.jpg)

There's a pretty interesting pattern that appears, which is that speakers of these languages are distinctly spatially clustered, with mother tongue Mandarin speakers in the western part of the city and mother tongue Cantonese speakers largely in the eastern part. Why do think that might be? Migration and settlement patterns where people follow relatives or neighbors from the old country to settle in the same geographic areas of the city? Household income? Any other ideas?

### Mapping Additional Languages
*1*{: .circle .circle-blue} Create a copy of this layer in the **Contents** pane by right-clicking and selecting **Copy** and then right-clicking **Map** and selecting **Paste** and save your map.

*2*{: .circle .circle-blue} Rename the layer we used to create a chloropleth map **Aboriginal Languages** by right-clicking the layer, selecting **Properties**, and renaming it under the **General** in the new window that pops up.

*3*{: .circle .circle-blue} Rename the layer we just symbolized with dot density to **Mandarin and Cantonese Languages** and the newly copied layer to **Panjabi Languages**. 

*4*{: .circle .circle-blue} Ensure the only layer turned on is the **Panjabi Languages**.

*5*{: .circle .circle-blue} Make sure this layer is using dot density symbology and that Panjabi is selected under the **Fields**.

*6*{: .circle .circle-blue} Reduce the dot size again and choose an appropriate color and make sure the **Background** symbology is black.

You can see that there is also a distinct geographic distribution of Panjabi mother tongue language speakers.

You also may have noticed by now that dot density symbology is more effective for this dataset compared to chloropleth symbology. You may want to create a copy of the **Aboriginal Languages** layer and compare the chloropleth and dot density symbologies for this dataset. 

![dotAborig.jpg](https://raw.githubusercontent.com/ubc-library-rc/intro-to-arcgis-pro/master/content/images/dotAborig.jpg)

### Exercise On Your Own
*1*{: .circle .circle-blue} Create an additional one or two copies of the language data and, using dot density symbology, create one or two examples of the distribution of language speakers for a language of your choice.

*2*{: .circle .circle-blue} Label these layers accordingly in the **Contents** pane.

We'll use one of these examples to create a map for export in the next section.

