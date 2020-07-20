---
layout: page
title: studies
permalink: /studies/
description: Studies you can participate in!
nav: true
---

We are currently looking for volunteers to participate in the studies below. Click on a study for more information about participating! Studies usually take place at the UConn Storrs campus.

<div class="projects grid">

  {% assign sorted_projects = site.studies | sort: "importance" %}
  {% for project in sorted_projects %}
  {% if project.active %}
  <div class="grid-item">
    {% if project.redirect %}
    <a href="{{ project.redirect }}" target="_blank">
    {% else %}
    <a href="{{ project.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if project.img %}
        <img src="{{ project.img | relative_url }}" alt="project thumbnail">
        {% endif %}
        <div class="card-body">
          <h3 class="card-title text-lowercase">{{ project.title }}</h3>
           <div class="row ml-1 mr-1 p-0">
            {% if project.population %}
				{{ project.population }}
            {% endif %}
          </div>
          <p class="card-text">{{ project.description }}</p>

        </div>
      </div>
    </a>
  </div>
  {% endif %}
{% endfor %}

</div>
