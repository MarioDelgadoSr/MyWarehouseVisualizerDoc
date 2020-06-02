# My Warehouse Visualizer Documentation 

# Contents

* [Introduction](#Introduction)
	* [Demonstration Site](#Demonstration-Site)
	* [A Place for Everything, and Everything in Its Place](#A-Place-for-Everything,-and-Everything-in-Its-Place)
* [Quick Start](#Quick-Start)
	* [Using the Layout and Inventory CSV files from a Google Sheet](#Using-the-Layout-and-Inventory-CSV-files-from-a-Google-Sheet)
	* [Uploading the Layout and Inventory CSV Files](Uploading-the-Layout-and-Inventory-CSV-Files)
* [Background](#Background)
	* [General](#General)
	* [Technical](#Technical)
* [Requirements](#Requirements)	
	* [Data](#Data)
		* [Special Note](#Special-Note)
		* [Data Attributes](#Data-Attributes)
	* [WebGL 3D Graphic](#WebGL-3D-Graphic)
* [Analysis](#Analysis)	
	* [Data Visual](#Data-Visual)
	* [Analyzer](#Analyzer)
		* [Data Grid](#Data-Grid)
		* [Visualization Scale and Legend](#Visualization-Scale-and-Legend)
	* [Visual Grid](#Visual-Grid)
* [Built With](#Built-With)
* [Creator](#Creator)
* [License](#License)
<!-- * [Concepts](#Concepts) -->

## Introduction

* ***My Warehouse Visualizer*** is a version of [***My Data Visualizer***](http://MyDataVisualizer.com); develped specfically to aid warehouse/supply chain managers for visualize inventory in a [WebGL](https://www.khronos.org/webgl/) 3D visuals of warehouses.
* The application implements the [DataVisual](https://observablehq.com/@mariodelgadosr/datavisual-data-visual-design-pattern-for-webgl-3d-assets) design pattern.
* Like ***My Data Visualizer***, ***My Warehouse Visualizer*** is a [100% Client-side application](https://en.wikipedia.org/wiki/Client-side); your data is not uploaded to a server or the cloud.

### Demonstration Site	

* [My Warehouse Visualizer Demo](http://mydatavisualizer.com/demo/warehouse)
	
Existing warehouse layouts and inventories can be viewed on the demonstration site or you can dynamically reference newly loaded data as described in the [*Quick Start*](#Quick-Start) section.
	
**Note**: 

* This documentation describes features and functionality in the free version of My Warehouse Visualizer.  
* The full licensed version of the application and framework has additional features detailed in a separate document.

### A Place for Everything, and Everything in Its Place

The *All about warehouse slotting* video provides a good overview of one of the supply chain managers best practices for warehouse storage.

[![All about warehouse slotting](https://img.youtube.com/vi/RzAcwQiPi-w/0.jpg)](https://www.youtube.com/embed/RzAcwQiPi-w)

*My Warehouse Visualizer* helps visualize the results of slotting strategies and optimizations.

## Quick Start

![Screen Shot of My Warehouse Visualizer](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/img/MyWarehouseVisualizerDamagedAnalysis.png)

* The quickest workflow to visualize a warehouse layout and its inventory is to use data from a Google Sheet.  

* The [Small Warehouse Google Sheet](https://docs.google.com/spreadsheets/d/14Xwqk9zJxkBt5enYEWTbOPUQrKn0AoMyFYaUePHtk8o/edit#gid=0) contains Layout and Inventory data in seperate pages that can be referenced in [Comma-seperated value](https://en.wikipedia.org/wiki/Comma-separated_values) format. 
	
* This sheet was utilized when demonstrating the technical foundation of *My Warehouse Visualizer* in the [*Warehouse Visualization With DataVisual](https://observablehq.com/@mariodelgadosr/warehouse-visualization-with-datavisual) Observable notebook.

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

Alternatively, the layout and inventory data can be uploaded to *My Warehouse Visualizer*.  Several sample files are provided in the [data folder](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/tree/master/data):

* Select *Upload...* from the *Warehouse:* drop-down menu:

![Screen Shot of Upload Selection](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/img/Upload.png)

* Select a layout and inventory files to upload.  The filenames must contain the text 'layout' and 'inventory' in their names to distinguish them.  The files can be dragged-and-dropped onto the page or selected from a file dialog.

![Screen Shot of File Selection](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/img/Upload2.png)

* Screen Shot for the loaded Layout and Inventory Data:
 
![Screen Shot of My Warehouse Visualizer](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/img/MyWarehouseVisualizer.png)


# FINISH =>



### General

***My Data Visualizer*** was developed to add an important *dimension* to data visualization; [WebGL 3D graphics](https://blogg.bekk.no/webgl-and-data-visualisation-379d8252ea51?gi=fe1368432a8f).

With ***My Data Visualizer*** data is contextualized on a 3D graphic representation of the real-world objects that the data is associated with.

For example, the following screen shot visualizes passenger revenue on a plane for each assigned seat location:

![Screen Shot of My Data Visualizer Plane Visualization](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/img/MyDataVisualizerPlaneScreenShot.png)


### Technical

The following two [Computational Essays](https://blog.stephenwolfram.com/2017/11/what-is-a-computational-essay/) hosted on [ObservableHQ.com](https://observablehq.com/@observablehq/introduction-to-notebooks) provide a technical background on the design approach for ***My Data Visualizer***:

* [DataVisual (Data + Visual) Design Pattern for WebGL 3D Assets](https://observablehq.com/@mariodelgadosr/datavisual-data-visual-design-pattern-for-webgl-3d-assets) and 
* [DataVisual (Data + Visual) Design Pattern for WebGL 3D Assets using a glTF with Embedded Data](https://observablehq.com/@mariodelgadosr/datavisual-data-visual-design-pattern-for-webgl-3d-assets-u)


## Requirements

***My Data Visualizer*** requires:

* **Data** (measures and dimensions) following a set of simple [specifications](#Data-Attributes);
* **WebGL 3D** Graphic with addressable [material(s)](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0#materials) for the graphic's sub-components that will be visualized.

Both of these components can be uploaded (see screen shot) to the [demonstration application](http://mydatavisualizer.com/demo/) as one of the following:

* A .gltf or .glb file with its associated .csv file (see [Quick Start](#Quick-Start) for an example);
* A .gltf file with embedded data; (see the [repository](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/tree/master/repository) for several examples).
* A .glb file with the embedded data (see the [repository](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/tree/master/repository) for several examples).

Data that are uploaded are parsed with the [D3 AutoType parser](https://github.com/d3/d3-dsv#autoType).

![Screen Shot of My Data Visualizer Upload](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/img/MyDataVisualizerUploadScreenShot.png)


#### Data

The data to be visualized can be in either a [.csv file](https://en.wikipedia.org/wiki/Comma-separated_values) or embedded in the [glTF file](https://github.com/KhronosGroup/glTF/tree/master/specification/) that describes the WebGL 3D graphic itself.

* The [Body.csv](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/repository/Tutorial/Body.csv) is an example of the data associated with the [*Body.gltf*](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/repository/Tutorial/Body.gltf) file:

name | INSURANCE_CLAIMS | DOCTOR_VISITS | LAB_ORDERS | DATE_LAST_TEST | COLOR_INSURANCE_CLAIMS | LINK_
-------|-------|-------|-------|-------|-------|-------
Brain | 27000 | 3 | 0 | 2019-02-01T00:00 | green | http://www.bing.com/search?q=
Heart | 234000 | 11 | 6 | 12019-06-09T00:00 | red | http://www.bing.com/search?q=
Kidneys | 14500 | 5 | 1 | 2019-08-01T00:00 | yellow | http://www.bing.com/search?q=

* Creating a .csv file with the data is relatively simple and can be accomplished with spreadsheet; like [Microsoft Excel](https://support.office.com/en-us/article/Import-or-export-text-txt-or-csv-files-5250ac4c-663c-47ce-937b-339e391393ba).

* In contrast, [BodyEmbeddedData.gltf](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/repository/BodyEmbeddedData.gltf) illustrates the embedded data scenario.  Below is a reference to one of the several [extras](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0#reference-extras) sections hosting the data associated with the individual meshes:

<pre style="background-color: gainsboro;"> 
	"extras": {
					"LINK_": "http://www.bing.com/search?q=",			
					"COLOR_INSURANCE_CLAIMS": "green",
					"DATE_LAST_TEST": "2019-02-01T00:00",
					"DOCTOR_VISITS": 3.0,
					"INSURANCE_CLAIMS": 27000.0,
					"LAB_ORDERS": 0.0
				}

</pre>


* The embedded data scenario involves using a graphical tool that allows you to add the [extras](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0#reference-extras) sections to the WebGL 3D graphics.  The github repository [***Python Script to Add Blender Custom Properties From CSV File***](https://github.com/MarioDelgadoSr/AddBlenderCustomPropertiesFromCSV) details one possbile approach for developers that use the popular [Blender](https://www.blender.org/) application.

	* This video also provides step-by-step instructions on adding [Custom Properties](https://docs.blender.org/manual/en/latest/data_system/custom_properties.html) to Blender that are then embedded as extras when a [Blender glTF file is exported](https://wiki.blender.org/wiki/Reference/Release_Notes/2.80/Import_Export):
	
	[![Adding Custom Properties to Objects](https://img.youtube.com/vi/MWkoviO_xkY/0.jpg)](https://www.youtube.com/watch?v=MWkoviO_xkY)


##### Special Note
	
* The [data specifications](#Data-Attributes) for the free/demonstration version of ***My Data Visualizer*** are more restrictive than those described in the [DataVisual (Data + Visual) Design Pattern for WebGL 3D Assets](https://observablehq.com/@mariodelgadosr/datavisual-data-visual-design-pattern-for-webgl-3d-assets) and the business version.
* Specifically, the attribute used to match/join the data to the visual objects is the [*name*](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0#indices-and-names) attribute associated with each individual [mesh](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0#meshes) that is the target of a visualization.
* Refer back to the [Quick Start](#Quick-Start) for a specific example of this with the *name* attribute referenced in both the data and glTF file.

##### Data Attributes

The following table summarizes the data attributes supported by ***My Data Visualizer*** for data hosted in either a .csv file or embedded within the glTF file:

Attribute | Description
-------|------------
*name* | The value associated with the *name* attribute must match the glTF mesh *names*.
*dimension* |  An attribute identifier for a dimension(s).  Examples: 'Part Number', 'Part_Number', 'PartNumber'
*measure*  | An attribute identifier for a measure(s). Example: 'Number of Complaints', 'Number_of_Complaints', 'NumberOfComplaints'
*COLOR_dimension, COLOR_measure* |  An indentifier with the '*COLOR_*' prefix designates an pre-define color attribute for a given *measure* or *dimension*.  Values can be any [CSS color name](https://www.w3schools.com/colors/colors_names.asp) or [hex triple](https://en.wikipedia.org/wiki/Web_colors#Hex_triplet) value.
*DATE_dimension, DATETIME_dimension, TIME_dimension* | An attriute identifier for an [ECMA Script](https://www.ecma-international.org/ecma-262/9.0/index.html#sec-date-time-string-format) formatted date specified as a *dimension* . The '*DATE_*', '*DATETIME_*' and '*TIME_*' prefixes designate the data as a JavaScript Date.  
*LINK_* | An attribute identifier for optional HyperLinks associated with *name* column values. At run-time, ***My Data Visualizer*** will append the *name* column value to the '*LINK_*' column value and instruct the browser to navigate to that [url](https://en.wikipedia.org/wiki/URL).	


#### WebGL 3D Graphic

* The WebGL 3D Graphic is described in a [glTF file with the 2.0 specifications](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0).  
* Several examples are provided in the documentation [repository](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/tree/master/repository).  
	* Note that each individual mesh (object sub-component) **must have a distinct material associated with it**.  If this condition is not satisfied, the visualization logic can not *drive* sub-component visualizations.
    * In addition, the glTF file **must have** any [buffers](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0#binary-data-storage) and [images](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0#images) for the .gltf file referenced with embedded [Data URIs](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0#uris).
		* This is a [specific export option with the Blender glTF exporter](https://github.com/KhronosGroup/glTF-Blender-Exporter/blob/master/docs/user.md#embedding).
	* This video is a tutorial for exporting a glTF with Blender:
	
		[![Exporting GLTF file using Blender](https://img.youtube.com/vi/xfUZ1GLG68o/0.jpg)](https://www.youtube.com/watch?v=xfUZ1GLG68o)

## Analysis

***My Data Visualizer*** has three primary panels used in the data visualization analysis:

* Data Visual 
* Analyzer
* Visual Grid

### Data Visual

The ***Data Visual*** panel displays a 3D rendering of the WebGL graphic.   Several mouse interactions, quick keys and  buttons are available to interact with the visual (see screen shot):

Mouse Action | Description
-------|------------
Left | Rotate
Scroll | Zoom
Right | Pan
Left Double-Click| Toggle search isolation of an object. 
CtrlKey + Left | Select an object and navigate link(s).  If a link is associate wth an object, a selection drop will be displayed allowing navigation to the designated address (see screen shot).

Key | Description
-------|------------
Arrow | Pan
'b' | 'B'ird's-eye View/Rotate 
'c' or 'Esc' | 'C'lear Data Selections

Button | Description
-------|------------
GPU Performaance | Displays Graphic Processing Unit (GPU) statistics.
Reset View | Resets Bird's-eye View.
Axes | Toggles display of the origin axes associate with the visual.
Background | A color selection picker for the background color.
Bounding Box/Color | Toggles disply of a visual bounding box and color selection.
Camera Field of View | Allows selection of the visual's field of view.
Polar Angel |  Allows selection of the rotation polar angle.  With a polar angle of 180 degrees, the image can be viewed from underneath.
Zoom Speed | Controls the scroll zooming speed for a visual.
Pan Speed | Controls the pan speed.
Grid/Grid Color | Toggles the display of the visual's grid and its color.
Center Line Color | Sets the center line color for the grid when it is being displayed.
Grid Divisions | Sets the number of grid divisions when it is being displayed.

![Screen Shot of My Data Visualizer ForkLift1](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/img/MyDataVisualizerForkLiftScreenShot1.png)

### Analyzer

The ***Toggle Analyzer*** button toggles the display of the Analyzer panel.  It contains the ***Data Grid***, ***Visualization Scale/Legend*** sub panels.

In the following screen shot: 

* The *PART* dimension associated with the Forklift visual is selected.
* A red (low) to green (high) color scale is selected and alphabetically assigned to the individual parts in the legend and visual sub-components.

![Screen Shot of My Data Visualizer ForkLift2](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/img/MyDataVisualizerForkLiftScreenShot2.png)

#### Data Grid 

The ***Data Grid***: 

* Displays the data that visualizes the 3D WebGL graphic.  
* Selecting a column directs the application to visualize the graphic by either a scale colorization determined by the column's values or preset color assignments.  
* Selecting the ***Visualize Grid*** button will color visualize the ***Data Grid*** itself.   
* Searches or row selections can be performed on the the ****Data Grid**** to isolate sub-objects in the visual panel.
* When the ***Visual Grid*** is being displayed, searches in the ***Data Grid** are coordinated with it.

#### Visualization Scale and Legend

The ***Visualization Scale*** and ***Legend*** panels display a color scale selection wheel with its corresponding legend.  The left mouse button is used to select the desired scale.

The triangle in the ***Visualization Scale***  panel illustrates the color scale from low to high values.

![Screen Shot of My Data Visualizer ForkLift3](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/img/MyDataVisualizerForkLiftScreenShot3.png)


### Visual Grid

The ***Visual Grid***:

* Is enabled with the ***Toggle Visual Grid*** button.
* Displays specific attributes common to all visuals; *name*, *Color* (the original color associated with a mesh), *id*, *x* coordinate, *y* coordinate and *z* coordinate. 
* Selecting a column directs the application to visualize the graphic by either a scale colorization determined by the column's values or the original color assignments.  
* Selecting the ***Visualize Grid*** button will color visualize the ***Visual Grid*** itself.   
* Searches or row selections can be performed on the the ****Visual Grid**** to isolate sub-objects in the visual panel.
* When the ***Data Grid*** is being displayed, searches in the ***Visual Grid** are coordinated with it.
 
![Screen Shot of My Data Visualizer ForkLift4](https://github.com/MarioDelgadoSr/MyWarehouseVisualizerDoc/blob/master/img/MyDataVisualizerForkLiftScreenShot4.png) 

## Built With

The following frameworks and applications were used to build ***My Data Visualizer***:

* [D3.js](https://d3js.org/) - D3 framework
* [Three.js](https://threejs.org/) - Three.js framework
* [glTF](https://www.khronos.org/gltf/) - Khronos' graphic library Transmission Format
* [GLTFLoader](https://threejs.org/docs/index.html#examples/loaders/GLTFLoader) - A loader for glTF 2.0 resources
* [Blender](https://www.blender.org/) - For building a 3D visual and [exporting](https://docs.blender.org/manual/en/dev/addons/io_gltf2.html) it to a glTF file.
* [w2ui UI Library](http://w2ui.com/web/) 


## Creator

* **Mario Delgado**  Github: [MarioDelgadoSr](https://github.com/MarioDelgadoSr)
* LinkedIn: [Mario Delgado](https://www.linkedin.com/in/mario-delgado-5b6195155/)
* [***My Data Visualizer***](http://MyDataVisualizer.com): A data visualization application using the [*DataVisual*](https://github.com/MarioDelgadoSr/DataVisual) design pattern.
* Contact: [MyDataVisualizer(at)gmail.com](mailto:MyDataVisualizer@gmail.com). 

## License

* [***My Data Visualizer***](http://MyDataVisualizer.com) is free for all non-profit entities.  
* Businesses and comerical enterprises must purchase a license.  
	* The license includes access to the ***My Data Visualizer*** JavaScript-based framework; which developers can use to embed data-driven WebGL assets in their applications. 

