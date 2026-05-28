# Louisville Housing Inequality by Neighborhood

## Project Overview
How do housing conditions vary across Louisville, KY in 2024?  

The project goals are to:
* Assign a Need Index for each census tract based on 2024 household income, rent, rent burden, home value, housing age, and poverty rate, with active construction permits as an outcome variable.
* Compare and contrast findings with visualizations and provide insights.

## How to Setup This Project
### Prerequisites  
* Python 3.10+
* [Git](https://git-scm.com/install/windows)
* [Visual Studio Code](https://code.visualstudio.com/download) (VS Code)  
> This project was developed in VS Code on Windows.

### Setup Instructions

1. Open a terminal (Git Bash, PowerShell, VS Code Terminal, etc.) and navigate to the directory where you want to clone the project. 

2. Create and activate a virtual environment:  

    **Windows**  
    `python -m venv venv`  
    `source venv/Scripts/activate`  
 
    **Linux/macOS**  
    `python3 -m venv venv`  
    `source venv/bin/activate`

3. Clone the repository:  
`git clone https://github.com/Code-You-Contributors/HUD_data_master`  
`cd curtis`

4. Install required dependencies:  
    `pip install -r requirements.txt`

## Running the Project
5. Open the project folder in VS Code.

6. Run the following notebooks **in order** using "Run All":  
    - curtis.ipynb
    - visualizations.ipynb

## Project Details
* The original scope of the project was to analyze data at the neighborhood level in Louisville. However, it proved impossible to 1) accurately convert the census data to neighborhoods and 2) find a neighborhood shapefile containing neighborhood designations/boundaries that covered the entire city (including outer Jefferson county, surburban areas, etc.). Instead, zip codes are used as a visual anchor to better present the visualizations.
* The project looks at and labels pre-1980 house builds as "older housing stock". Housing age by itself does not necessarily equate to poor condition, however, tracts with a higher concentration of older housing stock may indicate greater maintenance needs and infrastructure aging.
* All tract values and percentages use the estimated, median values from the source data.
* Tract 9801 encompasses the Louisville Muhammad Ali Airport, does not have any census data, and will show up noticeably blank in the chloropleths (except for permit counts).

## Conclusions
* Do high-need areas receive more or less development?
* Are lower-income tracts receiving less development while also having older housing stock?
* Which tracts/areas of the city have the highest need index?


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
    - [Zip Code Shapefile](https://louisville-metro-opendata-lojic.hub.arcgis.com/datasets/LOJIC::jefferson-county-ky-zip-codes/explore?location=38.185048%2C-85.582938%2C11)
    - Construction Permits
    - ~~Code Violations~~ - data is only for last 30 days and has no archive available for 2024
    - ~~Vacant Properties~~ - data is outdated and unusable
* [ArcGIS Hub](https://arc-gis-hub-home-arcgishub.hub.arcgis.com/)
    - [Louisville Neighborhood Shapefile](https://arc-gis-hub-home-arcgishub.hub.arcgis.com/datasets/e951c160f4724e379b91c242e7b467b7_0/explore?location=38.217033%2C-85.720880%2C13)
* [Census Shapefiles](https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.html)
    - [Kentucky Tract Shapefile](https://www.census.gov/cgi-bin/geo/shapefiles/index.php?year=2023&layergroup=Census+Tracts)
*[Capital Impact](https://www.ciclt.net/)
    - [Jefferson County Zip Codes and Cities](https://www.ciclt.net/sn/clt/capitolimpact/gw_ziplist.aspx?ClientCode=capitolimpact&State=ky&StName=kentucky&StFIPS=&FIPS=21111)