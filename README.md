# My Warehouse Visualizer Documentation 

# Contents

* [Introduction](#Introduction)
	* [Demonstration Site](#Demonstration-Site)
	* [A Place for Everything, and Everything in Its Place](#A-Place-for-Everything-and-Everything-in-Its-Place)
* [Quick Start](#Quick-Start)
	* [Using the Layout and Inventory CSV files from a Google Sheet](#Using-the-Layout-and-Inventory-CSV-files-from-a-Google-Sheet)
	* [Uploading the Layout and Inventory CSV Files](#Uploading-the-Layout-and-Inventory-CSV-Files)
* [Background](#Background)
	* [General](#General)
	* [Technical](#Technical)
* [Requirements](#Requirements)	
	* [Data](#Data)
		* [Layout Data Specifications](#Layout-Data-Specifications)
		* [Inventory Data Specifications](#Inventory-Data-Specifications)
		* [Data Attributes](#Data-Attributes)
* [Analysis and Visualization](#Analysis-and-Visualization)	
* [Built With](#Built-With)
* [Creator](#Creator)
* [License](#License)
<!-- * [Concepts](#Concepts) -->

## Introduction

* ***My Warehouse Visualizer*** is a version of [***My Data Visualizer***](http://MyDataVisualizer.com); develped specfically to aid warehouse/supply chain managers visualize inventory in a [WebGL](https://www.khronos.org/webgl/) 3D visuals of warehouses.
* The application implements the [DataVisual](https://observablehq.com/@mariodelgadosr/datavisual-data-visual-design-pattern-for-webgl-3d-assets) design pattern.
* Like ***My Data Visualizer***, ***My Warehouse Visualizer*** is a [100% Client-side application](https://en.wikipedia.org/wiki/Client-side); your data is not uploaded to a server or the cloud.

### Demonstrations	

* [My Warehouse Visualizer Demo](http://mydatavisualizer.com/demo/warehouse)  

	Existing warehouse layouts and inventories can be viewed on the demonstration site or you can dynamically reference newly loaded data as described in the [*Quick Start*](#Quick-Start) section.

* [Warehouse Visualization with DataVisual](https://observablehq.com/@mariodelgadosr/warehouse-visualization-with-datavisual?collection=@mariodelgadosr/datavisual)
	
### A Place for Everything, and Everything in Its Place

The *All about warehouse slotting* video provides a good overview of one of the supply chain managers best practices for warehouse storage.

[![All about warehouse slotting](https://img.youtube.com/vi/RzAcwQiPi-w/0.jpg)](https://www.youtube.com/embed/RzAcwQiPi-w)

***My Warehouse Visualizer*** helps visualize the results of slotting strategies and optimizations.

## Quick Start

![Screen Shot of My Warehouse Visualizer](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/img/MyWarehouseVisualizerDamagedAnalysis.png)

* The quickest workflow to visualize a warehouse layout and its inventory is to use data from a Google Sheet.  

* The [Small Warehouse Google Sheet](https://docs.google.com/spreadsheets/d/14Xwqk9zJxkBt5enYEWTbOPUQrKn0AoMyFYaUePHtk8o/edit#gid=0) contains Layout and Inventory data in separate pages that can be referenced in [Comma-separated value](https://en.wikipedia.org/wiki/Comma-separated_values) format. 

* This sheet was utilized when demonstrating the technical foundation of ***My Warehouse Visualizer*** in the [*Warehouse Visualization With DataVisual*](https://observablehq.com/@mariodelgadosr/warehouse-visualization-with-datavisual) Observable notebook.

### Using the Layout and Inventory CSV files from a Google Sheet

* The published CSV Layout data pages are available at the followig URLs: 

	* [https://docs.google.com/spreadsheets/d/e/2PACX-1vT3XpGLIsLj3cyj4rdraGQggWcjN-eHL4HgHec0gEWGc2g5lZi5q0FRpj-I73CCpYE-lsVeiHmhzeA3/pub?gid=0&single=true&output=csv](https://docs.google.com/spreadsheets/d/e/2PACX-1vT3XpGLIsLj3cyj4rdraGQggWcjN-eHL4HgHec0gEWGc2g5lZi5q0FRpj-I73CCpYE-lsVeiHmhzeA3/pub?gid=0&single=true&output=csv)

	* [https://docs.google.com/spreadsheets/d/e/2PACX-1vT3XpGLIsLj3cyj4rdraGQggWcjN-eHL4HgHec0gEWGc2g5lZi5q0FRpj-I73CCpYE-lsVeiHmhzeA3/pub?gid=377990885&single=true&output=csv](https://docs.google.com/spreadsheets/d/e/2PACX-1vT3XpGLIsLj3cyj4rdraGQggWcjN-eHL4HgHec0gEWGc2g5lZi5q0FRpj-I73CCpYE-lsVeiHmhzeA3/pub?gid=377990885&single=true&output=csv)

* Select *CSV URLs...* from the *Warehouse:* drop-down menu:

![Screen Shot of CSV URLs Selection](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/img/CSVURLs.png)

* Input the two CSV URLs and select the *OK* button.

![Screen Shot of CSV URLs Selection](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/img/CSVURLs2.png)

* Screen Shot for the loaded Layout and Inventory Data:
 
![Screen Shot of My Warehouse Visualizer](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/img/MyWarehouseVisualizer.png)

### Uploading the Layout and Inventory CSV Files

Alternatively, the layout and inventory data can be uploaded to ***My Warehouse Visualizer***.  Several sample files are provided in the [data folder](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/tree/master/data):

* Select *Upload...* from the *Warehouse:* drop-down menu:

![Screen Shot of Upload Selection](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/img/Upload.png)

* Select layout and inventory files to upload.  The filenames must contain the text 'layout' and 'inventory' in their names to distinguish them.  The files can be dragged-and-dropped onto the page or selected from a file dialog.

![Screen Shot of File Selection](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/img/Upload2.png)

* Screen Shot for the loaded Layout and Inventory Data:
 
![Screen Shot of My Warehouse Visualizer](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/img/MyWarehouseVisualizer.png)



## Background

### General

Both ***My Data Visualizer*** and ***My Warehouse Visualizer*** were developed to add an important *dimension* to data visualization; [WebGL 3D graphics](https://blogg.bekk.no/webgl-and-data-visualisation-379d8252ea51?gi=fe1368432a8f).

With ***My Warehouse Visualizer***, inventory data is contextualized on a 3D graphic representation of a warehouse layout.

![Screen Shot of My Warehouse Visualizer](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/img/MyWarehouseVisualizerDamagedAnalysis.png)

### Technical

The following [Computational Essay](https://blog.stephenwolfram.com/2017/11/what-is-a-computational-essay/) hosted on [ObservableHQ.com](https://observablehq.com/@observablehq/introduction-to-notebooks) provides a technical background on the design approach for ***My Warehouse Visualizer***:

* [*Warehouse Visualization With DataVisual*](https://observablehq.com/@mariodelgadosr/warehouse-visualization-with-datavisual)

## Requirements

***My Warehouse Visualizer*** requires:

* A warehouse layout file that specifies the the dimensions and locations of the storage slots.

* An inventory file that details what items are stored in the storage slots.

### Data

* The data to be visualized must be in a [Comma-separated](https://en.wikipedia.org/wiki/Comma-separated_values) format.  

	* Several sample files are available for review in the [data folder](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/tree/master/data).

* When loaded, the data are parsed with the [D3 AutoType parser](https://github.com/d3/d3-dsv#autoType).
	
	* Any column name that is prefixed with a '\s' instructs the parser to override the [D3 AutoType parser](https://github.com/d3/d3-dsv#autoType) and treat the columns contents as a string.  An example of this in the sample data is the *\sITEM NO* column in the [sample invetory files](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/tree/master/data). 

#### Layout Data Specifications

At a minimum, the Layout data must have the following columns of data:

Column Name | Notes 
-------|-------
LOCATION | A unique identifier for a slot. 'LOCATION' is also a column in the Inventory dataset.
WIDTH | A numeric value representing the width of an individual slot.
DEPTH | A numeric value representing the depth of an individual slot. 
HEIGHT | A numeric value representing the height of an individual slot. 
X | A numeric value representing the X coordinate of an individual slot. 
Y | A numeric value representing the Y coordinate of an individual slot. 
Z | A numeric value representing the Z coordinate of an individual slot.
AISLE | An aisle identifier for the slot.
CENTERAXIS | Contains either a value of 'X' or 'Y' to instruct the application along which axis the relative 'AISLE' is oriented on.
BAY | A unique identifier for a collection of 'LOCATION' slots.

#### Inventory Data Specifications

At a minimum, the Inventory data must have the following columns of data:

Column Name | Notes 
-------|-------
LOCATION | A unique identifier for a slot. 'LOCATION' is also a column in the Inventory dataset.


##### Data Attributes

The following table summarizes the data attributes supported by ***My Warehouse Visualizer*** for data hosted in the [Comma-separated](https://en.wikipedia.org/wiki/Comma-separated_values) format datasets:

Attribute | Description
-------|------------
*dimension* |  An attribute identifier for a dimension(s).  Examples: 'LOCATION', 'AISLE', 'BAY', '\sITEM NO'; see '\s' prefix below. 
*measure*  | An attribute identifier for a measure(s). Example: 'ITEM WGT', 'WEEKLY MVMT', 'ITEM COST'.
*COLOR_dimension, COLOR_measure* |  An indentifier with the '*COLOR_*' prefix designates an pre-define color attribute for a given *measure* or *dimension*.  Values can be any [CSS color name](https://www.w3schools.com/colors/colors_names.asp) or [hex triple](https://en.wikipedia.org/wiki/Web_colors#Hex_triplet) value.
*DATE_dimension, DATETIME_dimension, TIME_dimension* | An attriute identifier for an [ECMA Script](https://www.ecma-international.org/ecma-262/9.0/index.html#sec-date-time-string-format) formatted date specified as a *dimension* . The '*DATE_*', '*DATETIME_*' and '*TIME_*' prefixes designate the data as a JavaScript Date.  
*LINK_* | An attribute identifier for optional HyperLinks associated with *name* column values. At run-time, ***My Warehouse Visualizer*** will append the *name* column value to the '*LINK_*' column value and instruct the browser to navigate to that [url](https://en.wikipedia.org/wiki/URL).	
*\s* | An attribute identifier that instructs the data load parser to override the D3 AutoType parser](https://github.com/d3/d3-dsv#autoType) and treat the columns contents as a string.

## Analysis and Visualization

* Once Layout and Inventory data have been loaded, the analysis and visualization functionality is similar to ***My Data Visualizer***.  

* Detail documentation can be found at [https://github.com/MarioDelgadoSr/MyDataVisualizerDoc#analysis](https://github.com/MarioDelgadoSr/MyDataVisualizerDoc#analysis);


## Built With

The following frameworks and applications were used to build ***My Warehouse Visualizer***:

* [D3.js](https://d3js.org/) - D3 framework
* [Three.js](https://threejs.org/) - Three.js framework
* [w2ui UI Library](http://w2ui.com/web/) 


## Creator

* **Mario Delgado**  Github: [MarioDelgadoSr](https://github.com/MarioDelgadoSr)
* LinkedIn: [Mario Delgado](https://www.linkedin.com/in/mario-delgado-5b6195155/)
* [***My Data Visualizer***](http://MyDataVisualizer.com): A data visualization application using the [*DataVisual*](https://github.com/MarioDelgadoSr/DataVisual) design pattern.
	* [***My Warehouse Visualizer***](http://MyDataVisualizer.com/demo/warehouse)
* Contact: [MyDataVisualizer(at)gmail.com](mailto:MyDataVisualizer@gmail.com). 

## License

* [***My Data Visualizer***](http://MyDataVisualizer.com) and [***My Warehouse Visualizer***](http://MyDataVisualizer.com/demo/warehouse) are free for all non-profit entities.  
* Businesses and commercial enterprises are granted full use license as long as they make their application freely available to non-profits. 
