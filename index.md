---
title: Home
category: home
layout: default
---

{% capture index %}{% include_relative content/website_data/index.md %}{% endcapture %}
{{ index | markdownify }}

### Module Handbook

A pdf copy of the module handbook can be downloaded [here](content/handbook/handbook.pdf).

### Citation

If you use material from this course, I would appreciate if you used the
following citation:

```
@online{darribas_gds18,
  author = {Dani Arribas-Bel},
  title = {Geographic Data Science'18},
  year = 2018,
  url = {http://darribas.org/gds18},
}
```

### Code repository

<a rel="repo" href="https://github.com/darribas/gds18"><img alt="@darribas/gds18" style="border-width:0" src="GitHub-Mark.png" /></a>

This website, as well as the entire set of materials, code, and data included
in this course are available as an open Github repository available at:


> [https://github.com/darribas/gds18](https://github.com/darribas/gds18)

### License

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Geographic Data Science'18</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://darribas.org" property="cc:attributionName" rel="cc:attributionURL">Dani Arribas-Bel</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
