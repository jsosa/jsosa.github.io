---
#
# You don't need to edit this file, it's empty on purpose.
# Edit minima's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: default
---

I'm a Marie Curie PhD Fellow under the [System-Risk](https://system-risk.eu/) project working at the University of Bristol's [Hydrology Group](http://www.bris.ac.uk/geography/research/hydrology/)
in the School of Geographical Sciences. I hold a MSc in Environmental Fluid Mechanics from the Universite Grenoble Alpes and a BSc in Mechanical Engineering from the Universidad San Francisco de Quito.

My Research interests are global meteorology, hydrological modelling, hydrodynamic modelling, flooding, remote sensing, ocean wave modelling, coastal engineering, big data, data analysis and data visualization.

I've worked in geoscience research for more than 5 years. Large expertise working in big datasets (NOAA-GFS, Era-Interim, ESA-GlobWave, Landsat, Sentinels) geo formats (GeoTIFF, NetCDF, GRIB) and programming languages (Python, Matlab, Fortran, C++).

Currently, I'm working on the development of tools to map flood risk across Europe at high resolutions by means of a hydrological-hydraulic modelling chain.

## Latest News

{% for post in site.posts %}

{{ post.date | date_to_string }} -- [{{ post.title }}]({{ site.baseurl }}{{ post.url }})

{% endfor %}