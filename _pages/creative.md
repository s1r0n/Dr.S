---
layout: archive
title: "Creative"
permalink: /creative/
author_profile: true
---

{% include base_path %}

<!-- New style rendering if creative categories are defined -->
{% if site.creative_category %}
  {% for category in site.creative_category %}
    {% assign title_shown = false %}
    {% for item in site.creative reversed %}
      {% if item.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h2>{{ category[1].title }}</h2><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html post=item %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for item in site.creative reversed %}
    {% include archive-single.html post=item %}
  {% endfor %}
{% endif %}



