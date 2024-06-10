# FieldMove Clino
FieldMove is a digital mapping app that has been designed for [Apple](https://apps.apple.com/ch/app/fieldmove-clino/id647463813?l=fr), [Android](https://play.google.com/store/apps/details/FieldMove_Clino?id=com.mve.fieldmove.clino&hl=fr&gl=US) and Windows tablets. 

FieldMove uses the available sensors in a tablet to measure the orientation of planar and linear features (extension fractures, striated planes, ...) with a digital compass clinometer.

## Description
A CSV file stores geo-referenced point data and photo locations in a spreadsheet style layout. When choosing to export as CSV, several files will be output, with each file containing data for a single data type, e.g. line.csv, plane.csv, note.csv.

The first column of each .csv file contains a locailtyID which is assigned to each locality and data point. This can be used to cross reference localities and their associated data.

CSVfiles do not support photos or screenshots. Instead the geographic location and name ofeachphoto is found within the image.csv file. Photos can be found in the Images folder, which is stored in the .fm folder.

CSVfiles can be opened and/or imported into many GIS software packages as CSV/ASCII data. They can also be viewed quickly in simple text editors (i.e. Notepad) or spreadsheet software (i.e. MS Excel).