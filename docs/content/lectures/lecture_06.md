% Geographic Data Science - Lecture VI
% Exploring Space in Data
%[Dani Arribas-Bel](http://darribas.org)

#
## Today

* ESDA
* Spatial Autocorrelation
* Measures

    * Global
    * Local

#
## **`ESDA`**
##

**E**xploratory

**S**patial

**D**ata

**A**nalysis

##

**[Exploratory]**

Focus on discovery and assumption-free investigation

**[Spatial]**

Patterns and processes that put *space* and *geography* at the core

**[Data Analysis]**

Statistical techniques

##

Questions that **ESDA** helps...

**Answer**

* *Is the variable I'm looking at concentrated over space? Do similar values
  tend to locate closeby?*
* *Can I identify any particular areas where certain values are clustered?*

<div class="fragment">
**Ask**

* *What is behind this pattern? What could be generating the process?*
* *Why do we observe certain clusters over space?*
</div>

#
## Spatial Autocorrelation

##

<center>
*Everything is related to everything else, but near things are more related
than distant things*
</center>

<div style="text-align:right">
<small>
Waldo Tobler (1970)
</small>
</div>

## Spatial Autocorrelation

-Statistical representation of Tobler's law

-Spatial counterpart of traditional correlation

<span class="fragment">
<b>*Degree to which similar values are located in similar locations*</b>

<div class="fragment">
Two flavors:

* **Positive**: similar values $\rightarrow$ similar location (*closeby*)
* **Negative**: similar values $\rightarrow$ disimilar location (*further
  apart*)
</div>

## Examples

**Positive** SA: <span class="fragment">income, <span class="fragment"> poverty,
<span class="fragment"> vegetation, <span class="fragment"> temperature...

**Negative** SA: <span class="fragment"> supermarkets, <span class="fragment"> police
stations, <span class="fragment"> fire stations, <span class="fragment">
hospitals...

## Scales

<div>
**[Global]**

*Clustering*: do values tend to be close to other (dis)similar values?
</div>

<div class="fragment">
**[Local]**

*Clusters*: are there any specific parts of a map with an extraordinary
concentration of (dis)similar values?
</div>

#
## **Global** Spatial Autocorr.
## **Global** Spatial Autocorr.

**<i>"Clustering"</i>**

*Overall trend where the distribution of values follows a particular pattern
over space*

<span class="fragment">
**[Positive]** Similar values close to each other (high-high, low-low)

<span class="fragment">
**[Negative]** Similar values far from each other (high-low)

<span class="fragment">
How to measure it???

## Moran Plot

* Graphical device that displays **a variable** on the horizontal axis against **its spatial lag** on the vertical one
* Variable and spatial weights matrix are preferably **standardized**
* Asssessment of the overall association between a variable in a given
  location and in its *neighborhood*

##

<center>
<img src="../content/lectures/figs/l06_imd_score_choro.png" alt="IMD Choropleth"
style="width:450px;height:450px;"/>
<span class="fragment"> 
<img src="../content/lectures/figs/l05_moranplot_std.png" alt="IMD Moran Plot"
style="width:450px;height:450px;"/>
</center>

## [[Interactive Demo]](http://mybinder.org/repo/darribas/int_sp_auto)

## Moran's I

**Formal test** of global spatial autocorrelation

**Statistically** identify the presence of clustering in a variable

Slope of the Moran plot

Inference based on how likely it is to obtain a map like observed from a
purely random pattern

<div class="fragment">
<script type="math/tex; mode=display">
I = \dfrac{N} {\sum_{i} \sum_{j} w_{ij}} \dfrac {\sum_{i} \sum_{j}
w_{ij}(Z_i) (Z_j)} {\sum_{i} (Z_i)^2}
</script>
</div>

#
## **Local** Spatial Autocorr.
## **Local** Spatial Autocorr.

**<i>"Clusters"</i>**

*Pockets of spatial instability*

Portions of a map where values are correlated in a particularly strong and
specific way

<span class="fragment">
**[High-High]** + SA of *high* values (*hotspots*)

<span class="fragment">
**[Low-Low]** + SA of *low* values (*coldspots*)

<span class="fragment">
**[High-Low]** - SA (*spatial outliers*)

<span class="fragment">
**[Low-High]** - SA (*spatial outliers*)

## LISAs

**L**ocal **I**ndicators of **S**patial **A**ssociation

Statistical tests for **spatial cluster detection** $\rightarrow$ Statistical significance

**Compares** the **observed** map with many **random**ly generated ones to see how likely
it is to obtain the observed associations **for each location**

<div class="fragment">
<script type="math/tex; mode=display">
I_i = \frac{Z_i}{m_2} \sum_j W_{ij} Z_j \; \; ; \; \;  m_2= \frac{\sum_i Z_i^2
}{N}
</script>
</div>

##

<center>
<img src="../content/lectures/figs/l06_brexit_choro.png" alt="Choropleth"
style="width:450px;height:650px;"/>
<span class="fragment"> 
<img src="../content/lectures/figs/l06_brexit_lisa.png" alt="LISA Map"
style="width:450px;height:650px;"/>
</center>

#
## Recapitulation

**ESDA** is a family of techniques to explore and spatially interrogate data

Main function: characterize **spatial autocorrelation**, which
  can be explored:

* **Global**ly (e.g. Moran Plot, Moran's I)
* **Local**ly (e.g. LISAs)

#
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Geographic Data Science'18</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://darribas.org" property="cc:attributionName" rel="cc:attributionURL">Dani Arribas-Bel</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.