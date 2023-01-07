---
layout: Excel-post
title : Bullet Chart
category: Excel
author: Emmanuel Arize

---

In the business world, no matter the industry you found yourself, you always have targets and goals that you want to archive. In order to know how you are progressing, you tend to find effective ways to represent your performance against the set target. Using bullet charts you can effectively represent your performance against the target. Bullet charts are variation of bar charts, used for making comparisons such as showing performance metrics against a target.

## How do you read a bullet chart?
A bullet chart usually encodes three different data elements:
 2. An observed value known as **Feature or performance Measure** (performance score or the bullet). This is the primary data and is usually encoded as a bar, like the bar on a bar chart (encoded as black bar in the chart below) and centered in the plot area.
 3. A target value known as **Comparative Measure** used as a target marker to compare against the Feature Measure value.  This is shown in the chart below as a short red line marker that runs perpendicular to the orientation of the chart. Whenever the **Feature Measure** hit or intersect the target, you know you've hit your target.
 1. A qualitative Range of values used for grading. These ranges do  not only communicate the qualitative state of the featured measure but also the degree to which it resides within that state. If for instance the feature measure extends into a range that represents good, the distance that it travels into this range indicates how good it is.

For example in the chart below, we are measuring the year to date (YTD) revenue rating for the year. Using this chart, we can see that the YTD rating is 80% and it is shown as a black bar. Using this rating you can easily see that your YTD rating could not hit the target value 90%  which is represented as a red line perpendicular to the black bar. Although your performance came close the target value, you could not archive your set goal or target  which is 90%.

<br>
<img src="{{'assets/images/Excel/bullet1.jpg'| relative_url}}"/>
<br>


### Steps to Create a Bullet Chart in Excel

Using the table below we have the three different data elements namely

1. First four values are the qualitative range of values used for grading.
2. Performance score (feature measure) is the revenue rating for year.
3. Target value is the target that we set and wanted to archive for the year.

 to create the bullet chart.

<br>
<img src="{{'assets/images/Excel/bullet2.jpg'| relative_url}}"/>
<br>

With this data now

1. Select the needed data (in our case the entire table). After selecting the data click on the **insert tab** and select **recommended Charts**  then **ALL Charts**. From all Charts select Column chart and then a stacked column chart as below

<br>
<img src="{{'assets/images/Excel/bullet3.jpg'| relative_url}}"/>
<br>

and click on **ok** to get a chart as below

<br>
<img src="{{'assets/images/Excel/bullet4.jpg'| relative_url}}"/>
<br>
<p>
2. The  range of values on the y-axis is from 0% to 300%, let change it to have values from 0% to 100% by clicking on the
stacked column chart then from <b>Series Options </b> under <b>Format Data Series </b> select <b>vertical (Axis) value</b> .
After selecting vertical (Axis) value, now select <b>Axis Options</b> and click on the <b>Axis Options</b> to change the <b>maximum </b> value from 3.0 in
</p>
<br>
<img src="{{'assets/images/Excel/bullet5.jpg'| relative_url}}"/>
<br>

to 1.0 as below

<br>
<img src="{{'assets/images/Excel/bullet6.jpg'| relative_url}}"/>
<br>
<p>
3. Right-click the stacked column chart and choose Change Series Chart Type. Use the Change Chart
Type dialog box to change the Target series to a Stacked Line with Markers and check the checkbox under the secondary axis and click ok.
</p>

<br>
<img src="{{'assets/images/Excel/bullet7.jpg'| relative_url}}"/>
<br>


After clicking ok to the change, the Target series will show on the chart as a single dot as below.

<br>
<img src="{{'assets/images/Excel/bullet71.jpg'| relative_url}}"/>
<br>

<p>
4. Right-click on the chart and select Format Data Series, then from the <b>Series Options</b> under <b>Format Data Series</b> select <b>series "Target"</b> .

Now under the <b>Fill & Line </b> click on the Marker option and adjust the marker to look like a line and change the size to 20. </p>
Expand the Fill section, select **solid line** and change the color of the solid line to red. Expand the Border section and set the Border to No Line.
<br>
<img src="{{'assets/images/Excel/bullet8.jpg'| relative_url}}"/>
<br>

 After making changes to the maker click on the **Line option** and expand the line section, select **solid line** and change the color of the solid line to red.

<p> 5. Right click on the new secondary axis that was added to the right side of the chart and the delete it to have a chart as below.

<br>
<img src="{{'assets/images/Excel/bullet9.jpg'| relative_url}}"/>
<br>

<p>
6. Now right-click on the chart and select Format Data Series, then from the <b>Series Options</b> under <b>Format Data Series</b> select <b>series "Performance score"</b>. </p>

<p> 7. In the Format Data Series dialog box, select Secondary Axis. </p>

<p> 8. Still in the Format Data Series dialog box under Series Options, adjust the Gap Width property so that the Performance score series is slightly narrower than the other columns in the chart —here you are using 400% as below.
</p>

<br>
<img src="{{'assets/images/Excel/bullet10.jpg'| relative_url}}"/>
<br>

<p>
9. Still in the Format Data Series dialog box , under  the <b> Fill & Line option</b>, expand the Fill section, and then select the Solid fill option to set the color of the Performance score series to black as below</P>

<br>
<img src="{{'assets/images/Excel/bullet11.jpg'| relative_url}}"/>
<br>


<p>10. At this point all that’s left to do is change the color for each qualitative range to incrementally lighter
hues.</p>

<p> 11. After changing the qualitative range to incrementally lighter hues let also change the title to YTD revenue Rating</p>

The final bullet chart is given below

<br>
<img src="{{'assets/images/Excel/bullet12.jpg'| relative_url}}"/>
<br>
