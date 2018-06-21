Using ArcMap to understand the Disneyland Measles Outbreak in United States, 2015
===



Objective
---

The United States in 2015 reported an unusually large amount of measles cases tied primarily to a single outbreak at Disneyland in Orange County, CA. This has subsequently brought into question the current vaccination rates throughout the United States to better understand how such outbreaks have such far reaching effects.

In this project, my goal is to  investigate the relationship between reported measles cases and estimated MMR vaccination coverage in the United States for 2015. Specifically, I am interested in whether states with higher reported measles cases have higher or lower MMR vaccination coverage.  Using data from the U.S. Census and the Center for Disease Control (CDC), I will investigate a substantive interpretation using basic descriptive statistics and data with ArcMap.



Data
---
To assess the relationship between MMR vaccination coverage and reported measles cases, we use data provided by the CDC and the US Census.  Census information will give a population estimate by state in 2015, which we can use to calculate our measles rate. Cases of measles per state was obtained from the CDC, who publish a summary of cases for every year. The vaccination coverage data was also obtained from the CDC. This is an estimate gathered from the National Immunization Survey. The NIS is a large, on-going survey of immunization coverage among U.S. pre-school children 19 through 35 months old.



**Sources:**

1. [Population estimates in 2015 from the U.S. Census ](https://www.census.gov/data/datasets/2017/demo/popest/state-total.html)
2. [Annual summary of measles cases reported by the CDC ](http://www.cdc.gov/mmwr/mmwr_nd/index.html)
3. [Measles vaccination coverage data from the National Immunization Survey (NIS) ](https://www.cdc.gov/vaccines/imz-managers/coverage/childvaxview/data-reports/mmr/reports/2015.html)



The dependent variable is measles cases, operationalized in the “measles” variable, which measures the measles cases per 100,000 persons by state.  Our independent variable is vaccination coverage, operationalized in the “vaccination” variable, which estimates the vaccination coverage in percentage for measles, mumps, and rubella (MMR) by state. These are both expressed as continuous variables in Table 1 below.




**Table 1. Descriptive Statistics of All States Including Washington D.C.**
|Variable|Observations|Mean|Std. Dev.|Min|Max|
|---|---|---|---|---|---|
|Vaccination|51|92.25|2.63|83.4|97.5|
|Measles|51|0.04|0.09|0|0.45|





Methods
---

My GIS map was created using ArcMap 10.51.1.  I used a shapefile for the US state map provided at https://gis.cancer.gov/tools/seerstat_bridge/fips_vars/. This used a projected coordinate system of “NAD_1983_Albers”, in feet.  Data for both variables was imported to ArcMap as continuous and later divided into quartiles through the classify function..

**Creating a Measles Rate**

To evaluate the frequency of reported measles and the population by state, I created a new variable that calculated a rate where I used the formula "total cases / poplulation * 100,000. Those values with zero or no reported measles cases were simply coded as "no reported value" and kept in the analysis.  Once a rate was created, I used this to compare against the MMR vacciantion coverage percentage, by state. 



Gallery
---

![map](https://github.com/kyodahl/measles/blob/master/map.jpg)



Discussion
---
While I believe the findings indicate a weak but positive association between higher rates of measles in states with lower percentages of MMR vaccination coverage, I cannot make any statistical claims that reject or support this hypothesis.  To better understand the relationship between measles rates and vaccination coverage, I think emphasis on individual level data might provide better explanation.



![cdcgraph](https://github.com/kyodahl/measles/blob/master/cdc.jpg)
**Figure 2 from CDC MMWR report, April 17, 2015 vol 64/No.14**



A report published by the CDC in 2015 investigated why individuals who reported having measles were never vaccinated. They created four mutually exclusive categories (Figure 2) and observed a pattern of reported measles cases with individuals who were given exemption from mandated immunizations. We can consider “Philosophical/Religious beliefs” category to be a proxy for exemption, accounting for a large majority of unvaccinated residents from our measles population. The article claimed “Exemptions from mandated immunizations have been shown to increase risk for acquiring disease as well as increasing the risk of a disease outbreak at the com¬munity level. Exemption rates are higher in jurisdictions where exemption requirements are procedurally easier to meet” (CDC MMWR, 2015). This points back to my hypothesis and provides a more substantive explanation where we lack statistical analysis.  We would expect to find higher rates of measles in states with lower rates of vaccinations because they might have state laws or regulations that are more relaxed or easily circumvented. When a community allows opportunity for lower vaccination rates with the threat of highly contagious disease, we are likely to see higher numbers of reported cases of the disease.  In this case, it was apparent in the large outbreak of measles cases.




Citations
---
1) Victory, K. R., Coronado, F., Ifono, S. O., Soropogui, T., Dahl, B. A., Centers for Disease, C., & Prevention. 				   (2015). Ebola transmission linked to a single traditional funeral ceremony - Kissidougou, Guinea, December, 	2014-January 2015. MMWR Morb Mortal Wkly Rep (Vol. 64). https://doi.org/10.15585/mmwr.mm6438a2






