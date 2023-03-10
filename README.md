# NEON Fish Invasion (Python)
## Final Project for MACS401

### Using Python to Look at Invasive Fish at NEON Sites

### Goals
The goal for this project is to visualize invasion at different NEON sites, from a scale of 0-1 or 0-100 (depending on the invasion metrics). 
Additionally, this project analyzes three-year nitrate averages against invasion metrics (Spearman's correlation coefficient since it's non-parametric data). This project also uses a for loop to create plots of observed fish lengths against FishBase reported Maximum Total Length to compare if lengths are falling within the range of site lengths. There are no stats tests associated with these plots, since it compares maximum total length and several observed lengths. However, these plots are allowing me to flag species that may have some data discrepancies.

### Background
This project is a continuation of work that I'm doing in R using National Ecological Observatory Network (NEON) data. This work is using statistics to look at functional traits, phylogenetic traits (e.g. phylogenetic diversity), land-use data, and anthropogenic impacts on invasion. Invasive species can be economically and ecologically devestating. Additionally, with an increasingly global trade and travel system, understanding community relationships can be vital to ensuring biodiversity preservation and ecological strength. Aquatic species specifically pose an interest to fisheries, sport fishing, and ecological impacts. Despite a barrier of land, the interconnectedness of global water can spread invasive species into vulernable aquatic ecosystems. Compounding factors such as stocking increase the impact that invasive fish can have on human and ecological systems. I have previously created invasion metrics. Relative invasive abundance is calculated by sum of reported invasive observations divided by sum of reported total observations. Relative invasive richness is calculated by number of invasive species divided by snumber of species total at each NEON site.

### Data Sources
I am using data from NEON and the U.S. Census for this project. As some of this data has already undergone analysis in Excel and R, all files will be included in this GitHub repository. U.S. Census data is a shapefile of the U.S. used as a basemap. NEON data includes data on fish observation, invasion status (added in independently by members of my research team), site nitrate measurements, site locations (latitude and longitude in WGS83). Additionally, I pull in data from FishTraits Database, which is a repository of information on different fish species. I have added entries into this database to supplement a full view of relevant NEON species.

### Method and Approach
I use .csv manipulation using Pandas. Using GeoPandas, I also created maps that visualize invasion. I will also use Numpy and Scipy to perform some statistical tests, such as Spearman's correlation coefficient. Using a for loop, I was able to create an automated process to create plots of observed vs expected fish lengths. This will allow me to assess the accuracy of my FishTraits augmentations as well as flag some potential issues with combining these datasets.
A note: the final plots may not show up within the .ipynb Jupyter notebook or in the Binder hub. This is due to a memory warning from mpl since this code creates more than 20 plots. Executing this code in Jupyter Notebook should have no issue running and showing this code.

### Results
The invaded/not invaded map shows that 19 out of 28 sites are invaded. The spectrum maps detail the extent of invasion, as calculated by relative invasive abundance and relative invasive richness. The nitrate graphs show that there is no statistically significant correlation between nitrate and invasion status at NEON sites. Lastly, plots from the for loop show that there are some discrepancies. For example, *Gambusia affinis* shows that observed fish lengths are larger than the maximum length reported in FishTraits database. This suggests that further reports are needed to verify *G. affinis's* maximum field length reports are accurate, and that reported observations are accurate. Flagging these species will further my research and strengthen the accuracy of conclusions. 

### Learning Moments
This process has increased my understanding of how to use programs to sift through large datasets. It has also been interesting to translate R knowledge (e.g. piping in dplyr() to deal with .csv files into knowledge of pandas() for processing .csv files). I have also started to learn about the process of memory-intensive processing, and how to streamline code. This project also exposed me to for looping to automate plot creation, which is a tactic I'll be utilizing in the future.

### References
NEON data portal : https://www.neonscience.org/data \
Fish Traits database : https://www.sciencebase.gov/catalog/item/5a7c6e8ce4b00f54eb2318c0 


### Interactive Jupyter Notebook: 
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/bdubs4/MACS401_EODA_final/HEAD)

