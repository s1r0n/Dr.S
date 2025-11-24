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

<article class="archive__item" itemscope itemtype="http://schema.org/CreativeWork">
  <h2 class="archive__item-title" itemprop="headline">
    <a href="{{ post.url | relative_url }}" rel="permalink">{{ post.title }}</a>
  </h2>

  {% if post.date %}
  <p class="page__meta">
    <i class="far fa-calendar-alt" aria-hidden="true"></i>
    <time datetime="{{ post.date | date_to_xmlschema }}" itemprop="datePublished">
      {{ post.date | date: "%B %-d, %Y" }}
    </time>
  </p>
  {% endif %}

  {% if post.description %}
  <p class="archive__item-excerpt" itemprop="description">
    {{ post.description | markdownify }}
  </p>
  {% endif %}
</article>

    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.creative reversed %}

<article class="archive__item" itemscope itemtype="http://schema.org/CreativeWork">
  <h2 class="archive__item-title" itemprop="headline">
    <a href="{{ post.url | relative_url }}" rel="permalink">{{ post.title }}</a>
  </h2>

  {% if post.date %}
  <p class="page__meta">
    <i class="far fa-calendar-alt" aria-hidden="true"></i>
    <time datetime="{{ post.date | date_to_xmlschema }}" itemprop="datePublished">
      {{ post.date | date: "%B %-d, %Y" }}
    </time>
  </p>
  {% endif %}

  {% if post.description %}
  <p class="archive__item-excerpt" itemprop="description">
    {{ post.description | markdownify }}
  </p>
  {% endif %}
</article>

  {% endfor %}
{% endif %}
