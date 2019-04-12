# Creating_Isochrones_with_Python_Scipt_in_QGIS.py

## Creates individual isochrones with v.net.iso in GRASS
when we use v.net.iso tool to create isochrones, we face four issues.
  1. v.net.iso does not create isochrones from individual points.
  2. The output is the whole network layer. We should filter isochrones by attribute 'cat' values
  3. The lines of output are seaprated each other.
  4. The attribute values of output do not inherit the attributes of the original points

The python script can solve these problems and save the results.\
The process follows these steps.
  1. Load network layer and point layer of starting point for isochrones.
  2. Copy Field names and values from the point layer.
  3. Call a feature of point layer one by one and run v.net.iso.
  4. Remove unnecessary features of output and merge them to one feature.
  5. Paste the field information to the isochrone feature.\
Every step is processed in PyQGIS automatically.\
The algorithm saves all the output of the process.

## Usage
The script works in Python console in QGIS and needs upto QGIS version 3 and python version 3.\
The algorithm uses GRASS 7 module (Geographic Resources Analysis Support System).\
If GRASS is not installed in QGIS, install it in QGIS plugins.
