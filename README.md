# Species Distribution Modeling using Maxent
### A Tutorial for Data Preparation | Mitchell Lazarz | 07 December 2020 | ID30274 Final Project

This repo contains this README explaining the steps for data preparation for the Maxent software for modeling species niche and and distribution.  This README will walk the user through the steps of software download, data download, local drive preparation, the python script for data preparation, running of the Maxent software, as well as a short analysis of outputs.  The .py script and species occurrence and study area mask data used in this tutorial are contained in this repo.

## What is Maxent?  And why use Maxent?

[Maxent](https://biodiversityinformatics.amnh.org/open_source/maxent/) is an open-source software that utilizes a machine learning algorithm in order to model species distribution based on species occurrence records and a set of climate variables.  The software extracts values at species occurrence coordinates from the series of climate grids and projects the distribution by comparing to a set of randomly selected points used as psedo-absense records.  The algorithm is based on the maximum entropy theory that estimates the greatest probability based on our current understanding of the distribution and attributes of our input records.  More information about the statistics behind this software can be found here [(Elith et. al 2010).](https://web.stanford.edu/~hastie/Papers/maxent_explained.pdf)  The Maxent approach of species distribution modeling is a widely accepted method in the ecological modeling community.  As of 2006, the Maxent software has been cited over [6000 times](https://onlinelibrary.wiley.com/doi/full/10.1111/ecog.03049) for use in ecological studies in Google Scholar (Philips et. al 2017).

The Maxent software is beneficial for conservation and land management agencies with a limited budget.  Because Maxent is open-source, it is available generally for use by the public for no cost.  This software also is relatively simple to use and the output report gives clear explanations of the findings of the model.  Because it is so widely used, there are many additional resources for result interpretation.  A set of resources from the creator, Robert Anderson, can be found [here.](https://www.andersonlab.ccny.cuny.edu/resources)

## Software Needed

In this tutorial, the user will need: 
1. Maxent species modeler application 
2. A Python IDLE (I used [IDLE (Python GUI) 3.9.0](https://www.python.org/downloads/)) 
3. ArcGIS Map or Pro with spatial analyst extension

To download Maxent, go to [this site](https://biodiversityinformatics.amnh.org/open_source/maxent/) and download the latest version.  Unzip folder contents onto your computers hard drive; I unzipped to my Program Files.  To open the Maxent modeler (you do not need to do this now), open the maxent executable .jar file within the folder.

## Data

In this tutorial we will be using three sets of data:
1. A .csv of species occurrence records
2. A study area mask
3. A set of climate variables downloaded as GEOTIFFs

#### Species Occurrence .csv
Found in this repo is a .csv of Bicknell's Thrush sightings from 2010 to 2019.  This .csv was accessed from the [Global Biodiversity Information Facility](https://www.gbif.org/).  This database contains species records from over 54,000 species.  If you would like to model distribution for a different species in the future, GBIF.org has a [user-friendly interface](https://www.gbif.org/occurrence/search) for querying for your species of interest and timeframe.  The .csv within this repo is a raw dataset that contains over 40 fields.

#### Study Area Mask
Within the StudyAreaMask folder in this repo is a shapefile of Vermont and New Hampshire, our area of interest.  This shapefile was accessed from [TIGER U.S. Census States, 2018](https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.html).   

#### Climate Variables
The set of climate varibles used in this tutorial are the WorldClim Bio Variables V1.  This is a set of 19 historic bioclimatic variables ranging from average/minimum/maximum temperature, annual/monthly/quarterly precipitation, and seasonal weather variables.  A list of these variables can be seen below:



