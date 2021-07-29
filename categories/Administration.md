---
layout: category
categories: ["Dynamics Business Central", "Administration"]
permalink: /Dynamics Business Central/Administration/
---
{% for category in site.categories %}
    {% if category[0] == page.categories[0] %}
        {% assign parent_cat = category[0] %}
    {% endif %}
    {% if parent_cat == page.categories[0] and category[0] == page.categories[1] %}
        {% for post in category[1] %}
            {% include archive-single.html type=page.entries_layout %}
        {% endfor %}
    {% endif %}
{% endfor %}
