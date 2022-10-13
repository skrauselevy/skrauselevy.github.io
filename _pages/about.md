---
permalink: /
title: "About"
excerpt: "About"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

My name is Sophia Krause-Levy and I am a Ph.D. Candidate in the <a href="https://cse.ucsd.edu/" target="_blank">Computer Science & Engineering Department</a> at the <a href="https://ucsd.edu/" target="_blank">University of California San Diego (UCSD)</a>. My research focuses on finding ways to improve how we teach computer science. I seek to uncover barriers faced by different populations of students studying computing. By uncovering and remedying those barriers, I believe we can provide an environment that supports all students.

<b>I am currently on the job market and am looking for academic positions.</b>


<!-- <center><a href="#online">Online Courses</a> – -->
<center><a href="#ucsd">University of California San Diego</a></center>

{% include base_path %}

<!-- <h2 id="online">Online Courses</h2>
{% assign online_courses = site.teaching | where: 'location', 'online' | sort: 'startdate' %}
<ul>{% for post in online_courses reversed %}
  <li>
    {% assign tmp = post.title %}
    {% if post.coursenum %}
      {% assign tmp = post.coursenum | append: ': ' | append: tmp %}
    {% endif %}
    {% assign tmp = '<a style="text-decoration:underline" href="' | append: post.courseurl | append: '" target="_blank">' | append: tmp | append: '</a>' %}
    <b>{{ tmp }}</b>
    <ul style="font-size:0.75em">
      {% if post.instructors %}
        <li><u>Instructors</u>: {{ post.instructors }}</li>
      {% endif %}
      <li><u>Duration</u>: {{ post.startdate }} to {{ post.enddate }}</li>
    </ul>
  </li>
{% endfor %}</ul>

<center>— <a href="#top">Top</a> —</center> -->

<h2 id="ucsd">University of California San Diego</h2>
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