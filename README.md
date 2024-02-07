# AFR Data Set

Representative sample set from an AFR run

Note AFR's levels are low because the car is running E85

This run was lean for most of the map but it is a good representation of the tpye of
data set one might get from a logging run, including missing data points and areas of
operation the car never gets into. Of specific interest to me is plotting on a 3D chart
the relationship of the data points using chart based on this article.

https://www.codeproject.com/Articles/5293980/Editor3D-A-Windows-Forms-Render-Control-with-inter

Logging was done with Innovate MotorSport LM2 Wideband O2 with the csv derived from the logworks software 
available for thier product.

![image](https://github.com/myupctoys/AFR-Data-Sets/assets/5317221/7bcab097-09f3-4e65-8ad8-a53c6a580db0)

csv file if raw data from the logger.
afrs.dat is just the average AFR values in an X/Y array.
rpm_map_afr.dat are all the specs derived from the origional csv data set.
D32 file is the origional Innovate MotorSport logging file extracted from the SD card.

Note data set needs massaging for data points that are zero. 
