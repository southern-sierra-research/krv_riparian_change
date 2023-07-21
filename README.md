# krv_riparian_change
R code and methods to capture data about habitat changes in the Kern River Valley in California.  To generate plots of NDVI and data for comparing to Yellow Billed Cuckoo population changes.

For now, we will use MODISTools to get NDVI and other data.

[Example code: https://cran.r-project.org/web/packages/MODISTools/vignettes/modistools-vignette.html](https://cran.r-project.org/web/packages/MODISTools/vignettes/modistools-vignette.html)

## Background

### Normalized Difference Vegetation Index (NDVI)

[https://gisgeography.com/ndvi-normalized-difference-vegetation-index/](https://gisgeography.com/ndvi-normalized-difference-vegetation-index/)

These data are gathered roughly every 16 days.

## Tutorial followed

To get plots over time of NDVI at specific 250x250 m pixels, I used this tutorial
[https://jepsonnomad.github.io/tutorials/MODISTools_Intro.html](https://jepsonnomad.github.io/tutorials/MODISTools_Intro.html)

## Plan

* Define bounds of NDVI rasters
  * For Leaflet maps I am currently using 
    * 5 km to either side East to West and 
    * 1 km North to South
* Pick reference sites to measure greenup for 
  * Old riverbed (no trees)
  * Cottonwood
  * Gooding's willow
* Find best NDVI overflight dates for sites for all available years
  * Plot individual locations across dates to show greenup
* Use dates with max greenup to capture NDVI for bounding box 
  * Currently just using 1st or second overflight in June
* Make maps of bounding box for each year
  * Look for predicted shifts in channel (post 2017 and 2019 spring floods)
  * Look for evidence of drought (2012-2016)
  * Look for ways to demonstrate both of the above using plots of NDVI at reference sites
    * This seems to work well for a test at 3 sites over 2016-2022
    * Drought effects would be better demonstrated over longer times spans
