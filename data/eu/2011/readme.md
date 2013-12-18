# "Start here" Readme for EU27 2011

This directory contains all Input Data (see [nomenclature](https://github.com/quintel/etdataset/blob/master/nomenclature.md) for an explanation of terms) that is needed to construct our EU 2011 dataset (in the 'output' folders within each analysis folder). 
Furthermore, all 'input' folders contain a CSV files that store 'dashboard inputs'. These inputs are read into the respective analysis and shape the energy flow of the 'EU 2011' dataset. 
If you want to know what the EU Input Data is based on (references, justifications), please go to our "Source analyses". These can be found on Dropbox, in `Dropbox/Quintel/Projects/Restructure Research Dataset/Etdataset/Source Analyses/eu/2011` (temporary solution, the directory might change). 


## Source analysis content tree

All source analyses mirror the research analyses. In other words: For every research analysis folder on the ETDataset repository, you will find a corresponding Source analysis folder for the specific country and year that justifies the inputs for that particular analysis. 

### 0. Preparation of IEA data

IEA data table are prepared for the research analysis dataflow. A shift of solar PV generation is undertaken (from main activity sector to residences and services). 

### 1. CHP analysis
Similarly to the CHP analysis, the PP_HP analysis also assigns FLH to power plants, which will determine the installed capacity per plant. Full load hours and installed capacities are very relevant in the ETM, for example in the calculation of the 'loss of load' or 'plant profitability'. 

much of a carrier can be exported or might need to be imported in the future. 



Apart from defining energy flows, the ETM also needs to know several figures that are not of an energetic nature. For example, the ETM needs to know the population and size of a country. 
Area data is stored in a file called nl.ad or de.ad (country.ad). A research analysis that creates this file automatically after prompting user input is not yet available. 

## Shortcomings

There are a number of shortcoming in the EU dataset: 

1. preparation of IEA data / solar PV shift: It is not properly researched how much solar PV is in stalled in the sectors residences and services and in main activity. 
* CHP analysis: FLH are not properly researched. 
* PP_HP analysis: FLH are often derived to make installed capacity fit. It is not validated if these FLH are reflecting reality. 
* The total installed capacity that results from the CHP and PP_HP analyses: Only two reports were found that report installed capacities. Depending on the country, this research data is often out-dated or missing. Installed capacities are based on data from 2009 or before. 
* primary production: the production profiles are extrapolated from the historic development of the last 10 years. Is there a better forecasting method? Also, the other dashboard inputs (actual and maximum production of certain carriers) needs to be researched and updated. 
* metal analysis: The amount of aluminium production is too low at the moment. Also, the share of recycled aluminium should be researched. 
* residence analysis: Many of the technology splits are based on matching the IEA energy balance. There is no independent source analysis. The share of old/new houses and the level of insulation (eu.ad) needs to be researched. 
* services analysis: The application and technology splits are based on matching the IEA energy balance. There is no independent source analysis. 
* transport: The split of diesel demand for trucks and cars needs to be researched. 
* not all IEA carriers are accounted for, see agriculture and other analysis. 
* merit order: There are only a couple of profiles defined for the EU. Many profiles are taken directly from the Dutch database. 
* area data: there is no proper source analysis for the area data (eu.ad). 
* the following modules are disabled, because of a lack of research data
 * employment module
 * network calculations
* CO2 emissions: The total CO2 emissions (and the reduction in comparison to 1990) are derived by the ETM. Does our calculated CO2 emission match reality?



 