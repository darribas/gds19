% Geographic Data Science - Lecture IV
% Mapping Data
%[Dani Arribas-Bel](http://darribas.org)

#
## Today

* Mapping data
* MAUP
* Choropleths
    * Definition
    * Classes
* Cartograms
* Conditional maps
* Space-Time mapping

#
##
<h3>Mapping Data with Data maps</h3>

* **Abstraction** from the purely geographical map
* Representing **numerical values** within a **spatial** context
* A geographical approach to statistical visualization

<div class='fragment'>
`Key components`

* "Container" geographies
* Choropleths: displaying data on maps (choropleths)

</div>

#
## MAUP

##
**M**odifiable **A**real **U**nit **P**roblem <span class='fragment'>(Openshaw, 1984)</span>

##

<center>
<img src="../content/lectures/figs/l04_maup_pts.png" alt=""
style="width:300px;height:300px;"/>
<span class="fragment"> 
<img src="../content/lectures/figs/l04_maup_2x2_grid.png" alt=""
style="width:300px;height:300px;"/>
<span class="fragment"> 
<img src="../content/lectures/figs/l04_maup_2x2_map.png" alt=""
style="width:300px;height:300px;"/>
</center>

##

<center>
<img src="../content/lectures/figs/l04_maup_pts.png" alt=""
style="width:300px;height:300px;"/>
<span class="fragment"> 
<img src="../content/lectures/figs/l04_maup_5x5_grid.png" alt=""
style="width:300px;height:300px;"/>
<span class="fragment"> 
<img src="../content/lectures/figs/l04_maup_5x5_map.png" alt=""
style="width:300px;height:300px;"/>
</center>

##

<center>
<img src="../content/lectures/figs/l04_maup_pts.png" alt=""
style="width:300px;height:300px;"/>
<span class="fragment"> 
<img src="../content/lectures/figs/l04_maup_10x10_grid.png" alt=""
style="width:300px;height:300px;"/>
<span class="fragment"> 
<img src="../content/lectures/figs/l04_maup_10x10_map.png" alt=""
style="width:300px;height:300px;"/>
</center>

##

<center>
<img src="../content/lectures/figs/l04_maup_2x2_map.png" alt=""
style="width:300px;height:300px;"/>
<img src="../content/lectures/figs/l04_maup_5x5_map.png" alt=""
style="width:300px;height:300px;"/>
<img src="../content/lectures/figs/l04_maup_10x10_map.png" alt=""
style="width:300px;height:300px;"/>
</center>

## MAUP

**Scale** and **delineation mismatch**  between:

* Underlying process (e.g. individuals, firms, shops)
* Unit of measurement (e.g. neighborhoods, regions, etc.)

In some cases, it can **seriously mislead** analysis on aggregated data (e.g.
[Flint, MI!!!](http://theconversation.com/how-zip-codes-nearly-masked-the-lead-problem-in-flint-65626))

<span class="fragment">Always keep **MAUP** in mind when exploring aggregated data!!!

#
## Choropleths
## Choropleths

<center>
*Thematic map in which values of a variable are encoded using a color
gradient of some sort*
</center>

* Counterpart of the histogram
* **Values** are **classified** into specific **colors**: value --> bin
* **Information loss** as a trade off for **simplicity**

## Classification choices

* Colors <span class="fragment"> --> in alignment with the goal of the map
* Bins <span class="fragment"> --> How many?
* Algorithm:

<ul class="fragment"> 
 <li> Unique values </li>
 <li> Equal interval </li>
 <li> Qua/Quintiles (equal count) </li>
 <li> Fisher-Jenks </li>
 <li> ... </li>
</ul>

## Color schemes

Align with your purpose

* **Categories**, non-ordered [<img src="../content/lectures/figs/l04_pal_qual.png" alt="Qualitative"
style="width:300px;height:50px;vertical-align:middle;border:0px;" class="fragment"/>](https://jiffyclub.github.io/palettable/wesanderson/#fantasticfox2_5)
* Graduated, **sequential** [<img src="../content/lectures/figs/l04_pal_seq.png" alt="Sequential"
style="width:300px;height:50px;vertical-align:middle;border:0px;" class="fragment"/>](https://jiffyclub.github.io/palettable/colorbrewer/sequential/#rdpu_5)
* Graduated, **divergent** [<img src="../content/lectures/figs/l04_pal_div.png" alt="Divergent"
style="width:300px;height:50px;vertical-align:middle;border:0px;" class="fragment"/>](https://jiffyclub.github.io/palettable/colorbrewer/diverging/#rdylgn_5)

## {data-background=../content/lectures/figs/l04_colorbrewer.png data-background-size=contain}

[[Source](http://colorbrewer2.org/)]

## Classification algorithms

## Unique values

* Categorical data
* No gradient (reflect it with the color scheme!!!)
* Examples: Religion, country of origin...

## Unique values
<center>
<div style="height: 600px;" markdown="1">
![](../content/lectures/figs/l04_unique_values.png)
</div>
</center>

## Equal interval

* Take the **value** span of the data to represent and split it equally
* **Splitting** happens based on the **numerical value**
* Gives more weight to outliers if the distribution is skewed

## {data-background=../content/lectures/figs/l04_equal_interval.png data-background-size=contain}

## Quantiles

* Regardless of numerical values, split the distribution keeping the same
  amount of values in each bin
* **Splitting** based on the **rank** of the value
* If distribution is skewed, it can put very different values in the same bin

## {data-background=../content/lectures/figs/l04_quantiles.png data-background-size=contain}

## Other

* Fisher-Jenks
* Natural breaks
* Outlier maps: box maps, std. maps...

## Tips

Different classification schemes can produce widely different maps as a
result of:

* The distribution of the values
* The inherent simplification that a choropleth implies

Best advice is to **explore** different ones and **combine** choropleths with other
graphical devices like histograms or density plots

#
## Cartograms

*"**Data maps** where the variable is encoded, not by a color gradient, but by
**distorting the shape/size** of the geographical objects"*

<ul class="fragment">
<li> Useful in cases where the natural size/shape induces to wrong
interpretation, or obscures the intended representation. </li>
<li> If not done carefully, it can distort the message in unintended ways
</li>
</ul>

## Cartograms

<center>
<img src="../content/lectures/figs/l04_liv_choro.png" alt=""
style="width:400px"/>
<span class="fragment"> 
<img src="../content/lectures/figs/l04_liv_carto.png" alt=""
style="width:400px"/>
</center>

## {data-background=../content/lectures/figs/l04_carto_consumption.png data-background-size=contain}

[[Source](http://www.worldmapper.org/)]

#
## Conditional maps

<center>
Split a dataset in *buckets* by *conditioning* on additional variables, then
create a map for each *bucket*
</center>

* If no association, maps should look the same
* But, if the conditioning variables are somewhat related to the outcome we
  are mapping, the spatial distribution can vary substantially
* **Exploration** of **multivariate** relationships

## Conditional maps

<center>
<div style="width: 600px;" markdown="1">
![](../content/lectures/figs/l04_conditional_plot.png)
</div>
</center>

#
## Space-Time mapping
## Space-Time mapping

* Bringing time into a spatial 2D context is "tricky" (it's really 3D!)
* Traditionally <span class="fragment"> --> sequence of time periods, 3D plots
* More recently <span class="fragment"> --> animation and interactivity

## 

[[Source](http://www.svgopen.org/2005/papers/abstract_neumann_thematic_navigation_in_space_and_time/)]
<div style="height: 500px;" markdown="1">
![](../content/lectures/figs/l04_space_time_cube.png)
</div>


<!--
## {data-background-iframe="http://cartodb.github.io/torque/examples/navy_leaflet.html"}

[[Source](http://cartodb.github.io/torque/examples/navy_leaflet.html)]
-->

## {data-background-iframe="https://d9a.cartodb.com/viz/fe9751f0-6ced-11e4-98f3-0e9d821ea90d/embed_map"}

[[Source](https://cartodb.com/case-studies/la-metro-movement/)]

#
    
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Geographic Data Science'18</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://darribas.org" property="cc:attributionName" rel="cc:attributionURL">Dani Arribas-Bel</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.

