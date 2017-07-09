---
#
# You don't need to edit this file, it's empty on purpose.
# Edit minima's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: default
---

I'm a Marie Curie PhD Fellow at the University of Bristol's [Hydrology Group](http://www.bris.ac.uk/geography/research/hydrology/) 
in the School of Geographical Sciences.

## Latest News

{% for post in site.posts %}

{{ post.date | date_to_string }} -- [{{ post.title }}]({{ site.baseurl }}{{ post.url }})

{% endfor %}