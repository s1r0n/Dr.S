---
layout: archive
title: "Creative Work"
permalink: /creative/
author_profile: true
---

The pieces collected under **Creative Work** extend the Lightning Path and Avatar.Global projects into deliberately mythopoetic, experimental, and affective registers. Where the more formal essays and monographs work through argument, data, and conceptual apparatus, the poems, allegories, and videos gathered here stage the same problems—the damage of Toxic Socialization, the realities of trauma, the possibility of reconnection with the Fabric of Consciousness—in imagistic, narrative, and sonic form. They are not “illustrations” of theory so much as parallel sites of inquiry, designed to engage the bodily ego and the Spiritual Ego simultaneously, and to invite reflection at the level of feeling, imagination, and symbol as well as intellect.

From an academic perspective, these works function as compact symbolic condensations of a broader critical–theoretical corpus. The allegories, for example, model complex sociological and psychological processes (socialization, ideological capture, civilizational crisis, Spiritual Emergence) in tightly structured narrative environments that can be used for teaching, clinical reflection, and comparative research on myth, religion, and consciousness. The poems and videos likewise explore themes of connection, damage, healing, and planetary transition in ways that foreground voice, rhythm, and visual metaphor, opening up questions that are difficult to articulate within conventional disciplinary prose. Taken together, the creative materials on this page are part of an intentional effort to construct a new, explicitly decolonizing mythopoetic architecture: a shared symbolic language capable of supporting individual healing, collective awakening, and the design of healthier planetary institutions.


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
