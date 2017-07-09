---
#
# You don't need to edit this file, it's empty on purpose.
# Edit minima's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: default
---

cover page

<div class="item {% if post.star %}star{% endif %}">
    <a class="url" href="{{ site.url }}{{ post.url }}">
        <aside class="date"><time datetime="{{ post.date | date:"%d-%m-%Y" }}">{{ post.date | date: "%b %d %Y" }}</time></aside>
        <h3 class="title">{{ post.title }}</h3>
    </a>
</div>