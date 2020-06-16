---
layout: default
title: User Interface
nav_order: 2
---

## USER INTERFACE
ArcGIS Pro is the latest desktop GIS software from the software company Esri. This software must be purchased, downloaded, installed, and configured on your computer for it to work as intended. Those of you at the University of British Columbia can find more information about the availability of ArcGIS Pro software :exclamation: here :exclamation:.

Open the software and get familiar with the default user interface.
1.  In Windows, go to the Programs menu and find the ArcGIS Program Group, then select ArcGIS Pro.
2. In the dialog window, click on **Create a New Project > Blank**. This will create a new project file (.**aprx**), and open the ArcGIS Pro main user interface.
3. In the new dialog window, click ok to accept the defaults and finish creating your new project.

You should see something like this:
:exclamation:[image showing the main UI components]:exclamation:

### Main UI Components
The ArcGIS Pro user interface (UI) has a few main components:
- The **Map Frame**: This is where your data will be visualized.
- The **Contents Pane**: This will likely be your most used "tabbed" window because it's where you'll interact with your data. As you add data to your project, they'l appear here as **layers**.
- The **Catalogue Pane**: This pane is similar to Windows Explorer, or Mac Finder. You can create connections to data sources (drives, folders, networks, etc.) and perform several data maintenance and management tasks in this pane. The search option is also available here, which is used to search for tools, documents, and data.
- **Menu Tabs**: These are located at the top of the main UI and can be  selected/activated as needed. We will use these later in the tutorial.

#### Insert a New Map
The first step we will want to take is to insert a new map in our UI.
 In the **Main Menu**, select **Insert > New Map**. Notice that a new map tab has been added to the Map Frame and Tools from the Main Menu are now enabled.

#### Interact with Tabbed Menus
 Move your cursor to the **Contents Pane**, and notice the small down arrow on the right side. If clicked, this arrow give you options to **Float**, **Dock**, **Auto-Hide**, and **Close** the pane.    

Using the **Catalog Title Bar**, click and drag the Catalog Pane away from its docked position. Notice the "docking arrows" that appear as you move the window.

#### Explore the Windows (Catalog)
Using the Windows Explorer,  navigate to the **Intro-to-ArcGIS-Pro** directory where you extracted this workshop's files, and click into the **Data** folder.

Note that there are more files in this folder than there are Shapefiles as ArcGIS Pro shows. This is because a Shapefile is not actually _a file_, but instead _a collection of files_.

1. Return to ArcGIS Pro and right-click on the folders item in the **Catalog Pane**, then select **Connect Folder** (or **Go to Insert**) **> Add Folder**
2. Select the **Desktop** icon and click **OK**.
3. Expand the resulting **Folder Connection** in the **Catalog Window** and expand the folder::exclamation: **XXXX.gdb**.:exclamation:

Note that the features are simplified in the **Catalog Window**. Although the Feature Class is made of several files, ArcGIS Pro knows it's better just to show the Shapefile. This allows you to copy, paste, rename, etc. without having to manage several files per dataset.
