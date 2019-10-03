# Assignment 5: BI Clients & Data Processing.

Gruppe Dangerous Memory: Jake, Christian, Alexander

https://github.com/datsoftlyngby/soft2019fall-bi-teaching-material/tree/master/week39/assignment_5


## How to run project 

1. Download, install and launch Pentaho as described [here](https://github.com/datsoftlyngby/soft2019fall-bi-teaching-material/tree/master/week39/assignment_5)

2. unzip/unpack the two files: "osm_export.zip" and "boliga_all.zip" 

3. Open Pentaho and import the file "assignment_5.xml"

4. change various paths to correspond with your local settings & locations

5. Press F9 key in Pentaho to run - the file "boliga_with_lat_lon.csv" should be generated

## Assignment Notes
- see [assignment_5.xml](assignment_5.xml) for comments to see what is happening..
- Write 5-10 lines of text discussing how this XML file could be useful, consider aspects like continuous integration/delivery, cron jobs, integration of data sources etc:
    - The xml file makes it possible to export the logic of the operations, from a local development environment into a CI pipeline - or simply to another developers development environment.
    - A pentaho instance could thereby be running in the pipeline as an automated part of a companys [continuous integration pipeline](https://support.pentaho.com/hc/en-us/articles/360007004051-Driving-DevOps-Success-with-Continuous-Integration)
    - This makes it possible to integrate and execute the processing in different ways, and without user interaction through a GUI, but executed on demand programmatically. 

## Developer notes

- Had to add ",row" to header row in "osm_export.csv" for the csv to be loaded correctly.
- Change type for "lon" and "lat" column to String (not sure if really needed)
- Switch off "lazy conversion" from csv input to avoid  "There was a data type error: the data type of [B object [[B@d1930e] does not correspond to value meta [String(34)]"

