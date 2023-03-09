# NEON Fish Invasion (Python)
Final Project for MACS401

Using Python to Look at Invasive Fish at NEON Sites

Goals:
The goal for this project is to visualize invasion at different NEON sites, from a scale of 0-1 or 0-100 (depending on the invasion metrics). 
Additionally, this project analyzes three-year nitrate averages against invasion metrics (Spearman's correlation coefficient since it's non-parametric data)
A working point for this project is using a for loop to create plots of observed fish lengths against FishBase reported Maximum Total Length to compare if lengths are falling within the range of site lengths

This project is a continuation of work that I'm doing in R. This work is using statistics to look at functional traits, phylogenetic traits (e.g. phylogenetic diversity), land-use data, and anthropogenic impacts on invasion. Invasive species can be economically and ecologically devestating. Additionally, with an increasingly global trade and travel system, understanding community relationships can be vital to ensuring biodiversity preservation and ecological strength. Aquatic species specifically pose an interest to fisheries, sport fishing, and ecological impacts. Despite a barrier of land, the interconnectedness of global water can spread invasive species into vulernable aquatic ecosystems. Compounding factors such as stocking increase the impact that invasive fish can have on human and ecological systems. 

I am using data from NEON and the U.S. Census for this project. As some of this data has already undergone analysis in Excel and R, all files will be included in this GitHub repository. U.S. Census data is a shapefile of the U.S. used as a basemap. NEON data includes data on fish observation, invasion status (added in independently by members of my research team), site nitrate measurements, site locations (latitude and longitude in WGS83). Additionally, I pull in data from FishTraits Database, which is a repository of information on different fish species. I have added entries into this database to supplement a full view of relevant NEON species.

I will use .csv manipulation using Pandas. Using GeoPandas, I will create maps that visualize invasion. I will also use Numpy and Scipy to perform some statistical tests, such as Spearman's correlation coefficient. Time permitting, I will also use these packages to attempt ANOVA between maximum length and mean site length. I'll use Matplotlib to plot. 

This process has increased my understanding of how to use programs to sift through large datasets. It has also been interesting to translate R knowledge (e.g. piping in dplyr() to deal with .csv files into knowledge of pandas() for processing .csv files). I have also started to learn about the process of memory-intensive processing, and how to streamline code.

References
NEON data portal : https://www.neonscience.org/data 
Fish Traits database : https://www.sciencebase.gov/catalog/item/5a7c6e8ce4b00f54eb2318c0 
