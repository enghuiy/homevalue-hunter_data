# Homevalue Hunter

scripts and plot for finding undervalued areas for home-buying

## The Idea
Homevalue Hunter is an app that helps home buyers find locations that are undervalued based on their specific criteria. The idea behind it is that the home price is influenced by a large number of factors, but if we project it down to a small set of features that a user cares about (using say linear regression), it will reveal "inefficiencies" (i.e. home prices that are over- or undervalued) that arise from features that users don't care about.

## Data Sources
- Location definitions : school district shapefiles from census.gov (ftp://ftp2.census.gov/geo/tiger/TIGER2015/)
- Pricing data (median): Zillow (API: http://www.zillow.com/webservice/GetRegionChildren.htm)
- Pricing data (for ROI): http://files.zillowstatic.com/research/public/City/City_Zhvi_SingleFamilyResidence.csv 
- School Performance data: New York State Dept. of Education; gr 3-8 assessments (http://data.nysed.gov/files/assessment/14-15/3-8-2014-15.zip)
- walkability: walkscore.com (API: http://api.walkscore.com/score?)

## Implementation
- Data cleaning and assignment onto 672 locations (shapes)
  > getData.ipynb
  > prepareCrimeData.ipynb
  > preparePrice-ROI.ipynb
- populate Postgresql
- Web App: Flask framework + mapbox API
