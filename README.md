# GEE
The latest news about my work on GEE

*****GF-SG METHOD*****
Update history:
(1)06/2021, add cloud shadows as the invalid value in MODIS data.
(2)08/2021, 1.update the band name of Landsat 8 SR (B4 -> SR_B4;B5 -> SR_B5;pixel_qa -> QA_PIXEL)
         and geneneration of Landsat 8 cloud mask
         2.Users can choose to save a sub area or a period of time series from output data (L348,L366)
(3)10/2021, updation of generating Landsat 5/7 cloud flag with the new source of Landsat 5/7 surface reflectance on gee 
(4)12/2021, add the applyScaleFactors function when using USGS Landsat 5/7/8 Level 2, Collection 2 (ref: the guide of these datesets in Earth Engine Data Catalog)
(5)09/2022, correct some code commenting errors
(6)04/2024, The GF-SG V3 version (easy-implemented) has been released: [https://code.earthengine.google.com/aa5a7e3d27e9d71889cd5f25e0f6479c?noload=true](https://code.earthengine.google.com/a4ddd6bf0a33380e1332ac6e123bdea9?noload=true)
the original GF-SG V1 version can still be referenced via the link: [https://code.earthengine.google.com/ffae6b05282fb6e9a83ecbb5019b4958?noload=true](https://code.earthengine.google.com/f1253c94893eeace8997bcd95a75c8ef?noload=true)
  !!!!!!!!Features of the new version:
  1. Unlike the V1 version, which suggests calculating each Landsat tile separately before stitching them together for large area results, the new version supports direct calculation within any large-scale region (as defined by the range of the uploaded shp file) to obtain extensive regional time series data.
  2. The new version has significantly improved user memory usage and reduced computation time (for example, calculating the NDVI time series data for an area of 11,900 km2 (with an 8-day interval, 46 images) from over 5 hours previously to currently around 40 minutes).
  3. The new version supports the use of Landsat 5/7/8 data simultaneously for calculations.
  4. The new version provides SG filtering and Whittaker filtering as options for users to choose based on their needs.
  5. The new version offers other vegetation index calculations (EVI2, LSWI, NMDI) for reference.
  6. A simplified linear interpolation and SG filtering program have been provided to improve computational efficiency.
  7. The new version simplifies the MODIS shape matching process, using unsupervised clustering cross-comparison instead of the neighborhood search matching process.
  8. The new version has updated dataset usage links, improved some programming errors, reduced program redundancy, and improved some program syntax for easier reading and use.
  9. Interpolation_v2: https://code.earthengine.google.com/d4760c7869e1d9044ea7d8f5dc3ab138?noload=true
     SG_filter_v2: https://code.earthengine.google.com/09260eb2e819bac048e958c0c8b8d40f?noload=true
     Whittaker_filter_v1: https://code.earthengine.google.com/e588bdf9ecc4ea140319a762455f7f30?noload=true
(7)04/2024(2), Fixed a program error that occurred when calculating other vegetation indices
