---
layout: default
title: Home
---

<h1>Welcome to Toolskits Cloud Security Blog</h1>
<p>Explore tutorials, tools, and insights to secure cloud infrastructure.</p>

<h2>Latest Posts</h2>
<ul>
  {% for post in paginator.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span class="date">{{ post.date | date: "%b %d, %Y" }}</span>
    </li>
  {% endfor %}
</ul>

{% if paginator.total_pages > 1 %}
  <div class="pagination">
    {% if paginator.previous_page %}
      <a href="{{ paginator.previous_page_path | relative_url }}">&laquo; Previous</a>
    {% endif %}
    <span>Page {{ paginator.page }} of {{ paginator.total_pages }}</span>
    {% if paginator.next_page %}
      <a href="{{ paginator.next_page_path | relative_url }}">Next &raquo;</a>
    {% endif %}
  </div>
{% endif %}
