# Data512_Wildfire_Project

## Instructions:

Please utilize the link to the ipynb file running all modules:
- Please run this first : Wild_fire_aquisition_and_Smoke_Estimate_Howard.ipynb
- Then secondly run: AQI_Request_Howard.ipynb
- Also per assignment instructions please read : Common_analyis_part1_reflection.pdf

Link to project : https://drive.google.com/drive/folders/1ibE73MRTthdDTecKCEYTUSHyrlLfKUqc?usp=drive_link


## Describe the goal of the project.

### Goal:


The course project entails an in-depth examination of the repercussions of wildfires on a specific U.S. city.
Because the western United States has experienced an increasing frequency of summers marked by wildfires, resulting in smoke spreading across numerous western states. Various factors have been suggested as potential causes, including climate change, U.S. forestry policies, and heightened awareness, among others. The ultimate objective is to provide valuable insights to policymakers, city administrators, city councils, and other civic institutions, enabling them to make well-informed decisions regarding the development of strategies to mitigate future wildfire impacts. As part of this project I looked into Idaho, Coeur d'Alene annually form 1936 to present. 

## List the license of the Professor source data and a link to the Wildefire Geo data: 

#### Professors License:
https://drive.google.com/file/d/1qNI6hji8CvDeBsnLDAhJXvaqf2gcg8UV/view?usp=sharing
https://drive.google.com/file/d/1bxl9qrb_52RocKNGfbZ5znHVqFDMkUzf/view?usp=sharing
"This code examples were developed by Dr. David W. McDonald for use in DATA 512, a course in the UW MS Data Science degree program. These code files were provided under the Creative Commons CC-BY license. Revision 1.2 - August 14, 2023"

#### Link to all relevant API documentation URLS: 
https://www.sciencebase.gov/catalog/item/61aa537dd34eb622f699df81
https://docs.google.com/spreadsheets/d/1cmTW5fgU3KyH6JbrRao-qWjzu2GovKk_BkA7a-poGFw/edit?usp=drive_link
https://drive.google.com/file/d/1TwCkvdaw0MxJzW7NSDg6XxYQ0dvaS44I/view?usp=sharing
https://www.airnow.gov/sites/default/files/2020-05/aqi-technical-assistance-document-sept2018.pdf

#### mla citation :
Also used  GEEKS FOR GEEKS as a mla citation:
“Matplotlib Tutorial.” GeeksforGeeks, 22 Jun. 2023. https://www.geeksforgeeks.org/matplotlib-tutorial/#. Accessed 7 Nov. 2023. 


## Clearly name any intermediary data files and any final output files that your code creates, and for any files that your code :


#### Used perlimnary: files

- Title: USGS_Wildland_Fire_Combined_Dataset.json
- Reader.py (Instructor object class) 

#### Outout Files and Graphs:

##### 3 Pictures in png:

-Wildfires estimates and aqi from Idaho, Coeur d'Alene.png
-total acres burned per year from Idaho, Coeur d'Alene.png
- Number_of_Wild_Fires_Annually_from_Idaho,_Couer_d'Alene.png

#####  files: 
via month
 - coeur_smoke_estimate_df.csv :
- Idaho_Coeur_d'Alene_Fires.csv geopull request
- subsets:
Idaho_Coeur_d'Alene_Fires[o].json
Idaho_Coeur_d'Alene_Fires[1].json
Idaho_Coeur_d'Alene_Fires[2].json

- particulate_aqi.csv
 
## creates you should describe the values of all fields.:

-particulate_aqi: 
[year month :the attempted particle year from 1963 to 2023 written a "year-month-day" as string
 aqi : the list of daily aqi's as n float 64
]

- coeur_smoke_estimate_df.csv
[ Fire_Year : the object from 163 to 2022 of wilde fires 
GIS_Acres : the pologyon gis area in float 64 from 1963 to 2022
Shortest_distance: the shorest distance from the constraint of 1250 miles float 64 object from 1963 to 2022
Average_distance: the average distance from the 1250 miles limit constraint in float 64
Smoke_estimate : The smoke estimate of fires for my city from 1963 to 2022 float64 the formula (area/distance)^squared
 ]

 List any known issues or special considerations with the data that would be useful for another researcher to know:
Collab collapsed when running the reader object once, required me to switch to ipynb files. Also additional AQI particulate and (Gaseous was not used had only 10 rows) contained very little to know data so averages were filed null positions. 
