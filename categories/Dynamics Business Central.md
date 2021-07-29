---
layout: category
title: Dynamics Business Central
category: "Dynamics Business Central"
permalink: /Dyanamics Business Central/
---

<div>
    {% for category in site.categories %}
        {% if page.first_cat[1] == category[0] %}<h2><img src="/assets/images/logo_MS_Dynamics_BC.png"> {{ category | first}} ({{ category | last | size}})</h2><ul>
        {% else %} <li><a href="/categories/{{ category | first }}" style="text-decoration: none;"> {{ category | first}} <span class="roundbg" style="font-size: 75%;">{{ category | last | size}}</span></a></li> 
        {% endif %}
    {% endfor %}
    </ul>
</div>

{% for post in site.categories[page.category] %} {% include archive-single.html type=page.entries_layout %} {% endfor %}