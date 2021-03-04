# Webscraping with spatial data - Bergfex

![](Teaser_Bergfex.png)

This repository documents the webscraping of Bergfex webpage adding snow level information to each activity. It was elaborated by Malwina San José, Tiffany Carruthers and Sarah Dutschke. The information presented here is not approved for any kind of commercial use.

Project Team
-----------

[Sarah Dutschke](https://www.linkedin.com/in/sarah-dutschke/), 
[Malwina San José](https://www.linkedin.com/in/malwina-san-josé/),
[Tiffany Carruthers](https://www.linkedin.com/in/tiffanycarruthers/)

Partners
 -------
[Bergex](https://www.bergfex.com/) is a company that provides a wide range of information about mountains (such as mountain activities, weather information, accommodation options etc.).

Project description
-------------------
Planning a winter time hikes can be complicated in Switzerland. Sometimes hiking in the snow is an exciting adventure, but it can also be an unexpected surprise. There is no shortage of trail databases that contain information about how long or how difficult a trail is, however finding up to date information about snowfall data on these trails can be tedious. This notebook solves the snowline problem by scraping GPX data from bergfex.com and meteocentrale.ch. 

Weather GPS data is obtained from multiple weather towers across Switzerland that publicly provide current weather data. Since these towers are located in a specific latitude and longitude, an approximate chance of snowfall was assumed based on the distance from the tower and altitude. If a trail is within a certain distance from a tower, and is also at a certain altitude then it will be tagged with a snow alert. This was implemented by finding the closest hiking trails to a tower that has reported snow.

XXX potentially show visualization / dashboard...

Project Milestones
-------------------
### Milestone 1
Scraping the Bergfex.com website in order to create Pandas dataframes that contain important information about each trail. This code uses BeautifulSoup to parse the html tags into json, which is easier to work with. A for-loop iterates over each html tag and adds the corresponding information into empty lists. Data is cleaned and an initial data analysis is performed.

 ### Milestone 2
 Scraping the snow level data from XXX website in order to create Pandas dataframes that contain the snow level for XXX weather stations around Switzerland.
 
 ### Milestone 3
 Overlay the data form Milestone 1 and 2 to assess whether a certain activity has a snow alert or not.
 
 Outcomes
 ---------
As the final outcome of this project, we created three jupyter notebooks (one for each Milestone). With the help of these, XXXX for the entire data base can be created with one command. 

Example plots
---------
![](barplot_1.png)
![](treemap_1.png)
![](barplot_2.png)
![](treemap_2.png)

Requirements
------------
The libraries required to run this product are the following (details in environment.yml and environment2.yml):
  - ipykernel
  - pandas

XXX to update
  
  
Repository Structure
------------
    ├── README.md       <- top-level README file for anybody interested in this project
    ├── notebooks       <- one notebook for each Milestone
    ├── data            <- csv files, created based on each of the notebooks
    ├── environment.yml <- environment file that lists the channels and dependencies needed for this project
    ├── environment2.yml <- detailed environment file that contains specific versions used for this project
