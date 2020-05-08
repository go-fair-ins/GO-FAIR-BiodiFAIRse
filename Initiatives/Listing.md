# Interesting initiatives

## Ecological data management

* worldwide 
  * [GBIF](https://www.gbif.org/) (of course, this is THE AMAAAAAZIIIIIIIIING TERIFIC intitiative! Unfortunately (or not ;) ), occurences strongly oriented even if big effort are making it more useable with others biodiversity components / use only a very little part of EML metadata standard instead of capitalizing more on its amazing power! User often don't have access to raw data files, """only""" DwC transformed data files. Moreover, using DwC data standard, there is a lot of unnecessary redundancy into GBIF data files, from tested datasets, around 35% of GBIF datasets can be totally duplicated (35% of the dataset columns contains only one unique term/sentence, repeated 1,6 Millions times if 1,6 Millions lines...)
  * [DataOne](https://www.dataone.org/), AMAZIIIING as it allows the share of all kind of raw data, thank to the intensive use of EML metadata standard ! Disseminate metadata also through https://schema.org/Dataset metadata so findable through Google dataset for example + OAI-PMH (Dublin-core) for harvesting.
  * [Pangea](https://www.pangaea.de/), using directly https://schema.org/Dataset metadata.

* Europe
  * [DEIMS](https://deims.org/) for European LTER, system was totally refactored from Drupal based system to new DEIMS-SDR. Seems that this system is really not easy to use to search for raw datasets, notably in situ one. USe of B2share to store datasets.

* US (majority are part of DataOne federation https://www.dataone.org/ and linked to NCEAS)
  * KNB https://knb.ecoinformatics.org/ based on metacat
  * Arcticdata https://arcticdata.io/catalog/view/doi:10.18739/A2TQ5RD9K & Gulf of Alaska https://goa.nceas.ucsb.edu/#data show cutting edge Metacat/Metacatui https://github.com/NCEAS/metacatui data portal implementations
  * NEON https://data.neonscience.org/home using metacat in back-end but dedicated UI
  * Environmental Data Initiative (EDI) https://portal.edirepository.org/nis/home.jsp , a secure data repository and work closely with the LTER Network Communications Office and DataONE to promote data management best practices and stewardship
  * Easier Access to Scientific Data [ERDDAP](https://coastwatch.pfeg.noaa.gov/erddap/search/index.html?page=1&itemsPerPage=1000&searchFor=fish) with attribute information: https://coastwatch.pfeg.noaa.gov/erddap/info/ecocast/index.html

* Australia
  * LTER Network https://www.ltern.org.au/based based on metacat. there is partintioning into Supersites https://supersites.tern.org.au/about-us/what-is-a-supersite

* National
  * German [GFBio](https://www.gfbio.org/) providing Excel sheet as [metadata template](https://gfbio.biowikifarm.net/wiki/Data_submission_templates_for_biodiversity,_ecological_and_collection_data)
  * French [PNDB](https://www.cesgo.org/pndb/) deploying a national Biodiversity data hub based on metacat/metacatui and developping [MetaShARK](https://github.com/earnaud/MetaShARK-v2) R Shiny app to facilitate the creation of [EDI](https://environmentaldatainitiative.org/edi/) notion of data package based creating detailled [EML](https://eml.ecoinformatics.org/) metadata document with help of automatic inferences
  
## Ecological data analysis

* Australian
  * [Ecocloud](https://www.ecocloud.org.au/)
  * [The Biodiversity and Climate Change Virtual Laboratory (BCCVL)](http://www.bccvl.org.au/species-distribution-model/)
* US and related to EDI
  - The whole Tale https://wholetale.org/ and related DataOne webinar https://vimeo.com/365134580 
* European
  * [Galaxy-E](https://ecology.usegalaxy.eu/) cloud platform, part of European Galaxy infrastructure hosted by German [de.NBI](https://www.denbi.de/) infrastructure and managed by [Freiburg university](http://www.bioinf.uni-freiburg.de/team.html)
* German VAT system (used by GFBio and GEO BON)
* French Galaxy for Ecology [Galaxy-E](https://ecology.usegalaxy.eu/)

* [Kaggle](https://www.kaggle.com/rtatman/welcome-to-data-science-in-r)


