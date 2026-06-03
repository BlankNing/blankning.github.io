---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* **Doctor of Philosophy, Engineering Mathematics**
  University of Bristol, Sep 2024 – Nov 2028 (expected)

  Supervisors: Dr Edmund R. Hunt and Dr Nikolai WF Bode

* **Master of Science, Engineering Mathematics**
  University of Bristol, Sep 2023 – Sep 2024
  
  *Best Project Award* — awarded to the top student with the highest overall mark during the MSc

* **Bachelor of Engineering, Artificial Intelligence**
  Dalian University of Technology, Sep 2020 – Jul 2023

* **High School Diploma**
  High School Affiliated to Fudan University, Sep 2016 – Jun 2019

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
