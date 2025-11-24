---
layout: archive
title: "Creative Work"
permalink: /creative/
author_profile: true
---

{% include base_path %}

{% if site.creative_category %}
  {% for category in site.creative_category %}
    {% assign key = category[0] %}
    {% assign label = category[1].title %}
    {% assign title_shown = false %}
    {% for post in site.creative reversed %}
      {% if post.category != key %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
      ## {{ label }}
      ---
      {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.creative reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}
