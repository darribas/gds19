% Geographic Data Science - Lecture III
% (Geo-)Visualization
%[Dani Arribas-Bel](http://darribas.org)

#
## Today

* Visualization

    * *What* and *why*
    * History
    * Examples

* Geovisualization

    * *What*
    * "A map for everyone"
    * Dangers of geovisualization

#
## Visualization

##

<center>
*"Data graphics **visually display measured quantities** by means of the **combined
use** of points, lines, a coordinate system, numbers, symbols, words, shading,
and color."*
</center>

<div style="text-align:right">
<small>
*The Visual Display of Quantitative Information*. Edward R. Tufte.
</small>
</div>

##

<CENTER>
<img src="../content/lectures/figs/l03_monalisa_data.png" alt="ML data"
style="width:450px;height:450px;"/>
 <span class="fragment"> 
<img src="../content/lectures/figs/l03_monalisa.png" alt="ML pic"
style="width:450px;height:450px;"/>
</CENTER>


[[Source](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ec/Mona_Lisa,_by_Leonardo_da_Vinci,_from_C2RMF_retouched.jpg/687px-Mona_Lisa,_by_Leonardo_da_Vinci,_from_C2RMF_retouched.jpg)]

## A bit of history

<center>
Maps <span class="fragment">  --> Data Maps (XVIIth.C.) <span class="fragment">  --> Time series (1786) <span class="fragment">  --> Scatter plots
</center>

<span class="fragment">
<ul>
<li> Surprisingly recent: 1750-1800 approx. (much later than many other
  advances in math and stats!) </li>
<li> **William Playfair**'s *"linear arithmetic"*: encode/replace numbers in
  tables into visual representations. </li>
<li> Other relevant names throughout history: Lambert, Minard, Marey. </li>
</ul>

## Visualization

*The Visual Display of Quantitative Information*. Edward R. Tufte.

* By **encoding information visually**, they allow to present **large amounts** of
  numbers in a **meaninful** way.
* If well made, visualizations provide leads into the processes underlying the
  graphic.

## Historical examples

<TABLE>
 <TR>
 <TD class='fragment'>
<center>
 <img src="../content/lectures/figs/l03_pyrometrie.gif" alt=""
style="width:150px;height:150px;"/>
<small>
[[Source](http://www.fisme.science.uu.nl/wiskrant/artikelen/hist_grafieken/begin/images/pyrometrie.gif)] XVIIIth. Cent. - *Pytometrie* by J. H Lambert  
</small>
</center>
 </TD>
 <TD class='fragment'>
<center>
<img src="../content/lectures/figs/l03_playfair.gif" alt=""
style="width:150px;height:150px;"/>
<small>
[[Source](https://upload.wikimedia.org/wikipedia/commons/3/3f/Playfair_Barchart.gif)] Playfair's bar chart in The Commercial and Political Atlas (1786)
</small>
</center>
</TD>
</small>
 </TR>
 <TR>
 <TD class='fragment'>
<CENTER>
<img src="../content/lectures/figs/l03_lambert_plot.png" alt=""
style="width:150px;height:150px;"/>
<small>
[[Source](https://hal.archives-ouvertes.fr/halshs-00663305/document)] Lambert - Evaporation rate against temperature, 1769
</small>
</CENTER>
 </TD>
 <TD class='fragment'>
 <CENTER>
<img src="../content/lectures/figs/l03_minard.png" alt=""
style="width:250px;height:100px;"/>
<small>
Minard - Napoleon army map (XIXth. Cent.)
</small>
</CENTER>
</TD>
 </TR>
</TABLE>


#
## **Geo**visualization

## Tufte (1983)

<center>
*"The most extensive data maps [...] place millions of bits of information on
a single page before our eyes. No other method for the display of statistical
information is so powerful"*
</center>

## MacEachren (1994)

<center>
 *"**Geographic visualization** can be defined as the use of concrete visual
 representations --whether on paper or through computer displays or other
 media--to **make spatial contexts and problems visible**, so as to engage
 the most powerful **human information processing** abilities, those
 associated with vision."*
</center>

## GeoVisualization

* End goal is not to replace the human *in the loop*, but to **augment** her/him.
* Augmentation here comes through engaging the **pattern recognition**
  capabilities that our brain inherently has.
* Combines:
    * Traditional maps
    * Statistical maps
    * Statistical devices of other kind (charts, scatter plots, etc.)
* **Different roles** in the analysis process...

## A map for everyone

Maps can fulfill several needs

Depending on which one we want to stress, the best map will look very
different

MacEachren & Kraak (1997) identify three main dimensions:

* Knowledge of what is being plotted
* Target audience
* Degree of interactivity

## MacEachren & Kraak (1997) map cube

<div style="height: 500px;" markdown="1">
![](../content/lectures/figs/l03_map_cube.png)
</div>

[[Source](http://cartography.tuwien.ac.at/wordpress/wp-content/uploads/2013/01/cartotalk-corne-van-elzakker.pdf)]

## Un/known: *fast* and *slow* maps

## Fast maps [[Source](http://darribas.org/buzz_adam/)]

<div style="height: 450px;" markdown="1">
![](../content/lectures/figs/l03_adam_pc.png)
</div>

## Slow maps [[Source](http://www.tandfonline.com/doi/full/10.1080/21681376.2015.1067151)]

<div style="height: 500px;" markdown="1">
![](../content/lectures/figs/l03_pc4_low.png)
</div>

## Audience: *easy* and *hard* maps

<!--
The larger and non-specialized the audience, the less you can assume about
what they know, hence less information can be emedded

Highly specialized maps are not particularly compelling to the general eye,
but they contain a lot of specific information that can be easily decoded by
the trained eye

This changes with statistical/geographic literacy (the minimum grows)

Pro-tip: know your audience and optimize for it
-->

## Easy map

[[Source](https://en.wikipedia.org/wiki/Template:Map_of_same-sex_marriage_in_the_United_States#/media/File:Same-sex_marriage_in_the_United_States.svg)] Map of same-sex marriage in the US, 2015

<div style="height: 500px;" markdown="1">
![](../content/lectures/figs/l03_easy_map.svg)
</div>

## Hard map [[Source](http://epn.sagepub.com/content/44/9/2041.short)]

<CENTER>
<img src="../content/lectures/figs/l03_arribas_gerritse.png" alt="DAB-G"
style="width:550px;height:550px;"/>
</CENTER>

## Interaction: one or many maps in one

<!--
Talk about interaction, oportunity for discovery, and the end-user as explorer
rather than mere consumer

Interactivity, however, not always desired: sometimes you need one-message,
clear maps to make a case and you don't have time for rich interactive one. It
also takes much more time (althought changing)
-->

## Static map

<div style="height: 500px;" markdown="1">
![](../content/lectures/figs/l03_la.png)
</div>

## Interactive map

 <iframe 
           width='100%' height='450' frameborder='0'
               src='http://maps.cdrc.ac.uk/#/geodemographics/oac11/default/BTTTFTT/13/-2.9700/53.4000/'>
</iframe>

#
## **Dangers** of GeoVisualization

##

<div style="height: 600px;" markdown="1">
![](../content/lectures/figs/l03_lie.png)
</div>

## *How to lie with maps*

<CENTER>
<img src="../content/lectures/figs/l03_liv_equal.png" alt="ML data"
style="width:450px;;"/>
<img src="../content/lectures/figs/l03_liv_quantiles.png" alt="ML pic"
style="width:450px;;"/>
</CENTER>


## *How to lie with maps*

The human brain is so good a picking up patterns...

<p class="fragment">
... that it finds them even where they don't exist!
</p>

<p class="fragment">
**Patternicity** (Shermer, 2008)
*The tendency to find meaningful patterns in meaningless noise*
</p>
<p class="fragment">
**Apophenia** (Konrad, 1958)
*The experience of seeing patterns or connections in random or meaningless
data*
</p>

## Twitter clusters

<CENTER>
<img src="../content/lectures/figs/l03_kde.png" alt="ML data"
style="width:550px;height:550px;"/>
</CENTER>

## How to *be truthful* with maps

<center>
*"With great power comes great responsibility"*
</center>
 <span class="fragment"> 
**Statistics** to the rescue!!!
 <span class="fragment"> 
<ul>
<li> **Complement** and enhance visuals</li>
<li> Help disentangling **true** from **spurious** patterns (a.k.a. identifying
  the "Jesus on the toast")</li>
<li> **Reciprocity**: GeoVis can also enhance statistics and make them more useful</li>
</ul>

## Statistics for Twitter clusters

<CENTER>
<img src="../content/lectures/figs/l03_kfun.png" alt="ML data"
style="width:550px;height:550px;"/>
</CENTER>

#
## Recapitulation

* Visualization of statistical data is a fairly **recent** phenomenon.
* Its power comes from engaging and **augmenting** the human in the loop,
  rather than replacing her/him.
* Its power **can be misused**, but there are methods to limit this risk.

#
     
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Geographic Data Science'19</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://darribas.org" property="cc:attributionName" rel="cc:attributionURL">Dani Arribas-Bel</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.


