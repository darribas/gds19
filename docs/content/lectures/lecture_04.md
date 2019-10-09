% Geographic Data Science - Lecture IV
% Mapping Data
%[Dani Arribas-Bel](http://darribas.org)

#
## Today

* Visualisation
* Geo-Visualisation
* Mapping data
    * MAUP
    * Choropleths

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


## Visualization

* By **encoding information visually**, they allow to present **large amounts** of
  numbers in a **meaninful** way.
* If well made, visualizations provide leads into the processes underlying the
  graphic.

<div style="text-align:right">
<small>
*The Visual Display of Quantitative Information*. Edward R. Tufte.
</small>
</div>


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

* Not to replace the human *in the loop*, but to **augment** her/him.
* Augmentation through engaging the **pattern recognition**
  capabilities that our brain inherently has.
* Combines cartography, infovis and statistics

## A map for everyone

Maps can fulfill several needs, looking very different depending on the
end-goal

MacEachren & Kraak (1997) identify three main dimensions:

* Knowledge of what is being plotted
* Target audience
* Degree of interactivity

## MacEachren & Kraak (1997) map cube

<div style="height: 500px;" markdown="1">
![](../content/lectures/figs/l03_map_cube.png)
</div>

[[Source](http://cartography.tuwien.ac.at/wordpress/wp-content/uploads/2013/01/cartotalk-corne-van-elzakker.pdf)]


# Making good data maps

* "Containers"
* Choropleths

#
## Data "containers"

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

* N. of bins
* How to bin?
* Colors

## How many bins?

- Trade-off: detail Vs cognitive load
- Exact number depends on purpose of the map
- Usually not more than 12

## How to bin?

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

## Color schemes

Align with your purpose

* **Categories**, non-ordered [<img src="../content/lectures/figs/l04_pal_qual.png" alt="Qualitative"
style="width:300px;height:50px;vertical-align:middle;border:0px;" class="fragment"/>](https://jiffyclub.github.io/palettable/wesanderson/#fantasticfox2_5)
* Graduated, **sequential** [<img src="../content/lectures/figs/l04_pal_seq.png" alt="Sequential"
style="width:300px;height:50px;vertical-align:middle;border:0px;" class="fragment"/>](https://jiffyclub.github.io/palettable/colorbrewer/sequential/#rdpu_5)
* Graduated, **divergent** [<img src="../content/lectures/figs/l04_pal_div.png" alt="Divergent"
style="width:300px;height:50px;vertical-align:middle;border:0px;" class="fragment"/>](https://jiffyclub.github.io/palettable/colorbrewer/diverging/#rdylgn_5)

**TIP**: check [ColorBrewer](http://colorbrewer2.org/) for guidance

#
## Tips

- Think of the purpose of the map
- Explore by trying different classification alternatives
- Combine (Geo)visualisation with other statistical devices

#
    
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Geographic Data Science'19</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://darribas.org" property="cc:attributionName" rel="cc:attributionURL">Dani Arribas-Bel</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.

