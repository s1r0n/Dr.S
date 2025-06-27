---
layout: archive
title: "Student Work"
permalink: /student-work/
author_profile: true
---

{% include base_path %}

{% for post in site.student_work reversed %}
  {% include archive-student-single.html %}
{% endfor %}
