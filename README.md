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

# Hope for the plot
What I'm hoping for with the software is a 3D rendition of the above 2D array of data, assumed a bit of lateral thiking one might be able to draw that conclusion.
This data set is incomplete purely as a function of the way a car might operate. While it is car specific, there are many examples 
in the real world where there would be incomplete data sets one might want to be able to get a feel for in the third 
dimension. Physics experiments, tomography, point clouds etc etc.

Currently the above data set looks like this.<BR>
![image](https://github.com/myupctoys/AFR-Data-Sets/assets/5317221/b05806ee-c6f2-40ca-b22f-d4c51717e5bb)

This is closer to what I hope for. Still not right but closer.<BR>
![image](https://github.com/myupctoys/AFR-Data-Sets/assets/5317221/7c0cd211-073b-4d7d-8a10-aec4968f331f)

The problem with the first image is the "zero" data points and the polygon surface corresponding to the surrounding "real"
data point distorts the underlying data "trend for want of a better word" visually. The second image is the same data set, with the 0 data points changed to an average of the array,
array drawn, then the original 0 data points (now an average) deleted. Note still not valid but intuitively makes more sense.

When I come up with a better way of altering those 0 data points I will post an image. Have tried a few vairaions on the theme of liner, bilinear, bicuibic with the above "avarge for the zero points; but not happy with the resutls.
While modifying the data sets isn't ideal, one isn't modifying the real data. Purely massaging the 0 so that they are more sympathetic to the values of the real data points so that within
the constraints of the charting software the polygon surface makes more sense visually. Understand why in so far as the need for four points to make up the polygon surface but be nice to figure a way around it.


