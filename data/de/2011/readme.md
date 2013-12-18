# "Start here" Readme for DE 2011

Furthermore, all 'input' folders contain a CSV files that store 'dashboard inputs'. These inputs are read into the respective analysis and shape the energy flow of the 'DE 2011' dataset. 
If you want to know what the DE Input Data is based on (references, justifications), please go to our "Source analyses". These can be found on Dropbox, in `Dropbox/Quintel/Projects/Restructure Research Dataset/Etdataset/Source Analyses/DE/2011` (temporary solution, the directory might change). 

## Source analysis content tree

All source analyses mirror the research analyses. In other words: For every research analysis folder on the ETDataset repository, you will find a corresponding Source analysis folder for the specific country and year that justifies the inputs for that particular analysis. 

### 0. Preparation of IEA data

IEA data tables are prepared for the research analysis dataflow. A shift of solar PV generation is undertaken (from main activity sector to residences and services). 

### 1. CHP analysis
Similarly to the CHP analysis, the PP_HP analysis also assigns FLH to power plants, which will determine the installed capacity per plant. Full load hours and installed capacities are very relevant in the ETM, for example in the calculation of the 'loss of load' or 'plant profitability'. 

much of a carrier can be exported or might need to be imported in the future. 



Apart from defining energy flows, the ETM also needs to know several figures that are not of an energetic nature. For example, the ETM needs to know the population and size of a country. 
Area data is stored in a file called nl.ad or de.ad (country.ad). A research analysis that creates this file automatically after prompting user input is not yet available. 


## Shortcomings of the DE dataset

We did not perform extensive source analyses for the research analyses addressing the various sectors. The main purpose in setting up the DE dataset was to show that the research analyses could cope with a non-NL country. Many dashboard inputs are inspired by Quintel's 'old' DE dataset that was not based on this research analysis dataflow. Shortcomings of individual source analyses are mentioned directly in the source analysis. 

The ETM generates certain figures, which are not directly inputted into the dataset. By comparing these figures to the literature, the quality of a dataset can be judged upon: 

* **CO2 emissions**: The total CO2 emissions (and the reduction in comparison to 1990) are derived by the ETM. It turns out that they are about 100 MT CO2 too low in comparison to literature (should be ~800 MT). It is not clear why that is. A part can be explained by the metal sector, but there must be other reasons as well. (turning the metal sector off and aggregating the metal sector within the industry analysis will increase emissions)
* **installed generation capacity**: The ETM calculates installed capacities of power plants (based on the input of the PP_HP and CHP analysis). The resulting capacities should be compared with the literature. 


** The following ETM modules have been disabled for the German module:**
* **no merit order**: the DE version of the ETM runs without merit order. We do not yet have hourly profiles that represent demand, volatiles and must-run production in Germany. 
* We **disabled** a number of **modules** because of a lack of research data: 
 * no employment
 * no network calculations
 * no agriculture sector



Potential improvements: 

Apart form the shortcomings mentioned above and in the individual source analyses, the following can be improved for the DE dataset: 

Generate a de.ad that is properly researched. 
There is no source analysis for the area data (de.ad). 

Some keys in the de.ad need to be mirrored correctly in this analysis. See also https://github.com/quintel/etdataset/issues/365
 * services: there is no proper source analysis. All inputs are tweaked manually until checks are optimised.
 * transport: Research required that allows us to split demand for transport diesel over trucks and cars. 
 * other: 4 IEA carriers are disregarded. which amount to ~ 5.6 PJ. 

 
 