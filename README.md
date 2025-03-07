# RStudio-MWF-repo
Repo for modern workflows in data science

use the README file to write a mini-report (10%). 
It should include:

**a. description of the project (what you aim to do, where you got the data from, etc.)**
This project will aim to extract/transform, explore and visualize data about COVID 19 cases by location from the years 2020 to 2023. This data was extracted from the JHU record of confirmed number of cases by day for each country/region combination. Two datasets from this repository were merged by latitude for analyses, “UID_ISO_FIPS_LookUp_Table” and “time_series_covid19_confirmed_global”. 

**b. explain the organization of the repo (folder structure, where they can find the data and scripts,
what were the steps in creating the report)**

This repository contains 4 folders: 
1. data: This folder contains the data extracted from JHU's log of COVID19 cases by country.
2. scripts: This folder contains the R Markdown script to pull in the above data, merge and transform it, and create rdata outputs (in rdata_outputs) and plots of the data (in plots)
3. rdata_outputs: This folder is where the rdata in long and wide form will be output. 
4. plots: This folder is where the 3 plots will be output. 

The steps taken for creating this report were as follows: 
1. Create the repository in GitHub with README.
2. Download the necessary data from JHU's repository and move to the local clone of the repository. 
3. Create the R Markdown script, with the following steps: 
	a. Pull in and merge datasets, output to rdata_outputs
	b. Transform data as necessary for plots.
	c. Create plots of Overall Change in Log Number of Cases Over Time, Change in Log Number of Cases Over Time by Country, Change in Infection Rate per 100,000 Cases, Over Time and by Country
	d. Output plots
4. Organize folder structure and update the file paths to pull from/output data and plots to reflect this.

**c. main findings where you include the three graphs and a sentence or two on their interpretation**

We created 3 plots in this script. Here are each and my interpretation of each graph: 

1. Overall Change in Log Number of Cases Over Time: The overall log number of cases increases over time. This trend begins very steep and then plateaus out over time. 
2. Change in Log Number of Cases Over Time by Country: Despite being separated by country, the log number of cases follows a similar trend across countries - beginning very steep and then plateauing out over time. The steepness of the curve varies by country, with some having a flatter curve.
3. Change in Infection Rate per 100,000 Cases, Over Time and by Country: This is a very interesting graph, As it shows that the infection rate per 100000 is linear for each country. The change in rate of each country is linear, and the steepness of each rate is also specific to each country, with some being very steep and others being fairly flat.

**d. session info to help with reproducibility**

Below is the session info for this R Markdown script, the packages needed, dependencies, and Rversion, platform, and OS so one can reproduce the use of this script exactly: 

R version 4.3.1 (2023-06-16 ucrt)
Platform: x86_64-w64-mingw32/x64 (64-bit)
Running under: Windows 11 x64 (build 26100)

Matrix products: default


locale:
[1] LC_COLLATE=English_United States.utf8  LC_CTYPE=English_United States.utf8    LC_MONETARY=English_United States.utf8
[4] LC_NUMERIC=C                           LC_TIME=English_United States.utf8    

time zone: America/New_York
tzcode source: internal

attached base packages:
[1] stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:
[1] lubridate_1.9.3 ggplot2_3.4.4   tidyr_1.3.0     dplyr_1.1.4