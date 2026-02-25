---
layout: page
title: Knowledge Base
permalink: /knowledge/
---

{% for category in site.categories %}
  <h2>{{ category[0] | capitalize }}</h2>
  <ul>
    {% for post in category[1] %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
      </li>
    {% endfor %}
  </ul>
{% endfor %}