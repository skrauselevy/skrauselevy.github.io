---
permalink: /
title: "About"
excerpt: "About"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

My name is Sophia Krause-Levy and I am an assistant professor in the <a href="https://www.sandiego.edu/engineering/undergraduate/computer-science/" target="_blank">Computer Science Department in the Shiley-Marcos School of Engineering</a> at the <a href="https://www.sandiego.edu/" target="_blank">University of San Diego (USD)</a>. My research focuses on finding ways to improve how we teach computer science. I seek to uncover barriers faced by different populations of students studying computing. By uncovering and remedying those barriers, I believe we can provide an environment that supports all students.

<a href="#about-teaching">Teaching</a> – <a href="#about-awards">Awards</a> –  <a href="#about-research">Research</a>

<h2 id="about-teaching">Teaching</h2>

{% include base_path %}

<h3 id="usd">University of San Diego</h3>
{% assign usd_courses = site.teaching | where: 'location', 'usd' | sort: 'coursenum' %}
<ul>{% for post in usd_courses %}
  <li>
    {% assign tmp = '' %}
    {% if post.coursenum %}
      {% assign coursenum_split = post.coursenum | split: ' ' %}
      {% assign coursenum_numstrip = coursenum_split[1] | prepend: '!' | replace: '!00', '!' | replace: '!0', '!' | remove: '!' %}
      {% assign tmp = coursenum_split[0] | append: ' ' | append: coursenum_numstrip | append: ': ' | append: post.title | replace: ' : ', ': ' %}
    {% endif %}
    {% assign tmp = '<a style="text-decoration:underline" href="' | append: post.courseurl | append: '" target="_blank">' | append: tmp | append: '</a>' %}
    <b>{{ tmp }}</b>
    <ul style="font-size:0.75em">
      <li><u>Semesters</u>: {{ post.semesters }}</li>
    </ul>
  </li>
{% endfor %}</ul>

<h3 id="ucsd">University of California San Diego</h3>
{% assign ucsd_courses = site.teaching | where: 'location', 'ucsd' | sort: 'coursenum' %}
<ul>{% for post in ucsd_courses %}
  <li>
    {% assign tmp = '' %}
    {% if post.coursenum %}
      {% assign coursenum_split = post.coursenum | split: ' ' %}
      {% assign coursenum_numstrip = coursenum_split[1] | prepend: '!' | replace: '!00', '!' | replace: '!0', '!' | remove: '!' %}
      {% assign tmp = coursenum_split[0] | append: ' ' | append: coursenum_numstrip | append: ': ' | append: post.title | replace: ' : ', ': ' %}
    {% endif %}
    {% assign tmp = '<a style="text-decoration:underline" href="' | append: post.courseurl | append: '" target="_blank">' | append: tmp | append: '</a>' %}
    <b>{{ tmp }}</b>
    <ul style="font-size:0.75em">
      <li><u>Quarters</u>: {{ post.quarters }}</li>
    </ul>
  </li>
{% endfor %}</ul>

<center>— <a href="#top">Top</a> —</center>

{% include base_path %}

<h2 id="about-awards">Awards</h2>

<h3 id="honors-awards">Honors/Awards</h3>
<ul>{% for post in site.awards reversed %}
  {% if post.awardtype == 'honor' %}
    <li>
      <a style="text-decoration:underline" href="{{ post.awardurl }}" target="_blank"><b>{{ post.title }}</b></a>
      <ul style="font-size:0.75em">
        <li><u>Award Date</u>: {{ post.startdate }}</li>
        <li><u>Awarder</u>: {{ post.awarder }}</li>
        {% if post.videourl %}
          <li><u>Video</u>: <a href="{{ post.videourl }}" target="_blank">{{ post.videourl }}</a></li>
        {% endif %}
      </ul>
    </li>
  {% endif %}
{% endfor %}</ul>

<!-- <center>— <a href="#top">Top</a> —</center> -->

<h3 id="conference-awards">Conference Awards</h3>
<ul>{% for post in site.awards reversed %}
  {% if post.awardtype == 'conference' %}
    <li>
      <a style="text-decoration:underline" href="{{ post.awardurl }}" target="_blank"><b>{{ post.title }}</b></a>
      <ul style="font-size:0.75em">
        <li><u>Award Date</u>: {{ post.startdate }}</li>
        <li><u>Awarder</u>: {{ post.awarder }}</li>
        {% if post.videourl %}
          <li><u>Video</u>: <a href="{{ post.videourl }}" target="_blank">{{ post.videourl }}</a></li>
        {% endif %}
      </ul>
    </li>
  {% endif %}
{% endfor %}</ul>

<center>— <a href="#top">Top</a> —</center>

<h2 id="about-research">Research</h2>

{% include base_path %}

<h3 id="textbooks">Textbooks</h3>
<ol reversed>{% for post in site.publications reversed %}
  {% if post.pubtype == 'textbook' %}
    {% include archive-single-cv.html %}
  {% endif %}
{% endfor %}</ol>

<!-- <center>— <a href="#top">Top</a> —</center> -->

<h3 id="papers-articles">Papers</h3>
<ol reversed>{% for post in site.publications reversed %}
  {% if post.pubtype == 'paper' %}
    {% include archive-single-cv.html %}
  {% endif %}
{% endfor %}</ol>

<!-- <center>— <a href="#top">Top</a> —</center> -->

<h3 id="conference-presentations">Conference Workshops</h3>
<ol reversed>{% for post in site.publications reversed %}
  {% if post.pubtype == 'conference' %}
    {% include archive-single-cv.html %}
  {% endif %}
{% endfor %}</ol>

<center>— <a href="#top">Top</a> —</center>