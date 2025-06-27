---
layout: page
title: "Student Work"
permalink: /student-work/
sidebar:
  nav: studentwork
author_profile: true
---

{% assign entries = site.student_work | sort: 'date' | reverse %}

<div class="entries-list">
  {% for item in entries %}
    <article class="archive__item">
      <h2 class="archive__item-title">
        <a href="{{ item.url | relative_url }}">{{ item.title }}</a>
      </h2>

      {% if item.teaser %}
        <p class="archive__item-excerpt">{{ item.teaser }}</p>
      {% endif %}

      {% if item.courselink %}
        <p class="archive__item-meta">
          <a href="{{ item.courselink }}" target="_blank" rel="noopener">View Course</a>
        </p>
      {% endif %}
    </article>
  {% endfor %}
</div>
