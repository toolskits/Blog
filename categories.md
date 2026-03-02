---
layout: default
title: Categories
---

# Categories

<ul>
{% assign cats = site.posts | map: "categories" | uniq | sort %}
{% for cat_list in cats %}
  {% for cat in cat_list %}
    <li>
      <a href="#{{ cat }}">{{ cat }}</a>
      ({{ site.posts | where_exp:"p","p.categories contains cat" | size }})
    </li>
  {% endfor %}
{% endfor %}
</ul>
