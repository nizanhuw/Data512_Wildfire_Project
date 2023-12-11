# Data512_Wildfire_Project

## Goal: Coeur d'Alene, Idaho 
The course project entails an in-depth examination of the repercussions of wildfires on a specific U.S. city.
The western United States has experienced an increasing frequency of summers marked by wildfires, resulting in smoke spreading across numerous western states. Various factors have been suggested as potential causes, including climate change, U.S. forestry policies, and heightened awareness. The ultimate objective is to provide valuable insights to policymakers, city administrators, city councils, and other civic institutions, enabling them to make well-informed decisions regarding developing strategies to mitigate future wildfire impacts. As part of this project, I looked into Idaho and Coeur d'Alene annually from 1936 to the present. 

## License, USGS, and AQI Information: 

#### Professor License:
Dr. David W. McDonald developed these code examples for use in DATA 512,
a course in the UW MS Data Science degree program. 
These code files were provided under the Creative Commons CC-BY license. 
Revision 1.2 - August 14, 2023" :

-	Delegation of city Coeur d’ Alene: Spreadsheet contains the designated city chosen for the Wildfire project
https://docs.google.com/spreadsheets/d/1cmTW5fgU3KyH6JbrRao-qWjzu2GovKk_BkA7a-poGFw/edit#gid=1247370552

-	Calculating geo proximity example: Google Collab link  that provides an example of how to calculate the geographical proximity from a location  https://drive.google.com/file/d/1qNI6hji8CvDeBsnLDAhJXvaqf2gcg8UV/view
  
-	AQI air quality pull request example: Google Collab link that provides an example of requesting an AQI page view request. https://drive.google.com/file/d/1bxl9qrb_52RocKNGfbZ5znHVqFDMkUzf/view

-	Wildfire USGS reader example: zip file containing functions to help read the UTF-source code of USGS file. The Reader.py was used in my code, located in the preliminary_data/Reader.py directory path. https://drive.google.com/file/d/1TwCkvdaw0MxJzW7NSDg6XxYQ0dvaS44I/view
  
-	Delegation of city Coeur d’Alene: The spreadsheet contains the designated city chosen for the Wildfire project.  https://docs.google.com/spreadsheets/d/1cmTW5fgU3KyH6JbrRao-qWjzu2GovKk_BkA7a-poGFw/edit#gid=1247370552

#### AQI:
- The US Environmental Protection Agency (EPA) Air Quality Service (AQS) API. https://docs.airnowapi.org/ 
This is a historical API and does not provide real-time air quality data. Page requests were utilized to collect the AQI particle index. 
This open-source information provided by https://www.airnow.gov/

#### USGS:
- United States Geological Survey USGS Combined wildland fire datasets for the United States and certain territories, 1800s-Present (combined wildland fire polygons) is an open-source US public domain dataset containing the comprehensive data set of fires of polygon and attributes. The data file titled USGS_Wildland_Fire_Combined_Dataset.json is Coeur D’ Alene city located in the directory path preliminary_data USGS_Wildland_Fire_Combined_Dataset.json. Link: https://www.sciencebase.gov/catalog/item/61aa537dd34eb622f699df81

#### MLA Citations :
- I also used  GEEKS FOR GEEKS as an MLA citation:
“Matplotlib Tutorial.” GeeksforGeeks, 22 Jun. 2023. https://www.geeksforgeeks.org/matplotlib-tutorial/#. Accessed 7 Nov. 2023. 

- For the Data Descriptions from USGS_Wildland_Fire_Combined_Dataset.json
“Combined Wildland Fire Datasets for the United States and Certain Territories, 1800s-Present (Combined Wildland Fire Polygons) - ScienceBase-Catalog.” Www.sciencebase.gov, www.sciencebase.gov/catalog/item/61aa537dd34eb622f699df81. Accessed 11 Dec. 2023.

‌


## Instructions:

### For Common Analysis Part 1 
Please utilize the link to the ipynb file running all modules in the Source code folder:

The source code folder contains the following ipynb files to run in a specific order:
- Reader.py: Instructor's python `object` function from the Wildfire.zip to read in USGS GEO called and imported in     
  Wild_fire_aquisition_and_Smoke_Estimate_Howard.ipynb
  
- Please run this first: Wild_fire_aquisition_and_Smoke_Estimate_Howard.ipynb
  This file contains the process of collecting reader.py and USGS_Wildland_Fire_Combined_Dataset.json in the intermediate_data folder.
  This collects information from these files to produce coeur_smoke_estimate_df.csv in the Data_Results folder. Creates smoke estimations
  for Coeur D'Alene moke estimations and files used to collect an AQI. 
  
- Then secondly run: AQI_Request_Howard.ipynb
  This file contains the .ipyb. It requests a daily summary view count of an AQI page from 1984 to the present, creating particulate_aqi.csv in 
  Intermediate_data folder. In addition, it reads in coeur_smoke_estimate_df.csv to create visuals to compare the AQI result and the smoke estimations 
  for predicted future years using linear regression found in the Report_Results directory. 
  
- Per assignment instructions, please read Common_analyis_part1_reflection.pdf in the Report_Results directory.
  The report contains overall findings from the visuals, thoughts, and collaboration feedback. 
  
### For Common Analysis Part 2-3 (Implementation)
- Please Run .... file in the source code results
  This file contains
  
- Please read the .pdf in the report results folder
  This file contains

## Intermediate_data folder 
#### Preliminary_downloads

- **USGS_Wildland_Fire_Combined_Dataset[0][1][2].json** [Includes more than 15 + columns dictated columns collected] broken down into three files because of space constraints
  Date Description is taken from: Combined Wildland Fire Datasets for the United States and Certain Territories metadata, 1800s-Present (Combined Wildland Fire Polygons) - ScienceBase-Catalog. `Columns`:

>`OBJECTID`: Unique identification for the polygon and its attributes.
>
>`USGS_Assigned_ID`: A unique identification was assigned for the polygon and its attributes. 
>
>`Assigned_Fire_Type`:  assigned fire type: Wildfire, Likely Wildfire, Unknown - Likely Wildfire, Prescribed Fire, Unknown - Likely Prescribed Fire
>
>`Fire_Year`: The calendar year when the dataset creators determined the fire occurred
>
>`Fire_Polygon_Tier`: The tier from which the fire polygon was generated. 
>
>`Fire_Attribute_Tiers`: A list of all tiers where a polygon intersects the current fire perimeter in space and time
>
>`GIS_Acres`: The GIS calculated acres of the fire polygon.
>
>`GIS_Hectares`: The GIS calculated hectares of the fire polygon 
>
>`Listed_Fire_Types`: The number of features contributing to the specific fire type is in parentheses after the fire type.
>
>`Circle_Flag`:An ArcGIS Tabulate Intersection Tool was used to identify areas that burned with >10% overlap of the current fire within 1 or 2 years of the current burn 
>
>`Circleness_Scale`: A measure of a polygon's similarity to a true circle. calculated using the Shape_Length and Shape_Area fields.
>
>`Shape_Length`: Automatically calculated perimeter length in meters
>
>`Shape_Area`: Automatically calculated polygon area in square meters


- **Idaho_Coeur_d'Alene_Fires.csv `Columns`**

>`Assigned_Fire_Type`:  assigned fire type: Wildfire, Likely Wildfire, Unknown - Likely Wildfire, Prescribed Fire, Unknown - Likely Prescribed Fire
>
>`GIS_Hectares`: The GIS calculated hectares of the fire polygon 
>
>`Circle_Flag`:An ArcGIS Tabulate Intersection Tool was used to identify areas that burned with >10% overlap of the current fire within 1 or 2 years of the current burn 
>
>`Circleness_Scale`: A measure of a polygon's similarity to a true circle. calculated using the Shape_Length and Shape_Area fields.
>
>`Shape_Length`: Automatically calculated perimeter length in meters
>
>`Shape_Area`: Automatically calculated polygon area in square meters
>
>`Fire_Year`: the object from 163 to 2022 of wildfires
>
>`GIS_Acres`: the polygon gis area in float 64 from 1963 to 2022
>
>`Shortest_distance`: the shortest distance from the constraint of 1250 miles float 64 objects from 1963 to 2022
>
>`Average_distance`: the average distance from the 1250 miles limit constraint in float 64

- **Idaho_nacis_code72.csv** Food and Accomdiation Servies `columns`
>`Number of employees`: the number of employees in a workplace.
>
>`Number of Establishments`: the state's business amount.
>
>`year`: the annual date from 1978 to 2020.
>
> `Net Job Creation`: Rate of job creation net within the last 12 months. 
>
>`Rate of Job loss`: Rate of net job loss within the last 12 months. 
>

- **NAICS_71.csv** Arts Entertainment and Recreation `columns`
>`Number of employees`: the number of employees in a workplace.
>
>`Number of Establishments`: the state's business amount.
>
>`year`: the date annual from 1978 to 2020.
>
> `Net Job Creation`: Rate of job creation net within the last 12 months. 
>
>`Rate of Job loss`: Rate of net job loss within the last 12 months. 
>

- **Real_GDP_NAICS72.csv** Food and Accomdiation Servies `columns`
>`Real_GDP_Quaterly`: the real annual GDP in millions quarterly     float64
>
>`Quarter`:  the quarter out of 4 in which the GDP amount is calculated              object
>
>`Date`:  the date, month, day, year              object
>
>`Annual Real GDP`:    the real annual GDP in millions annually   float64

- **real_GDP_NAICS71.csv** Arts Entertainment and Recreation `columns`
>`Real_GDP_Quaterly`: the real annual GDP in millions quarterly     float64
>
>`Quarter`:  the quarter out of 4 in which the GDP amount is calculated              object
>
>`Date`:  the date, month, day, year              object
>
>`Annual Real GDP`:    the real annual GDP in millions annually   float64
  
## Data_Results folder

#### Created_for_analysis and saved for visuals and regression

- **coeur_smoke_estimate_df.csv** : `Columns`
>`Fire_Year`: the object from 163 to 2022 of wildfires
>
>`GIS_Acres`: the polygon gis area in float 64 from 1963 to 2022
>
>`Shortest_distance`: the shortest distance from the constraint of 1250 miles float 64 objects from 1963 to 2022
>
>`Average_distance`: the average distance from the 1250 miles limit constraint in float 64
>
>`Smoke_estimate`: The smoke estimate of fires for my city from 1963 to 2022 float64 the formula (area/distance)^squared

- **particulate_aqi.csv**: `Columns`
>` year month`: the attempted particle year from 1963 to 2023 written a "year-month-day" as a string
>
>`AQI`: the list of daily AQIs as n float 64

-**cleaned_NACIS72_df.csv** Food and Accomdiation Servies `columns`
>`Number of employees`: the number of employees in a workplace.
>
>`Number of Establishments`: the state's business amount.
>`year`: the date annual from 1978 to 2020.
>
> `Net Job Creation`: Rate of job creation net within the last 12 months. 
>
>`Rate of Job loss`: Rate of net job loss within the last 12 months. 
>
>`Smoke_estimate`: The smoke estimate of fires for my city from 1963 to 2022 float64 the formula (area/distance)^squared
>
>`Annual Real GDP`:    the real annual GDP in millions annually   float64
  

-**NAICs71_cleaned.csv** Arts Entertainment and Recreation `columns`
>`Number of employees`: the number of employees in a workplace.
>
>`Number of Establishments`: the state's business amount.
>`year`: the date annual from 1978 to 2020.
>
> `Net Job Creation`: Rate of job creation net within the last 12 months. 
>
>`Rate of Job loss`: Rate of net job loss within the last 12 months. 
>
>`Smoke_estimate`: The smoke estimate of fires for my city from 1963 to 2022 float64 the formula (area/distance)^squared
>
>`Annual Real GDP`:    the real annual GDP in millions annually   float64
  

## Report Results contain the following files: 

#### Common Analysis Part 1: 
- **Wildfire estimates and AQI from Idaho, Coeur d'Alene.png**:
This file contains the Wildfire estimates and AQI from Idaho Coeur d'Alene
- **total acres burned per year from Idaho, Coeur d'Alene.png**:
This file contains the total acres burned per year from Idaho, Coeur d'Alene.png
- **Number_of_Wild_Fires_Annually_from_Idaho,_Couer_d'Alene.png'**:
This file contains Number_of_Wild_Fires_Annually_from_Idaho,_Couer_d'Alene.png
- **'Common_analyis_part1_reflection.pdf**:
  This pdf file contains the Common_analyis_part1_reflection
  
#### Common Analysis Part 3 implementation 
* Add
- Common analysis presentation. pptx
This file contains 
- Common analysis part 4 Report
This file contains 

## Limitations 
-  AQI particulate and gaseous (not used because it had only 10 rows) contained very little to no data, so averages were filed where null positions were seen.
- Code run time for Project Part 1 files takes 3+ hours per file. 
- USGS JSON file downloads take 1+ hour to cultivate download and place in subset JSON files to be read in part 1 of the project.
- Parts 2-3 of the implementation analysis contain data scarcity, so the results of all regressions do not have fully linear covariance assumptions.

 
