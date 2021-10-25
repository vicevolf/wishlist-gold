---
title: "Cats"
permalink: "/cats.html"
---

这个页面统计了所有的标签。

<div>
<ul>
      {% assign categories_list = site.categories %}
      {% if categories_list.first[0] == null %}
        {% for category in categories_list %}
          <li class="nav-item"><a class="nav-link" href="{{site.baseurl}}/categories.html#{{ category | downcase }}">{{ category }} ({{ site.tags[category].size }})</a></li>
        {% endfor %}
      {% else %}
        {% for category in categories_list %}
          <li class="nav-item"><a class="nav-link" href="{{site.baseurl}}/categories.html#{{ category[0] | downcase }}">{{ category[0] }} ({{ category[1].size }})</a></li>
        {% endfor %}
      {% endif %}
    {% assign categories_list = nil %}
</ul>
</div>
