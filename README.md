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
What I'm hoping for with the software is a partial 3D rendition of the above 2D array of data.
This data set is incomplete purely as a function of the way a car might operate. While it is vehicle specific, there are many examples 
in the real world where there would be incomplete data sets one might want to be able to get a feel for in the third 
dimension. Physics experiments, tomography, point clouds etc etc.

The problem with the first image is the "zero" data points and the polygon surface corresponding to the surrounding "real"
data point distorts the polygon surface "trend for want of a better word" visually. The second image is the same data set, with the 0 data points changed to an average of the array,
array drawn, then the original 0 data points (now an average) deleted. Note still not valid but intuitively feels closer.

Currently the above 2D data array looks like below.<BR>
<img src="https://github.com/myupctoys/AFR-Data-Sets/assets/5317221/c40eb818-a7a9-4312-a484-e1e486d1a13d" width="600">

Below is closer to what I hope for. Still not right but closer.<BR>
<img src="https://github.com/myupctoys/AFR-Data-Sets/assets/5317221/7c0cd211-073b-4d7d-8a10-aec4968f331f" width="600">
# Problem defined
Note the following arrays show the data points and the coloured corrpesonding polygon surface relating to the surrounding data points.<BR>

# Baseline Scenario
<img src="https://github.com/myupctoys/AFR-Data-Sets/assets/5317221/de0da9ac-b4ac-4a87-b810-eef6e38c803b" height="150">
<BR>Above data set corresponds visually to a flat surface set of polygons. Makes sense.<BR><BR>
<img src="https://github.com/myupctoys/AFR-Data-Sets/assets/5317221/6691ee5b-a5ad-4b7c-87bd-562798f8b943" height="200">

# Scenario #1
<img src="https://github.com/myupctoys/AFR-Data-Sets/assets/5317221/82568331-c576-40ce-ba6b-c981375a0151" height="150">
<BR>We lose one data point at the edge of an array, corresponds to two polygon surfaces being altered.<BR><BR>
<img src="https://github.com/myupctoys/AFR-Data-Sets/assets/5317221/294f9534-ee95-42e8-a143-b736a27077f2" height="200">

# Scenario #2
<img src="https://github.com/myupctoys/AFR-Data-Sets/assets/5317221/86e5cbf0-aa8f-44f5-841b-c52c0eb62d54" height="150">
<BR>Still only the loss of one data point but in the middle of the array, we loose detail on four polygon surfaces.<BR><BR>
<img src="https://github.com/myupctoys/AFR-Data-Sets/assets/5317221/821e3a40-b8fd-4314-9712-ab68d72b24c6" height="200">

# Scenario #3
<img src="https://github.com/myupctoys/AFR-Data-Sets/assets/5317221/527d93e5-2352-4440-bd2c-9902d50d6966" height="200">
<BR>With the loss of two data points we lose surface polygon detail from 8 squares.<BR><BR>
<img src="https://github.com/myupctoys/AFR-Data-Sets/assets/5317221/80394bdd-5fbd-4a35-80f2-e79afd67b690" height="200">

# Summary
While the charting software can only but run with the data presented to it, as far as it’s concerned a zero value being just as valid a data point as any other value. Understand the fact that each polygon is defined by the four surrounding data points, and my question was based around how to get around the visual problem if one of them was zero, in the case of the sample set, missing.<BR><BR>
Simple enough to delete all the zero points but one also looses a lot of the surface polygon visual information from points that are valid (as shown above), especially when that data set might have a lot of edge cases and one-off isolated data points that are missing as detailed above.<BR>
Full data set then the chart is perfect. Partial data set and quite a bit of visual content is lost if deleted, or at best visually distorting the real data points that surround an unwanted data point to up to 4 polygon surfaces per missing data point.
<BR>My question was to ask for thoughts on the topic. Which was answered to my satisfaction in so far as the four data points being needed to define that polygon therefore deleting or modifying that data point wasn’t a solution if polygon surfaces were part of the picture. 
<BR><BR>The problem isn’t with the software, more that the current approach with the software, if missing data points needed to be catered for; isn’t a solution.
<BR><BR> A solution to this scenario might be each XY "point" is defined by four points to define a polygon surface with an additional Z axis parameter that would be the plotted polygon magnitude. That way the Z axis point could be deleted with no impact on the adjoining Z axis points as each Z axis point has its own set of four point defineing its own polygon. Additionally those four points could feasbily be modified to matching with adjoinging polygons. There would be no loss of detail simply because one point was missing.





