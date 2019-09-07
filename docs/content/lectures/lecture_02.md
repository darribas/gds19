% Geographic Data Science - Lecture II
% (New) Spatial Data
%[Dani Arribas-Bel](http://darribas.org)

#
## "Yesterday"

- Introduced the (geo-)data revolution
    
    * What is it?
    * Why now?

- The *need* of **(geo-)data science** to make sense of it all

## Today

- Traditional data: refresher
- New sources of spatial data
- Opportunities & Challenges

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

* **ACCIDENTAL** --> created for different purposes but available for analysis
  as a side effect
* Very diverse in nature, resolution, and detail but, potentially, much more
  **detailed** in both space and time
* Quality also varies greatly

Different ways to categorise them...

## Lazer & Radford (2017)

* Digital Life: digital actions (Twitter, Facebook, WikiPedia...)
* Digital traces: record of digital actions (CDRs, metadata...)
* Digitalised life: nonintrinsically digital life in digital form (Government
  records, web...)

## Arribas-Bel (2014)

Three levels, based on how they originate:

* **[Bottom up]** "Citizens as sensors"
* **[Intermediate]** Digital businesses/businesses going digital
* **[Top down]** Open Government Data

## Citizens as sensors

* Technology has allowed widespread adoption of sensors (bands, smartphones,
  tablets...) 
* (Almost) every aspect of human life is subject to leave a digital trace that can be
  collected, stored and analyzed
* Individuals become content/data creators (sensors, *Goodchild, 2007*)
* *Why relevant for geographers?* --> Most of it (80%?) has some form of
  spatial dimension

## Example: [Livehoods](http://livehoods.org)

<div style="height: 600px;" markdown="1">
![](../content/lectures/figs/l02_livehoods.png)
</div>

## Businesses moving online

* Many of the elements and parts of bussiness activities have been
  **computerized** in the last decades
* This implies, without any change in the final product or activity per se, a
  lot more digital data is "available" about their operations
* In addition, enirely new business activities have been created based on the
  new technologies (**"internet natives"**)
* Much of these data can help researchers better understand how cities work

## Example: [Walkscore](https://www.walkscore.com/)

<div style="height: 600px;" markdown="1">
![](../content/lectures/figs/l02_walkscore.png)
</div>

## Open data for open governments

Government institutions release (part of) their internal data in open format.
Motivations ([Shadbolt, 2010](http://eprints.soton.ac.uk/268787/)):

* Transparency and accountability
* Economic and social value
* Public service improvement 
* Creation of new industries and jobs

## Example: [BikeShare Map](http://oobrien.com/bikesharemap/)

<div style="height: 600px;" markdown="1">
![](../content/lectures/figs/l02_bikesharemap.jpg)
</div>

[Source](http://oobrien.com/wp-content/uploads/2013/06/bikesharemap.jpg)

## Class Quiz

## Class Quiz

In pairs, 2 minutes to discuss the origin of the following sources of
(geo-)data:

* Geo-referenced tweets <span class="fragment">  --> Bottom-up </span>
* Land-registry house transaction values <span class="fragment"> --> Open Government </span>
* Google maps restaurant listing <span class="fragment"> --> Digital businesses </span>
* ONS Deprivation Indices <span class="fragment"> --> Traditional (not accidental!) </span>
* Liverpool bikeshare service station status <span class="fragment"> --> Open Government Data </span>

#
## Opportunities & Challenges

## Opportunities

From Lazer & Radford (2017):

* Massive, passive 
* Nowcasting
* Data on social systems
* Natural and field experiments ("always-on" observatory of human behaviour)
* Making big data small

## Challenges

* Bias
* Technical barriers to access
* The need of new methods

## Bias

* Traditional data meet some quality standards (representativity, accuracy...)
* Because they're *accidental*, new data sources might not
* Researchers need to have extra care and put more thought into what conclusions they can reach from analyses with new sources of data
* In some cases, bias can run in favour of researchers, but this should never be taken for granted

## Technical barriers to access

* Much of these data are available
* However, their accidental nature makes them not be *directly* available
* Usually, a **different set of skills** is required to tap into their power

    * Basic programming
    * Computing literacy (understanding of the internet, APIs, databases...)
    * Software savvy-ness (a.k.a. "go beyond Word and Excel")

## (New) Methods

The nature of these data is not exactly the same as that of more traditional
datasets. For example:

* Spatial aggregation: Polygons Vs. Points
* Temporal aggregation(frequency): Decadal Vs. Real-time

Some of this does not "play well" with techniques employed traditionally to
analyze data in Geography  <span class='fragment'>--> *borrow* techniques from other disciplines,
or even *create* new ones</span>

## (New) Methods

<center>
<img src="../content/lectures/figs/l02_square_circle.jpg" style="width:500px;height:500;">
</center>

<center>
[[source](https://www.flickr.com/photos/epublicist/3546059144)]
</center>

#
## New **+** Old

**Traditional** data:

* High quality, detailed, and reliable
* Costly, coarse, and slow

**Accidental** data:

* Cheap, fine-grained, and fast
* Less reliable, harder to access, and potentially uninteresting

<span class='fragment'> --> 1 + 1 > 2 </span>

#

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Geographic Data Science'19</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://darribas.org" property="cc:attributionName" rel="cc:attributionURL">Dani Arribas-Bel</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
