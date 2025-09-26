---
layout: single-student
title: "Student Reflections"
permalink: /student-work/
author_profile: true
---

One of my favourite ways to evaluate student learning is simple: I ask, “What have you learned in this course?” This question cuts through the artificial constraints imposed by traditional exams and essays. It gives students space to reflect and use their own voice while exploring their own creativity. The responses are consistently more insightful, authentic, and moving than standard evaluation formats. They're also more rewarding to read than yet another formulaic answer to a generic test or essay prompt. I include some of the more potent ones below.  

Note, I anonymize all contributions here but I don't ask for student permission before posting. If you are a student and you find a response of yours here and you'd like it pulled, email me at mikes@athabascau.ca and I'll pull it right away.

{% include base_path %}

{% for post in site.student_work reversed %}
  {% include archive-student-single.html %}
{% endfor %}
