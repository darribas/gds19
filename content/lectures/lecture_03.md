% Geographic Data Science - Lecture III
% Spatial Data
%[Dani Arribas-Bel](http://darribas.org)

#
## "Day 1"

- Introduced the (geo-)data revolution

    * What is it?
    * Why now?

- The *need* of **(geo-)data science** to make sense of it all

## Today

- Types of (geo-)data: refresher
- Traditional and new sources of spatial data
- New ways for traditional approaches

# 
## Representing the World Digitally
## GIS Data Models
Traditionally, geographic information is represented as:

- `Vector` <span class='fragment'><span class='hlg'>finite</span> set of entities (<span class='hlg'>shapes</span>/geometries)</span>
- `Raster` <span class='fragment'> <span class='hlg'>images</span> encoding <span
  class='hlg'>surfaces</span> (values, colours, etc.)</span>

## Vector

<table>
<col width="33%">
<col width="33%">
<col width="33%">
<tr>
<td>
<img src="../content/lectures/figs/l03_points.png" style="height:250px">
</td>
<td>
<img src="../content/lectures/figs/l03_streets.png" style="height:250px">
</td>
<td>
<img src="../content/lectures/figs/l03_polygons.png" style="height:250px">
</td>
</tr>
</table>

## Raster

<table>
<col width="60%">
<col width="40%">
<tr>
<td>
<img src="../content/lectures/figs/l03_dem.jpg" style="height:300px">
</td>
<td>
<img src="../content/lectures/figs/l03_sat.jpg" style="height:300px">
</td>
</tr>
</table>

# 

## *Good old* spatial data

## *Good old* spatial data

[[source](https://www.youtube.com/embed/RY2J8ETZzLo)]

<iframe width="660" height="415" src="https://www.youtube.com/embed/RY2J8ETZzLo" frameborder="0" allowfullscreen></iframe>

## *Good old* spatial data (+)

Traditionally, datasets used in the (social) sciences are:

* Collected for the purpose --> **carefully** designed
* **Detailed** in information ("*...rich profiles and portraits of the country...*")
* **High quality**

## *Good old* spatial data (-)

But also: 

* Massive enterprises ("*...every single person...*) --> **costly**
* But **coarse** in resolution (to preserve pricacy they need to be
  aggregated)
* **Slow**: the more detailed, the less frequent they are available

## Examples

* Decenial census (and census geographies)
* Longitudinal surveys
* Customly collected surveys, interviews, etc.
* Economic indicators
* ...

#
## New sources of (spatial) data

## New sources of (spatial) data

Tied into the (geo-)data revolution, new sources are appearing that are:

* <span class='hlg'>**Accidental**</span> --> created for different purposes but available for analysis
  as a side effect
* Very <span class='hlg'>diverse</span> in nature, resolution, and quality but, potentially, much more
  **detailed** in both space and time

Different ways to categorise them...

## Lazer & Radford (2017)

* <span class='hlg'>Digital life</span>: digital actions (Twitter, Facebook, WikiPedia...)
* <span class='hlg'>Digital traces</span>: record of digital actions (CDRs, metadata...)
* <span class='hlg'>Digitalised life</span>: nonintrinsically digital life in digital form (Government
  records, web...)

## Arribas-Bel (2014)

Three levels, based on how they originate:

* <span class='hlg'>Bottom up</span>: "Citizens as sensors"
* <span class='hlg'>Intermediate</span>: Digital businesses/businesses going digital
* <span class='hlg'>Top down</span>: Open Government Data

## Opportunities (Lazer & Radford, 2017)

* Massive, passive 
* Nowcasting
* Data on social systems
* Natural and field experiments ("always-on" observatory of human behaviour)
* Making big data small

## Challenges (Arribas-Bel, 2014)

* Bias
* Technical barriers
* Methodological "mismatch"

#
## Old/New, raster/vector...
## Old/New, raster/vector...

<span class='fragment'>
Traditional <span class='hlg'>approaches</span> to represent the world in a computer are <span class='hlg'>blending</span> thanks to
new forms of data
</span>

<span class='fragment'>
Keep an <span class='hlg'>open mind</span> to tools, approaches, and methods
</span>

##

Buildings from satellite (NYTimes)

## {data-background=../content/lectures/figs/l03_strava.png data-background-size=contain data-transition=none}

##

GHSL

#
     
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Geographic Data Science'19</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://darribas.org" property="cc:attributionName" rel="cc:attributionURL">Dani Arribas-Bel</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.


