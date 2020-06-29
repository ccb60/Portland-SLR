# Portland SLR Data Analysis

<img
    src="https://www.cascobayestuary.org/wp-content/uploads/2014/04/logo_sm.jpg"
    style="position:absolute;top:10px;right:50px;" />
    
Analysis of sea level rise data from Portland Harbor, Portland Maine

# Statement of Purpose
CBEP is committed to the ideal of open science.  Our State of the Bay data archives ensure the science underlying the 2020 State of the Bay report is documented and reproducible by others. The purpose of these archives is to release raw data and data analysis code whenever possible to allow others to review, critique, learn from, and build upon CBEP science.

# Archive Organization
All CBEP 2020 State of the Bay data analysis repositories are organized into two to four four sub-folders.  (One or more folders may be absent, if they were not needed). Each subfolder contains data, code and analysis results as follows:  

- Original Data.  Original data, with a "READ ME.TXT" file that documents data sources.  DATA IN THIS FOLDER IS AS ORIGINALLY PROVIDED OR ACCESSED.
- Derived Data.  Data derived from the originaL RAW DATA.  Includes documentation of data reorganization steps, either in the form of files (R notebooks, Excel files, etc.) that embody data transformations, or via another README.txt file
- Analysis.  Contains one or more R Notebooks proceeding through the data analysis steps.
- Graphics.  Contains R Notebooks stepping through development of related graphics, and also raw copies of resulting graphics, usually in \*.png and \*.pdf formats.  Because of downstream graphic design processes, graphics included here may differ from how they appear in the State of the Bay.

In this case, as our goal was to recreate the graphic that NOAA makes available, we conducted only limited data analysis, and all analysis has been incorporated into the R Notebook for producing the graphics.

# Summary of Data Sources
The data used to produce the SLR graphic from the State of the Bay report was downloaded directly from NOAA Tides and Currents here:
[Portland, Maine SLR Info from NOAA](https://tidesandcurrents.noaa.gov/sltrends/sltrends_station.shtml?id=8418150).

The data description on the source web site says the following: 
> "The plot shows the monthly mean sea level without the regular seasonal fluctuations due to coastal
> ocean temperatures, salinities, winds, atmospheric pressures, and ocean currents. ... The plotted
> values are relative to the most recent Mean Sea Level datum established by CO-OPS."

In other words, these data are not raw data, but have been pre-processed by NOAA.
The webpage declares the average Sea Level Rise to be 1.89+/- 0.14 mm/yr which is equivalent to a change of 0.62 feet in 100 years. 
   
Related data, which we did not end up using, was downloaded directly from the NOAA API using a simple python script [included in this archive](Original_Data/portland_tide_gage_monthly_means.py).
Data from the two data sources is highly correlated, but not identical, which presumably reflects NOAA's pre-processing of the data.

# Link to R Notebooks
[SLR Graphics][Graphics/SLR_Graphic]
