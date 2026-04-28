# Louisville Housing Inequality by Neighborhood

## Project Overview
How do housing conditions vary across Louisville?  

The project goals are to:
* Assign a rating for each census tract based on household income, rent, rent burden, home value, housing age, active building permits, and property maintenance inspections.
* Compare and contrast findings with visualizations and provide insights.

## Project Details
* The original scope of the project was to analyze data at the neighborhood level in Louisville. However, it proved impossible to 1) accurately convert the census data to neighborhoods and 2) find a neighborhood shapefile containing neighborhood designations/boundaries that covered the entire city (including outer Jefferson county, surburban areas, etc.).

## Data Sources
* [Census / American Community Survey (ACS)](https://data.census.gov)  
    - Household Income B19013
    - Median Gross Rent B25064
    - Median Home Value B25077
    - Poverty Rate S1701
    - Rent Burden B25070
    - Housing Age B25034
    - [Kentucky Tracts Shapefile](https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.2023.html#list-tab-790442341)
    - [Jefferson County Tract Codes 2020](https://www2.census.gov/geo/maps/DC2020/PL20/st21_ky/censustract_maps/c21111_jefferson/)
* [Louisville Open Data](https://data.louisvilleky.gov)
    - Construction Permits*
    - Code Violations
    - Vacant Properties
* [ArcGIS Hub](https://arc-gis-hub-home-arcgishub.hub.arcgis.com/)
    - [Louisville Neighborhood Shapefile](https://arc-gis-hub-home-arcgishub.hub.arcgis.com/datasets/e951c160f4724e379b91c242e7b467b7_0/explore?location=38.217033%2C-85.720880%2C13)


*This analysis uses active construction data as a proxy for investment due to limitations in historical permit data availability.