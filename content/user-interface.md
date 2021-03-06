---
layout: default
title: User Interface
nav_order: 4
---

### USER INTERFACE
ArcGIS Pro is the latest desktop GIS software from the software company Esri. This software must be purchased, downloaded, installed, and configured on your computer for it to work as intended.

Open the software and get familiar with the default user interface.

*1*{: .circle .circle-blue} In Windows, go to the Programs menu and find the ArcGIS Program Group, then select ArcGIS Pro. Or search for ArcGIS Pro in the search bar and open the program.

*2*{: .circle .circle-blue} In the dialog window, click on **Create a New Project > Blank**. This will create a new project file (.**aprx**), and open the ArcGIS Pro main user interface.

*3*{: .circle .circle-blue} In the new dialog window, click ok to accept the defaults and finish creating your new project. Click on map under **Blank Templates** if necessary to enter the main user interface (UI) for ArcGIS Pro.

You should see something like this:
![mainUI_pro.jpg](https://raw.githubusercontent.com/fiddleHeads/intro-to-arcgis-pro/master/content/images/mainUI_pro.jpg)

### Signing into ArcGIS Pro
If you weren't already prompted to sign into your ArcGIS Online or UBC ArcGIS account, let's make sure to do so now. One of the advantages to ArcGIS Pro is its seamless connection to and interaction with ArcGIS Online and all of the layers and basemaps available.

*1*{: .circle .circle-blue} From the upper right of your map window, click the dropdown menu next to **Not signed in** and select **Sign in**.

*2*{: .circle .circle-blue} Sign into your ArcGIS Online account.

### Main UI Components
The ArcGIS Pro user interface (UI) has a few main components:
- The **Map Frame**: This is where your data will be visualized.
- The **Contents Pane**: This will likely be your most used "tabbed" window because it's where you'll interact with your data. As you add data to your project, they'l appear here as **layers**.
- The **Catalogue Pane**: This pane is similar to Windows Explorer, or Mac Finder. You can create connections to data sources (drives, folders, networks, etc.) and perform several data maintenance and management tasks in this pane. The search option is also available here, which is used to search for tools, documents, and data.
- **Menu Tabs**: These are located at the top of the main UI and can be  selected/activated as needed. We will use these later in the tutorial.

### Insert a New Map
If you are not already viewing a map as shown above, the first step will be to insert a new map in our UI.
In the **Main Menu**, select **Insert > New Map**. Notice that a new map tab has been added to the Map Frame and Tools from the Main Menu are now enabled.

### Interact with Tabbed Menus
 Move your cursor to the **Contents Pane**, and notice the small down arrow on the right side. If clicked, this arrow give you options to **Float**, **Dock**, **Auto-Hide**, and **Close** the pane.    

Using the **Catalog Title Bar**, click and drag the Catalog Pane away from its docked position. Notice the "docking arrows" that appear as you move the window.

### Explore the Windows (Catalog)

Using the Windows Explorer, navigate to the **Intro** folder containing the previously downloaded the workshop materials.

*1*{: .circle .circle-blue} Return to ArcGIS Pro and right-click on the folders item in the **Catalog Pane**, then select **Add Folder Connection** (or **Go to Insert**) **> Add Folder**

*2*{: .circle .circle-blue} Select the **Downloads** icon and click **OK**.

*3*{: .circle .circle-blue} Expand the resulting **Folder Connection** in the **Catalog Window** and expand the **Intro.gdb**.

There should be three [feature classes](https://pro.arcgis.com/en/pro-app/latest/help/data/geodatabases/overview/feature-class-basics.htm) in this geodatabase. A geodatabase helps us organize data collections in ArcGIS projects.
