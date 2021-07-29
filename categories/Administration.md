---
layout: category
categories: ["Dynamics Business Central", "Administration"]
permalink: /Dynamics Business Central/Administration/
sidebar_main: true
---
<a href="https://erphub.github.io">HOME</a> {{ site.categories[page.categories[0]] }}
<ul>
{% for category in site.categories %}
  <li><a name="{{ category | first }}">{{ category | first }}</a>
    <ul>
    {% for post in category.last %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
    </ul>
  </li>
{% endfor %}
</ul>

