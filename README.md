# Green-Areas
This model takes green_area polygons supplied by the user, clips the data to the domain and ensures the data is in the correct projection.
Spatial green areas can be used in the same way. If spatial green-areas are used the polygon must have a "Value" parameter with the parameters associated with this value given in infiltration.csv.

## Description
The CityCAT model can use green_area polygons to determine permeability. This model accepts green_area data in .gpkg format, clips the data to the selected area, and ensures all data is in the same projection. If the file sizes are too large, multiple .gpkgs can be added directly, or zipped.

## Input Parameters
*Permeable_areas
  * Description: are the green_areas defined as being polygons (i,e using the supplied data) all permeable or all impermeable? If green_areas is supplied then polygons is used (and output as a parameter) whatever value is input here. 

## Input Files (data slots)
* Green_areas
  * Description: A .gpkg file of the green_areas (or spatial green_areas). If Spatial green areas are used the polygon must have a "Value" parameter with the parameters associated with this value given in infiltration.csv
  * Location: /data/inputs/green_areas
* Boundary
  * Description: A .gpkg of the geographical area of interest. 
  * Location: /data/inputs/boundary
* Parameters
  * Description: location and projection
  * Location: /data/inputs/parameters

## Outputs
* The model should output should have a single .gpkg file of the chosen area containing the green_areas (or spatial green_areas of interest. If Spatial green areas are used an infiltration.csv is coped from the input data
  * Location: /data/outputs/green_areas
* the model should output a greenareas parameter file specfiy how green_areas are used in CityCAT
  * Location: /data/outputs/parameters
