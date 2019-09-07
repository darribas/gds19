---
title: Datasets
category: resource
layout: default
---

## Datasets

* Census socio-demographics
* IMD
* OS Geodata Pack
* Brexit vote
* AirBnb
* Twitter

{% capture census %}{% include_relative content/datasets/census.md %}{% endcapture %}
{{ census | markdownify }}

{% capture imd %}{% include_relative content/datasets/imd.md %}{% endcapture %}
{{ imd | markdownify }}

{% capture osgeo %}{% include_relative content/datasets/os_geodatapack.md %}{% endcapture %}
{{ osgeo | markdownify }}

{% capture js %}{% include_relative content/datasets/brexit.md %}{% endcapture %}
{{ js | markdownify }}

{% capture abb %}{% include_relative content/datasets/airbnb.md %}{% endcapture %}
{{ abb | markdownify }}

{% capture tweets %}{% include_relative content/datasets/twitter.md %}{% endcapture %}
{{ tweets | markdownify }}


