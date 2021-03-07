---
layout: default
title: Analyzing Data
nav_order: 9
parent: Working with Layers
---

### ANALYZING DATA
Let's take a look at data again to understand what we're working with.

*1*{: .circle .circle-blue} Open the attribute table of the **popMotherTongTractVan_Final** layer if it's not already open.

What do the numbers representing each language in each Census tract represent? Some numbers are over 100, so we know these are not percentages. These numbers represent actual language speakers of each language in each Census tract. 

*2*{: .circle .circle-blue} Scroll to the right and then down through the attribute table and notice what languages are represented by larger numbers of language speakers and which languages don't have very many speakers represented.

Just a visual glance at the data reveals that it appears there are relatively large numbers of speakers of Cantonese, Mandarin, and Panjabi, with Ukrainian, Urdu, and Polish representing relatively small numbers of speakers, among other.

*3*{: .circle .circle-blue} Take a look at the **Aboriginal Languages** column. There are not large numbers of mother tongue speakers of Indigenous languages in Vancouver according to this data.

This is also a good example of how data can both lend greater visibility to certain people and phenomena and erase or render less visible certain people and phenomena. Canada's first languages are made invisible in this dataset and lumped into one group instead of their own languages. This may make more sense given the small numbers of speaker numbers, which may be a function of how data is collected, but it is good to approach data with a critical eye.

### Select by Attributes
Let's take a closer look at the distribution of Aboriginal Languages by using a tool called **Select by Attributes** which enables us to query the data using different expressions.

*1*{: .circle .circle-blue} On the **Map Tab**, go to the **Selection** section and click on the **Select by Attributes** button, which will open a new dialog window.

*2*{: .circle .circle-blue} Set the following parameters:

-	Input Rows: popMotherTongTractVan_Final
- Selection type: New Selection
- Click: New Expression

For the Expression, Where:

-	Field: diameter
- is equal to (this is the default)
- click the dropdown in the third box of the clause to see the range of values

This is a good example of how you can use the Select by Attributes tool to better view the data before you even make a selection.

In this dropdown, the values are sorted by default in order of smallest to largest.

<details>
<summary>What is the largest value in the dataset?</summary>

133
</details>
<br>

Let's return to the **Select by Attributes** query we were building, where we'll select the records representing tracts with speakers numbering over 100.
For the Expression, Where:

-	Field: Aboriginal Languages
- is greater than or equal to
- '113'

*1*{: .circle .circle-blue} Click the **OK** button at the bottom of window to calculate the expression and apply the selection.

In the attribute table, three records are selected, but it may not be apparent at first.

*2*{: .circle .circle-blue}   is selectedScroll through the attribute table and note the records that are selected.

*3*{: .circle .circle-blue} You can observe that the selection from the attribute table is also reflected in the map.
