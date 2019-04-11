# Creating_Isochrones_in_QGIS.py

## Creates individual isochrones with v.net.iso tool
when we use v.net.iso tool to create isochrones, we face four issues.
1. v.net.iso does not create isochrones from individual points. We should create isochrones one by one point
2. The output is the whole network layer. We should filter isochrones by attribute 'cat' values
3. The lines of output are seaprated each other. We should merge the lines to one feature.
4. The attribute values of output do not inherit the attributes of the original points

The python script can solve these problems and save the results.
Every step is processed in PyQGIS automatically.

## Usage
The script works in Python console in QGIS and needs upto QGIS version 3.
The algorithm uses GRASS 7 module (Geographic Resources Analysis Support System).
If GRASS is not installed in QGIS, install it in QGIS plugins.
