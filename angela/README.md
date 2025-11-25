# Unsafe Outdoors: An Analysis of Extreme Temperature and Ozone Conditions in Louisville to Support Emergency Shelter Planning

## (added areas with ??? to remind myself to add to sections as project progresses)
---
### Objective:
This project analyzes temperature and ozone data in the Louisville Metro area to identify days when outdoor conditions become unsafe, particularly for individuals experiencing homelessness. By quantifying the frequency and severity of extreme weather and poor air quality, this project aims to provide data-driven evidence that supports the need for accessible indoor shelter and emergency response strategies during hazardous environmental conditions.

---
### Project Overview:

People without stable housing are disproportionately exposed to environmental risks. Extreme heat, extreme cold, and elevated ozone levels can lead to serious health complications, hospitalizations, and preventable deaths.

This project uses publicly available temperature and ozone measurements from the Louisville Metro area to:

- Identify periods of extreme heat, extreme cold, and unsafe ozone levels

- Categorize weather conditions by heat index, windchill, and ozone alerts

- Determine the number of “unsafe outdoor days”

- Visualize patterns across months and seasons

- Highlight trends that may increase shelter demand

- ??? more here?

- ??? more here?

The findings are intended to support organizations who provide or coordinate indoor shelter options during hazardous environmental conditions. Ultimately, this analysis underscores a simple truth backed by data: on certain days, being outdoors is not just uncomfortable — it’s dangerous.


---

### Project Setup Instructions:
Copy the code link to this repository and clone to your computer.

Open the repository folder in a code editor; and create the virtual environment in that folder.

Create and Activate a Virtual Environment (commands in table below)

Install the `requirements.txt` file

Open `angela.ipynb`

-??? (add more here)?

When you are finished, deactivate the virtual environment and close the repository folder.


## Virtual Environment Commands

|  **Command**	 |         **Linux/Mac**	         |         **Windows/GitBash**       |
| -------------- | -------------------------------   | -------------------------------   |
| Create         | `python -m venv venv`	                 | `python -m venv venv`             |
| Activate	     | `source venv/bin/activate`	     | `source venv/Scripts/activate`    |  
| Install	     | `pip install -r requirements.txt` | `pip install -r requirements.txt` |
| Deactivate	 | `deactivate`	                     | `deactivate`                      |


---
### Data Summary:

**Total Records:**\
*temperature dataset*: 366 rows, 9 columns\
*ozone dataset*: 2243 rows, 21 columns\
*humidity and windchill dataset*: 14404 rows, 125 columns

**Date Range:**\
*Daily data* from Jan 1, 2024 through Dec 31, 2024

**Basic Stats:**\
*Temperature(including heat index and windchill) in °F*:\
min: -11.3\
mean: 60.3 \
max: 123 

*Ozone Levels(AQI values)*:\
min: 12\
mean: 42.9\
max: 156

---
### Data Dictionary (from cleaned data):
Variables from **full_df** (combines all 3 datasets):

- **Date** (datetime64)- The calendar date of the recorded weather and air quality measurements. Each row represents a single day in the Louisville Metro area. 
- **Max_Temp** (int64)- The highest measured air temperature (°F) for that day.
- **Min_Temp** (int64)- The lowest measured air temperature (°F) for that day.
- **Average_Humidity** (float64)-The mean relative humidity (%) for the day. Higher humidity affects the heat index.
- **Sust_Wind_Speed** (float64)- The average sustained wind speed (mph) throughout the day. Wind can influence wind chill and exposure risks.
- **AQI_Value** (float64)- The Air Quality Index value for the day, representing overall air pollution levels. Scale 0-200. 100 or above indicates unsafe air.
- **Substance_Measured** (object)- The primary pollutant measured for the AQI value. Helps identify which pollutant drove the AQI rating. (this data looks specifically at Ozone)
- **Wind_Chill** (float64)- The perceived temperature (°F) when cold air and wind combine. Windchill 35 or below indicates extreme weather and increases health risk.
- **Heat_Index** (float64)- The perceived temperature (°F) when temperature and humidity combine. Heat index 95 or higher indicates extreme weather and increases health risk.
- **Extreme_Weather** (bool)- Indicates whether the day meets defined criteria for dangerous outdoor conditions
- **Month** (object)- The month extracted from the date. Used for grouping, and trend visualization.
- **Feels_Like** (float64)- A calculated metric representing perceived temperature based on Max_Temp, Wind_Chill, or Heat_Index depending on conditions. Used to classify temperature risk more realistically.
- **Temperature_Category** (object)- A labeled category (e.g., “Extreme Cold,” “Warm,” “Hot”) based on the Feels_Like value and defined temperature bins. Helps visualization of temperature trends.

---
### Technologies Used:
Languages & Core Libraries:\
*Python* – primary language for data analysis and project development\
*Pandas** – for data cleaning, transformation, and analysis

Visualization Tools:\
Matplotlib* – for basic charts and visualizations

--??? others?

Development Environment:\
*Jupyter Notebook* – for exploratory data analysis and documenting workflows\
*VS Code* – for script development and file management

Version Control & Documentation:\
*Git & GitHub* – for version control and project sharing\
*Markdown* – for notes, documentation, and explanations



---
### Data Sources:


**Dataset #1**: 2024 Louisville Daily Max and Min Temperatures

Source: https://www.ncdc.noaa.gov/cdo-web/search

**Dataset #2**: 2024 Louisville Daily Ozone Readings

Source: https://www.epa.gov/outdoor-air-quality-data/download-daily-data

**Dataset #3**: Louisville International Airport Climatological Data- contains wind speed and humidity

Source:  https://www.ncei.noaa.gov/access/search/data-search/local-climatological-data-v2?pageNum=1&dataTypes=DailyAverageRelativeHumidity&dataTypes=DailyMaximumDryBulbTemperature&dataTypes=DailyMinimumDryBulbTemperature&dataTypes=DailyPeakWindSpeed&dataTypes=DailySustainedWindSpeed&startDate=2024-01-01T00:00:00&endDate=2024-12-31T23:59:59&bbox=38.469,-85.965,38.043,-85.539


