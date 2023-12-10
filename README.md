# Data512_Wildfire_Project


## Instructions:

### For Common Analysis Part 1 
Please utilize the link to the ipynb file running all modules in the Source code folder:

The source code folder contains the following ipynb files to run in a specific order:
- Please run this first: Wild_fire_aquisition_and_Smoke_Estimate_Howard.ipynb
  This file contains
  
- Then secondly run: AQI_Request_Howard.ipynb
  This file contains
  
- Also, per assignment instructions, please read Common_analyis_part1_reflection.pdf in the report results
  The report contains 
  
### For Common Analysis Part 3 (Implementation)
- Please Run .... file in the source code results
  This file contains
  
- Please read the .pdf in the report results folder
  This file contains
  
### Goal: Coeur d'Alene
The course project entails an in-depth examination of the repercussions of wildfires on a specific U.S. city.
The western United States has experienced an increasing frequency of summers marked by wildfires, resulting in smoke spreading across numerous western states. Various factors have been suggested as potential causes, including climate change, U.S. forestry policies, and heightened awareness. The ultimate objective is to provide valuable insights to policymakers, city administrators, city councils, and other civic institutions, enabling them to make well-informed decisions regarding developing strategies to mitigate future wildfire impacts. As part of this project, I looked into Idaho and Coeur d'Alene annually from 1936 to the present. 

## Professors License:
Thanks to the notebooks used :
- https://drive.google.com/file/d/1qNI6hji8CvDeBsnLDAhJXvaqf2gcg8UV/view?usp=sharing 
- https://drive.google.com/file/d/1bxl9qrb_52RocKNGfbZ5znHVqFDMkUzf/view?usp=sharing
These code examples were developed by Dr. David W. McDonald for use in DATA 512, a course in the UW MS Data Science degree program.
These code files were provided under the Creative Commons CC-BY license. Revision 1.2 - August 14, 2023"

#### Link to all relevant API documentation URLS: 
https://www.sciencebase.gov/catalog/item/61aa537dd34eb622f699df81
https://docs.google.com/spreadsheets/d/1cmTW5fgU3KyH6JbrRao-qWjzu2GovKk_BkA7a-poGFw/edit?usp=drive_link
https://drive.google.com/file/d/1TwCkvdaw0MxJzW7NSDg6XxYQ0dvaS44I/view?usp=sharing
https://www.airnow.gov/sites/default/files/2020-05/aqi-technical-assistance-document-sept2018.pdf

#### MLA Citations :
I also used  GEEKS FOR GEEKS as an mla citation:
“Matplotlib Tutorial.” GeeksforGeeks, 22 Jun. 2023. https://www.geeksforgeeks.org/matplotlib-tutorial/#. Accessed 7 Nov. 2023. 


## The intermediate data folder contains two subset folders:
#### Preliminary_downloads 
- Title: USGS_Wildland_Fire_Combined_Dataset.json
-  Reader.py (Instructor object class) Taken from the
-  
  This contains the
#### Created_for_anlysis
- coeur_smoke_estimate_df.csv :
[ Fire_Year: the object from 163 to 2022 of wild fires 
GIS_Acres: the polygyon gis area in float 64 from 1963 to 2022
Shortest_distance: the shortest distance from the constraint of 1250 miles float 64 object from 1963 to 2022
Average_distance: the average distance from the 1250 miles limit constraint in float 64
Smoke_estimate: The smoke estimate of fires for my city from 1963 to 2022 float64 the formula (area/distance)^squared
 ]
- Idaho_Coeur_d'Alene_Fires.csv Geo pull request
- subsets:
Idaho_Coeur_d'Alene_Fires[o].json
Idaho_Coeur_d'Alene_Fires[1].json
Idaho_Coeur_d'Alene_Fires[2].json


- particulate_aqi.csv
[year month : the attempted particle year from 1963 to 2023 written a "year-month-day" as a string
 AQI : the list of daily AQI's as n float 64]

## Report Results contain the following files: 

#### Common Analysis Part 1: 
-Wildfire estimates and AQI from Idaho, Coeur d'Alene.png
This file contains the 
-total acres burned per year from Idaho, Coeur d'Alene.png
This file contains the 
- Number_of_Wild_Fires_Annually_from_Idaho,_Couer_d'Alene.png
This file contains 
- Common_analyis_part1_reflection.pdf
  This pdf file contaisn
  
#### Common Analysis Part 3 implementation 
* Add
- Common analysis presentation. pptx
This file contains 
- Common analysis part 4 Report
This file contains 

## Limitations 

 List any known issues or special considerations with the data that would be useful for another researcher to know:
Collab collapsed when running the reader object once, requiring me to switch to ipynb files. Also, additional AQI particulate and (Gaseous was not used had only 10 rows) contained very little to no data so averages were filed null positions. 
