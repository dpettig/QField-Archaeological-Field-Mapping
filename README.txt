This project is licensed under the MIT License — please credit Devin B. Pettigrew when using or adapting this work.

This is a geopackaged project template for archaeological pedestrian reconnaissance using the open-source QField mobile application for QGIS. The geopackage contains the mapping layers and project template to be copied to each new mapping project. Data can be collected on a smartphone or tablet linked to a Bluetooth GPS receiver for improved accuracy and uploaded to QGIS for post-field analysis. The project records an automated field number (fn) for each mapping device and record class. Point, line, and polygon layers contain classes with unique symbols for artifacts, datums, features, etc. For points, lines, and polygons that fall within or intersect a site_boundary polygon, an association field records the site fn associated with those mapped features. Photographs can be taken within the application as child records attributed to each geometry. Site forms with artifact tallies and descriptions of components, setting, etc. can also be recorded. Note that long narratives on a mobile device can be rapidly recorded by dictating with a trainable voice-to-text app, such a FUTO Voice.

Importantly, when you first setup QField on your device, within the QField application go to QField Settings -> Variables, and add a new variable. Call it exactly "device_id" and enter an ID for your device. The automated fn code will begin with the first character of your device_id, so each mapping device used on your project should have an ID that starts with a unique character to avoid fn duplicates. For example, the first artifact recorded for a particular project on "Devin's phone" will have the fn, D-ART001.
 

Note that the following instructions are for QFieldCloud. For the QField cable upload options, see the QField documentation. 

Instructions: 
1) Download the geopackage to a location on your computer and connect it under "Geopackage" in the QGIS browser. 
2) Open the ProjectTemplate from within the geopackage on the browser. 
3) Go to project properties and provide a name for your particular project.
4) Change the CRS for the project, point, line, and polygon layers to match the longitude of your project area. 
5) If you will not have reception in the project area, use the Generate XYZ Tiles (MBTiles) function on QGIS to save a map to a folder on your computer, drop it into the layers panel, and upload it to /Android/data/ch.opengis.qfield/files/QField/basemaps on your device (see further instructions here: https://github.com/opengisch/QField/discussions/5942#discussioncomment-11834073)
6) Finally use the QFieldCloud plugin to create the cloud project. This should save new .gpkg and .qgz files along with a DCIM file in the QField -> Cloud folder on your computer. On QGIS, you will now be working within the cloud .qgz, not the ProjectTemplate. To start a new project, resume steps 2-6.


At this point you can open the project on your mobile device and start mapping. Note that the process is a bit different for the cable upload options in QField. Check the QField documentation. 

In post-field processing, data can be copied from the attribute tables from the different layers. A plugin will be available soon for consolidating these data into a .csv table, as well as creating mapping labels for reports.

Enjoy! Please pass along any feedback to improve the project.