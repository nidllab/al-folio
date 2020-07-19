---
layout: page
title: people
permalink: /people/
description: Lab members
nav: true
---

<div class="projects grid">

  {% assign sorted_people = site.people | sort: "lastname" %}
  {% for person in sorted_people %}
  <div class="grid-item">
    {% if person.redirect %}
    <a href="{{ person.redirect }}" target="_blank">
    {% else %}
    <a href="{{ person.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if person.img %}
        <img src="{{ person.img | relative_url }}" alt="profile picture">
        {% endif %}
        <div class="card-body">
          <h5 class="card-title">{{ person.title }}</h5>
          <p class="card-text text-lowercase">{{ person.position }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if person.website %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="Code Repository">
                <a href="{{ person.website }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
{% endfor %}

</div>
