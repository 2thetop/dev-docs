---
layout: page
order:
title: Technical Research
heading: Technical Research
description: Current, historic and work in progress research relating to technical aspects of the micro:bit.
permalink: /research/
ref: research
lang: en
post_filter: research
---

This page collates technical projects, research and development that have been done on/with the BBC micro:bit in universities, labs, clubs and schools around the world. It has been created by the micro:bit community, and you are welcome to add any of your own work to it by editing the page and submitting a Pull Request.

If you’d like to see [research about the impact of micro:bit, head over to our main site](https://microbit.org/research/). 

---  

{% for research in site.research %}
  {% if research.post_filter contains 'research' %}
  <div class="research-post">
  <h2>
    <a href="{{ research.permalink }}">
    {{ research.title }}
    </a>
  </h2>
  <p>{{ research.description | markdownify }}</p>
  <div class="categories">
    {% assign sortedCategories = research.categories | sort %}
    {% for category in sortedCategories %}
        <span class="category">
            <a href="/category/{{ category }}" class="btn btn-info">{{ category }}</a>
        </span>
    {% endfor %}
  </div>
  </div>

  {% endif %}
{% endfor %}
