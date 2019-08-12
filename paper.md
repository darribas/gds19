---
title: 'A course on Geographic Data Science'
tags:
- Geographic Data Science
- GIS
- Data Science
- geopandas
- pysal
authors:
- name: Dani Arribas-Bel
  orcid: 0000-0002-6274-1619
  affiliation: "1, 2"
affiliations:
- name: Geographic Data Science Lab
  index: 1
- name: The University of Liverpool
  index: 2
date: 03 January 2019
bibliography: paper.bib
---

# Summary

This paper presents a computational learning module on Geographic Data
Science (GDS). This resource is part of a larger set that also includes 
a series of lecture slides, that has been used for four conscutive academic 
years to teach the course "Geographic Data Science" at the University of 
Liverpool.

# Statement of need

Although the content presented is relevant, the
currently available set of options to teach it leaves clear gaps. 
Data Science [@donoho201750] has become one of the most demanded skills thanks to an
explosion in the availability of data [@kitchin2014data]. Most of these new sources are, 
directly or indirecly, geographic in that they can be related to a particular
location on a map. However, the vast majority of data science
resources available currently ignore the spatial dimension of data,
particularly when it comes to the more analytic set of methods covered.
At the 
same time, traditional resources for teaching the handling, visualisation, and
analysis of geographic data are based on a paradigm that emphasises
graphical interfaces and "point-and-click" software packages. This approach, 
although valid, limits the flexiblity with which the analyst can effectively
move from data to insights, and is more difficult to connect with and benefit
from modern advances in both data tools and workflows.
This paper presents a pedagogical bridge
between the "spatially unaware" set of practices emerging from Data Science,
and more traditional resources designed to teach spatial analysis within a
Geographic Information Systems (GIS) environment.

# Learning objectives

Upon completion, students are able to:

* Demonstrate advanced GDS concepts and be able to use the tools
  programmatically to import, manipulate and analyse spatial data stored in
  a variety of formats.
* Understand the motivation and inner workings of the main methodological 
  approcahes of GDS, both analytical and visual.
* Critically evaluate the suitability of a specific technique, what it can
  offer and how it can help answer questions of interest.
* Apply a number of spatial analysis techniques in Python and explain how
  to interpret the results, in a process of turning data into information.
* When faced with a new data-set, work independently using GDS tools
  programmatically to extract valuable insight.

# Content

The module represents the computational element of a larger resource used in
the delivery of the course "Geographic Data Science" at the University of
Liverpool. Materials are organised and made available to the
students through the course website, which can be found at:

> [http://darribas.org/gds18/](http://darribas.org/gds18/)

The content is organised in three main blocks, each of them with a similar
amount of material, and designed to take similar length in its delivery:

* The
**first part** (notebooks `lab_00` to `lab_02`) introduces the student to the main computational tools that will
become the building blocks of the course. This includes the *Jupyter notebook*,
as well as the basics of non-spatial data manipulation and visualisation using `pandas` and `matplotlib`.
* The
**second part** (notebooks `lab_03` to `lab_05`) builds on the previous one and
shows how several of the programming patterns learnt for non-spatial data apply
directly, or very similarly, when the data provided have a spatial signature.
In addition, this part uses Python programming, `geopandas` and `pysal` to introduce the
student to building blocks of spatial analysis such as (choropleth) mapping and
spatial weights matrices. 
* The **third part** (notebooks `lab_06` to `lab_09`) relies on the previous two
to show the intuition and application of more advanced,
explicitly spatial computational techniques. In particular, this set of
notebooks cover exploratory spatial data analysis [ESDA, @anselin1999interactive], point patterns [@boots1988point], and
unsupervised learning, including both geodemographic analysis [@harris2005geodemographics] as well as
regionalisation algorithms [@duque2007supervised] that impose an additional spatial constraint.

Taken
altogether, the computational module can be seen as a collection of
independent learning objects [@norman2007designing] that can be used
individually or repurposed for
different contexts, but that also form a coherent learning program that allows
the student to progress from basic to more advanced concepts in both
Geographic Data Science and Python programming.
 
# Instructional design

There are ten Jupyter
notebooks, each covering materials that would usually be presented to
the student at a rate of one per week. Since the course expects no previous
knowledge on the core theoretical concepts, students first attend a 1h. 
lecture every week
where the main ideas behind each notebook are presented, and they are 
encouraged to examine the notebook before the computer lab (2h./week),
following a semi-flipped classroom approach [@lage2000inverting]. In the
lab, following an enquiry-based learning approach 
[@hutchings2006principles], they are expected to work individually and at
their own pace through each notebook. Although the learning emphasis
is placed first and foremost on the student, there is support provided mainly
through two
channels: within the lab, there is at least one instructor for every 15
students answering questions one-on-one or in small groups; beyond contact
time, the class
has access to an online discussion forum monitored by the course leader, where
students are encouraged to post not only questions but also answers and
responses both to other students and to their original enquiry, in case they
solve it themselves.

Each notebook is conceived as a self-contained computational narrative where theoretical
concepts are threaded with programming illustrations. The aim of this strategy
is twofold. On the one hand, the programming element presents a vehicle for the
student to experiment with more abstract ideas, as well as to illustrate
their relevance in practical applications using real world data. On the other
hand, the geographic and data science topics covered in class act as a
specific case in which several programming techniques such as loops, variables
and functions, are used.
By embedding these more general notions into a particular context, students
are able to experience their utility as tools to solve problems they may face,
rather than as abstract computational ideas.
In
addition, the self-contained nature of each notebook facilitates their use in a 
variety of contexts, from a full-fledged semester course such as "Geographic
Data Science", to shorter intensive bootcamps, or even as repurposed show'n'tell
independent master classes.

# Experience of use 

The materials in this computational resource have been used, updated and 
maintained for over three years, since the first iteration of "Geographic Data
Science" ([`http://darribas.org/gds15/`](http://darribas.org/gds15/)) was
delivered. In this time, the materials have been repurposed for a multiplicity
of contexts, with different goals and for different audiences. Most of these
experiences fall under the following two scenarios:

* **Semester-long course**: for four consecutive years 
  ([2015](http://darribas.org/gds15/), 
  [2016](http://darribas.org/gds16/), 
  [2017](http://darribas.org/gds17/), and
  [2018](http://darribas.org/gds18/)), these materials have formed the
  computational backbone of the "Geographic Data Science" course taught at the
  University of Liverpool. The course is offered to Year 3 undergraduate
  students in Geography and Planning, and to MSc students across campus. Every
  year, a varying cohort from 80 to 120 students with diverse degrees of
  prior programming experience take the course.
* **Workshops**: the module has also provided building blocks to deliver
  intensive workshops of length between one half and three days. The audiences
  for these shorter events range from social scientists with experience in
  programming but not in geographic analysis, to practitioners with experience
  in GIS but not in programming. In all these cases, one or more of the
  notebooks have formed the basis of the materials used to
  deliver computer sessions. Modifications relate mostly to
  adjusting the length to fit into the required time, or swaping the data used
  to provide more relevant examples.

# References
