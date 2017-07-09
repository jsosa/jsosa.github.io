---
#
# You don't need to edit this file, it's empty on purpose.
# Edit minima's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: default
---

cover page

## Recent posts

{% for post in site.posts %}

<table width="100%">
<tbody>
<tr>
<td>[{{ post.title }}]({{ site.baseurl }}{{ post.url }})</td>
<td style="text-align: right;">{{ post.date | date_to_string }}</td>
</tr>
</tbody>
</table>

{% endfor %}