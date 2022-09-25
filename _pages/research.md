---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

<center><a href="#textbooks">Textbooks</a> – <a href="#papers-articles">Papers</a> – <a href="#conference-presentations">Conference Workshops</a></center>

{% include base_path %}

<h2 id="textbooks">Textbooks</h2>
<ol reversed>{% for post in site.publications reversed %}
  {% if post.pubtype == 'textbook' %}
    {% include archive-single-cv.html %}
  {% endif %}
{% endfor %}</ol>

<center>— <a href="#top">Top</a> —</center>

<h2 id="papers-articles">Papers</h2>
<ol reversed>{% for post in site.publications reversed %}
  {% if post.pubtype == 'paper' %}
    {% include archive-single-cv.html %}
  {% endif %}
{% endfor %}</ol>

<center>— <a href="#top">Top</a> —</center>

<h2 id="conference-presentations">Conference Workshops</h2>
<ol reversed>{% for post in site.publications reversed %}
  {% if post.pubtype == 'conference' %}
    {% include archive-single-cv.html %}
  {% endif %}
{% endfor %}</ol>

<center>— <a href="#top">Top</a> —</center>