## Python beyond the workshop

Some people find the course interesting and would like to find out more about
how python can be used for data analysis and how to continue learning about
Python for (Geographic) Data Science. This section collects a few references
to point you in that direction.

### Books

Two excellent (free) books are:

- [*Think Python*](http://greenteapress.com/wp/think-python/) 
  ([`http://greenteapress.com/wp/think-python`](http://greenteapress.com/wp/think-python)) 
  by Allen B. Downey,
  which introduces the reader to the "Python way of thinking" and has a
  fantastic pedagogy behind it.
- [*Think Stats*](http://greenteapress.com/wp/think-stats-2e/) 
  ([`http://greenteapress.com/wp/think-stats-2e/`](http://greenteapress.com/wp/think-stats-2e/)), 
  also by Allen B. Downey. 
  This book is more geared towards the use for Python in a statistical
  context. Mind, this is a book about statistics, not about Python, but all
  the examples and computational illustrations, which are core to the author's
  approach to teaching the subject, are in Python.

There are two popular books that are good introductions to using Python for
Data Science:

- [*Python for Data
  Analysis*](https://www.oreilly.com/library/view/python-for-data/9781491957653/)
  ([`https://www.oreilly.com/library/view/python-for-data/9781491957653/`](https://www.oreilly.com/library/view/python-for-data/9781491957653/)),
  by Wes McKinney, the creator of the `pandas` library. This an excellent
  comprehensive introduction to using Python to access, manipulate, transform
  and begin to explore your data. There is very limited treatment of any
  statistical methodology but, remember, 80% of the time spent analyzing data
  is on this type of operations rather than advanced modelling!
- [*Python Data Science
  Handbook*](http://shop.oreilly.com/product/0636920034919.do) 
  ([`http://shop.oreilly.com/product/0636920034919.do`](http://shop.oreilly.com/product/0636920034919.do)), 
  by Jake VanderPlas. This is a cookbook so, rather than being structured
  around a coherent narrative, it is made up of "recipes" for specific tasks
  that are common in Data Science. There is a bit of overlap with "Python for
  Data Analysis" but this one includes more content on machine learning
  techniques.

Note these are introductions to Data Science but there is very limited, if
any, coverage of spatial data and spatial analysis.

### Package references

Several of the core packages for data science written in Python have
prepared impressive resources as part of their documentation. In some cases,
these references are a fantastic summary not only of the functionality of the
library, but also of the methods behind them. Here is a short list with some
of the most relevant ones:

- [`pandas`](http://pandas.pydata.org/pandas-docs/stable/) 
  ([`http://pandas.pydata.org/pandas-docs/stable/`](http://pandas.pydata.org/pandas-docs/stable/)): 
  the `pandas` documentation contains very throrough tutorials on every
  detail about how the library is built and how it can be used in a large
  variety of contexts. Maybe not the best to follow from start to finish, but
  the ideal place to understand how common operations such as table joins or
  group-by operations work.
- [`seaborn`](http://seaborn.pydata.org/tutorial.html)
  ([`http://seaborn.pydata.org/tutorial.html`](http://seaborn.pydata.org/tutorial.html): its tutorial 
  page contains a detailed account of all the functionality provided to
  satisfy your plotting needs without the difficulty of having to go always to
  `matplotlib`. In addition, it includes fantastic tutorials for concepts
  relevant to visualisation tasks, from how to choose an appropriate color
  palette to how to visualise categorical data.
- [`scikit-learn`](http://scikit-learn.org/stable/)
  ([`http://scikit-learn.org/stable/`](http://scikit-learn.org/stable/)) is the
  main entry gate to the world-class machine learning library. In addition to
  a detailed description of functionality, there are several tutorials that
  are fantastic introductions to the methods behind this tool. `scikit-learn`
  incorporates state-of-the-art machine learning and is constantly updated,
  along with its website.
- [`statsmodels`](http://www.statsmodels.org/stable/index.html)
  ([`http://www.statsmodels.org/stable/index.html`](http://www.statsmodels.org/stable/index.html))
  is the main library for statistical modelling in Python. It is not up to par
  with what one could find in R, but it incorporates a large amount of
  foundational techniques, from generalised linear models to hierarchical
  models or time series analysis. The library website contains reference to
  functionality and several useful tutorials.
- [`geopandas`](http://geopandas.org/)
  ([`http://geopandas.org/`](http://geopandas.org/)) contains the best 
  one-stop-shop for learning how to read, manipulate and transform spatial
  data in Python. The library itself is an abstraction of several other more
  low-level libraries that acts as the glue to make working with all of the as
  seamless as possible. The website includes tutorials on file formats,
  projections, and spatial operations, among other topics.
- [`pysal`](http://pysal.org/) ([`http://pysal.org/`](http://pysal.org/)) is
  the best resource to explore functionality in Python to perform spatial
  analysis. The library is currently going under an overhaul that will mean
  more related packages will be available through the PySAL "brand" so, its
  website represents the best one-stop shop to see what is possible in terms
  of spatial analysis in Python.
- The [*Scipy Lecture Notes*](http://www.scipy-lectures.org/) 
  ([`http://www.scipy-lectures.org/`](http://www.scipy-lectures.org/)) is fairly
  low-level, so maybe not for absolute beginners but, if you need to use
  Python to write your own application, this might be a great starting place.

### Videos

There are several online resources to learn Python, to a point that it becomes
too hard to know where to start. One of the most useful ones is the recordings
of the SciPy conference for scientific computing in Python, which takes place
every July in Austin (TX). The conference includes both short presentations of
new packages and projects and 4h workshops that delve into the details of the
main functionality in the scientific Python stack. The playlist of the 2018 
edition is available at:

> [`https://www.youtube.com/playlist?list=PLYx7XA2nY5Gd-tNhm79CNMe_qvi35PgUR`](https://www.youtube.com/playlist?list=PLYx7XA2nY5Gd-tNhm79CNMe_qvi35PgUR)

And, in the context of Geographic Data Science, the following two workshops
are of particular interest:

- ["Introduction to Geospatial Data Analysis"](https://youtu.be/kJXUUO5M4ok)
  
> [`https://youtu.be/kJXUUO5M4ok`](https://youtu.be/kJXUUO5M4ok)

- ["Introduction to `cartopy`"](https://youtu.be/TE4uXbkHK_Y)

> [`https://youtu.be/TE4uXbkHK_Y`](https://youtu.be/TE4uXbkHK_Y)

### Online Courses

In addition to disconnected resources, there are starting to appear full
bodied courses on the use of Python for (Geographic) Data Science. Here are a
couple of interest:

- [Geographic Data Science](http://darribas.org/gds18/)
  ([`http://darribas.org/gds18/`](http://darribas.org/gds18/)) is a course
  taught entirely in Python at the University of Liverpool.

