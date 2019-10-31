% Geographic Data Science - Lecture VIII
% Points
%[Dani Arribas-Bel](http://darribas.org)

#
## Today

* The *point* of points
* Point patterns
* Visualization of point patterns
* Identifying clusters of points

#
## The *point* of points
## Points like polygons

Points *can* represent **"fixed" entities**

<span class='fragment'>
In this case, points are **qualitatively** similar to **polygons/lines**

<span class='fragment'>
The **goal** here is, taking location fixed, to model other aspects of the
data

## Points like polygons

Examples:

<ul>
<li> Cities (in most cases) </li>
<li> Buildings </li>
<li> Polygons represented as their centroid </li>
<li> ... </li>
</ul>

## When points are not polygons

Point data are not only a different geometry than polygons or lines...

<span class="fragment">
... Points can also represent a fundamentally different way to approach spatial analysis

## Points unlike polygons

<ul>
<li class="fragment current-visible">  Rather than exhausting the entire space, points can be **events** subject to
  **occur anywhere** </li>
<li class="fragment current-visible"> The **location** of the event is **part** of what we are trying to understand/**model** </li>
<li class="fragment current-visible"> The interest focuses on **characterizing** the **pattern**
that the points follow **over space**
</ul>

## A few examples...

## {data-background=../content/lectures/figs/l09_crime.png}

[[Source](http://www.crimemapping.com/map.aspx?aid=3db8cf99-a73b-46d2-b218-bd24cf491577)]

## {data-background=../content/lectures/figs/l09_trees.png}

[[Source](http://jillhubley.com/project/nyctrees/)]

## UFO Sightings (1933-)

<iframe width='100%' height='520' frameborder='0' src='https://lcpearso.cartodb.com/viz/e36e448a-da87-11e4-a327-0e018d66dc29/embed_map' allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>

## Geo-tagged tweets

<iframe width="100%" height="500px" frameBorder="0" src="https://api.tiles.mapbox.com/v4/enf.c3a2de35/page.html?access_token=pk.eyJ1IjoiZW5mIiwiYSI6IkNJek92bnMifQ.xn2_Uj9RkYTGRuCGg4DXZQ#12/53.4155/-2.9680"></iframe>

#
## Point patterns

## Point patterns

Distribution of **points over** a portion of **space**

Assumption is a point can happen anywhere on that space, but only happens in
specific locations

<div class='fragment'>
* **Unmarked**: locations only
* **Marked**: values attached to each point
</div>

##

**`Point Pattern Analysis`**

Describe, characterize, and explain point patterns, focusing on their **generating process**

* <u>Visual exploration</u>
* *Clustering* properties and <u>*clusters*</u>
* Statistical modeling of the underlying processes

#
## Visualization of PPs
## Visualization of PPs

Two routes (today):

* *Aggregate* <span class='fragment'> $\leftrightarrow$ "Histogram"
* *Smooth* <span class='fragment'> $\leftrightarrow$ KDE

## Aggregation
##

<center>
*Points meet polygons*
</center>

<span class="fragment"> Use **polygon** boundaries and **count** points per area

<span class="fragment"> [Insert your skills for **choropleth mapping** here!!!]

<span class="fragment"> **But**, <span class="fragment"> the polygons need to *"make sense"* (their
delineation needs to relate to the point generating process)

## 

<center>
<img src="../content/lectures/figs/l09_liv_pts.png" alt=""
style="width:400px;height:500px;"/>
<span class="fragment"> 
<img src="../content/lectures/figs/l09_liv_cho.png" alt=""
style="width:400px;height:500px;"/>
</center>

## Hex-binning

If **no** polygon boundary seems like a **good candidate** for aggregation...

<span class='fragment'> ...draw a **hexagonal** (or squared) **tesselation**!!!

<div class='fragment'>
Hexagons...

* Are **regular**
* **Exhaust** the space (Unlike circles)
* Have **many sides** (minimize boundary problems)
</div>

## 

<center>
<img src="../content/lectures/figs/l09_liv_pts.png" alt=""
style="width:300px;height:400px;"/>
<span class="fragment"> 
<img src="../content/lectures/figs/l09_liv_hex_empty.png" alt=""
style="width:300px;height:400px;"/>
<span class="fragment"> 
<img src="../content/lectures/figs/l09_liv_hex_filled.png" alt=""
style="width:300px;height:400px;"/>
</center>


## But...

<div class="fragment">
(Arbitrary) aggregation may induce **MAUP** (see Lecture 4)
</div>

<center class="fragment">
$+$
</center>

<div class="fragment">
Points usually represent events that affect only **part** of the population
and hence are best considered as **rates** (see Lecture 4)
</div>

## Kernel Density Estimation
## Kernel Density Estimation

*Estimate the (**continuous**) observed **distribution** of a variable*

<div class='fragment'>
* Probability of finding an observation at a given point
* "Continuous histogram"
* Solves (much of) the MAUP problem, but not the underlying population issue
</div>

## {data-background=../content/lectures/figs/l09_kde.png data-background-size=contain}

[[Source](https://en.wikipedia.org/wiki/Kernel_density_estimation#/media/File:Comparison_of_1D_histogram_and_KDE.png)]

## Bivariate (spatial) KDE

*Probability of finding observations at a given point in space*

* **Bivariate** version: distribution of **pairs of values**
* In **space**: values are coordinates (XY), locations
* Continuous "version" of a choropleth

## {data-background=../content/lectures/figs/l09_kde2d.png}

## 

<center>
<img src="../content/lectures/figs/l09_liv_pts.png" alt=""
style="width:400px;height:500px;"/>
<span class="fragment"> 
<img src="../content/lectures/figs/l09_liv_kde.png" alt=""
style="width:400px;height:500px;"/>
</center>

#
## Finding clusters of PPs

##

<span class='fragment fade-out'> **Cluster** is a hard to define term </span>

<CENTER>
<span class='fragment'> *Concentrations/agglomerations of points over space, significantly more so than in the rest
of the space considered* </span>
</CENTER>

<span class='fragment'> Huge literature spanning **spatial analysis**, **statistics** and **computer science**. Today, we'll look at... </span>

##

`D`<span class='fragment'>ensity</span> 

`B`<span class='fragment'>ased</span> 

`S`<span class='fragment'>patial</span> 

`C`<span class='fragment'>lustering of</span>

`A`<span class='fragment'>pplications with</span> 

`N`<span class='fragment'>oise</span>

##

<iframe width="700" height="500" src="https://www.youtube.com/embed/5E097ZLE9Sg" frameborder="0" allowfullscreen></iframe>

## `DBSCAN`

<small>(Additional)</small> **Pros**:

- Not necessarily spatial
- Very fast to run so $\rightarrow$ scales relatively well $\rightarrow$
  applicable to large datasets

<small>(Additional)</small> **Cons**:

- Not based on any probabilistic model (no inference)
- Hard to learn about the underlying process

#

    <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Geographic Data Science'19</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://darribas.org" property="cc:attributionName" rel="cc:attributionURL">Dani Arribas-Bel</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.

