# AFR Data Set

Representative sample set from an AFR run. Note AFR's levels are low because the car is running E85 (9.76). 98 would 
be typically somewhere below 14.7

This run was lean for most of the map but it is a good representation of the type of
data set one might get from a logging run, including missing data points and areas of
operation the car never gets into. Of specific interest to me is plotting on a 3D chart
the relationship of the data points using chart based on this article.

https://www.codeproject.com/Articles/5293980/Editor3D-A-Windows-Forms-Render-Control-with-inter

Logging was done with Innovate MotorSport LM2 Wideband O2 with the csv derived from the logworks software 
available for thier product. I will make no comment on the Innovate Motorsport LM2 product other 
than it has one redeeming feature, very fast AFR update rates.
Image of the data set from their software.

![image](https://github.com/myupctoys/AFR-Data-Sets/assets/5317221/7bcab097-09f3-4e65-8ad8-a53c6a580db0)

csv file is raw data from the logger.<br>
afrs.dat is just the average AFR values in an X/Y array.<br>
rpm_map_afr.dat are all the specs derived from the origional csv data set.<br>
D32 file is the origional Innovate MotorSport logging file extracted from the SD card.<br>

