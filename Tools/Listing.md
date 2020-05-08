# Interesting tools
* Work with messy data from db
 * [OpenRefine](http://openrefine.org/) Implemented as GIE [docker repo](DockerHub repo : https://hub.docker.com/r/valentinchdock/openrefine-galaxy-ie/)
  * [FAIRifier](https://github.com/DTL-FAIRData/FAIRifier) based on OpenRefine and associated to [FAIR-metadata-editor](https://github.com/DTL-FAIRData/FAIR-metadata-editor/tree/develop). To test through GIE and linked to EML!
 * Other solutions:
    * [DataCleaner](https://datacleaner.org/)
    * [Karma](http://usc-isi-i2.github.io/karma/) A Data Integration Tool
* Tadarida tools suite: A Toolbox for Animal Detection on Acoustic Recordings Integrating Discriminant Analysis
 * [Ubat slicer](https://github.com/mont29/ubat/): Tadarida pre-processing
 * [Tadarida-D](https://github.com/YvesBas/Tadarida-D)
 * [Tadarida-C](https://github.com/YvesBas/Tadarida-C)
 * [Tadarida-L](https://github.com/YvesBas/Tadarida-L)
* STOC (Temporal monitoring of common birds)
 * Simple punctual sampling
    * Regional scale: scriptSTOCeps.R
 * Capture
* STERF (Temporal Follow-up of France Rhopalocera)

   * TRIM is now also available as R package (rtrim, via install.packages("rtrim") from CRAN). This will make it much more easy for many of you to calculate trends. But remember to have the input file in good order (so with missing values and zeroes). Of course you can also use the result of Reto's regional_gam (https://github.com/RetoSchmucki/regionalGAM/blob/master/README.md) as input.
   * Manuals and helpfiles are available via https://github.com/markvanderloo/rtrim
   * CBS also made their Multi Species Indicator tool available: https://www.cbs.nl/nl-nl/maatschappij/natuur-en-milieu/indexen-en-trends--trim--/msi-tool. With this tool you can build your own indicators from the results of rtrim.
      * regionalGAM
      * rtrim
      * MSI-tool
* [Species distribution modeling](https://cran.r-project.org/web/packages/dismo/vignettes/sdm.pdf) SDM
  * Wallace Shiny app
  * BCCVL (Sarah Richmond) tools & workflows:
    * https://github.com/BCCVL/data_conversion
    * https://github.com/BCCVL/org.bccvl.tasks/tree/develop/src/org/bccvl/tasks/datamover
    * https://github.com/BCCVL/org.bccvl.compute -> Collection and wrappers of R compute scripts
scripts R pour biomod2 https://github.com/BCCVL/org.bccvl.compute/blob/develop/src/org/bccvl/compute/rscripts/bccvl.R
    * xml who can be mapped with Galaxy xml ? https://github.com/BCCVL/org.bccvl.compute/blob/develop/src/org/bccvl/compute/content/toolkit/bioclim/bioclim.xml
* [Maxent](https://biodiversityinformatics.amnh.org/open_source/maxent/)
* GIS data handling
   * [Geospatial Abstracation Data Librairy](http://www.gdal.org/)
   * Impute missing value: https://github.com/RetoSchmucki/CESCO_R-scripts/blob/master/replace%20missing%20values%20in%20raster.r
   * Sites extraction
   * Conversion
   * Buffering
   * Calculate mean by buffer
* Visualize GIS data
   * Through "classical" GIS specialists oriented solutions:
      * [Geoserver](http://geoserver.org/)
      * [QGIS server](https://github.com/jancelin/docker-qgis-server) ou [QGIS desktop](https://github.com/jancelin/docker-qgis-desktop). A particular interesting QGIS based tool : [LizMap](https://www.3liz.com/lizmap.html) et [LizMap Docker](https://github.com/jancelin/docker-lizmap)
      * [GeoCMS](https://github.com/dotgee/geocms) GeoCMS is a complete open source solution for consuming and visualizing geospatial data
      * ~~[OpenEV](http://openev.sourceforge.net/) a software library and application for viewing and analysing raster and vector geospatial data (last release 2007!)~~
   * To manage data:
      * [PostGIS](http://www.postgis.net/) with a [Docker version](https://github.com/jancelin/docker-postgis-rpi) usable through the [Galaxy pg datatype and relatde tools implementation](https://github.com/bgruening/galaxytools/pull/642) /[Leaflet](http://leafletjs.com/) through Interactive Environment ?
      * [H2GIS](http://www.h2gis.org/support/) light and standalone GIS database
   * Through GIS non-specialists oriented solutions:
      * [Magrit](http://magrit.cnrs.fr/modules) for thematic GIS (in french and english)
* GIS data analysis
   * [WhiteboxTools advanced geospatial data analysis engine](https://github.com/jblindsay/whitebox-geospatial-analysis-tools/tree/master/whitebox_tools#available-tools)
   * [GeoTools The Open Source Java GIS Toolkit](http://www.geotools.org/)
   * [Grass Geographic Resources Analysis Support System](https://grass.osgeo.org/)
   * [NCAR Command Language](https://www.ncl.ucar.edu/index.shtml)
* Taxa automated recognition through [TensorFlow](https://tensorflow.wq.io/about)
* Dashboards for a community intensively oriented toward R
   * [R-Shiny](https://shiny.rstudio.com/) Interactive Environment
      * GIS shiny GIE through leaflet based shiny apps to display data by french regions and related plots
      * Statistics shiny GIE through [radiant](http://vnijs.github.io/radiant/)
      * Dashboard / restitution shiny GIE through [flexdashboard+shiny](https://rmarkdown.rstudio.com/flexdashboard/shiny.html) or [shiny dashboard](https://rstudio.github.io/shinydashboard/structure.html)
      * Macroecology through [Wallace](http://onlinelibrary.wiley.com/doi/10.1111/2041-210X.12945/full)
      * Marxan, [a shiny app](https://github.com/mattwatts/RunMarxanTas) for [systematic conservation planning](http://marxan.net/marxanio) 
   * Shiny and reproducibility through `interactive document` concept
      * rmarkdown, a new way to build Shiny apps through [interactive documents](http://shiny.rstudio.com/articles/interactive-docs.html)
      ```
      Interactive documents will not replace standard Shiny apps since they cannot provide the design options that come with a ui.R or index.html file. However, interactive documents do create some easy wins:

    The R Markdown workflow makes it easy to build light-weight apps. You do not need to worry about laying out your app or building an HTML user interface for the app.

    You can use R Markdown to create interactive slideshows, something that is difficult to do with Shiny alone. To create a slideshow, change output: html_document to output: ioslides_presentation in the YAML front matter of your .Rmd file. R Markdown will divide your document into slides when you click “Run Document.” A new slide will begin whenever a header or horizontal rule (***) appears.

    Interactive documents enhance the existing R Markdown workflow. R Markdown makes it easy to write literate programs and reproducible reports. You can make these reports even more effective by adding Shiny to the mix.

To learn more about R Markdown and interactive documents, please visit rmarkdown.rstudio.com.
      ```
# Interesting R packages

* [glmmTMB](https://cran.r-project.org/web/packages/glmmTMB/index.html)
* [biomod2](https://cran.r-project.org/web/packages/biomod2/index.html)
* [ENMEval](https://github.com/bobmuscarella/ENMeval)
* [virtualspecies](https://cran.r-project.org/web/packages/virtualspecies/index.html)
* [sdmplay](https://cran.r-project.org/web/packages/SDMPlay/index.html)
* [migclim](https://cran.r-project.org/web/packages/MigClim/index.html)
* [zoon](https://github.com/zoonproject/zoon)
* [bdvis](https://github.com/vijaybarve/bdvis)
