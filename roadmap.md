---
layout: default
title: Roadmap
permalink: /roadmap/
---

<div class="wrapper hero">
  <div class="grid">
    <div class="w12">
      <h1>Roadmap</h1>
      <p>Being ready for an advesarial future takes planning and foresight</p>
    </div>
  </div>
</div>


<div class="wrapper roadmap">
  <div class="grid">
    <div class="w12">

      {% assign roadmap = site.roadmap | where:'complete',true | sort: 'date' %}
      {% for item in roadmap %}

      <div class="roadmap-item{% if item.complete == true %} complete{% endif %}">
        <div>
          <h3>{{ item.title }}</h3>
          <span class="date">
            {{ item.date | date:'%B %Y' }}
          </span>
          <div class="content">{{ item.content}} </div>
        </div>
      </div>
      {% endfor %}
    </div>

  </div>
</div>

<div class="wrapper roadmap">
  <div class="grid">
    <div class="w12">

      {% assign roadmap = site.roadmap | where:'complete',false | sort: 'date' %}
      {% for item in roadmap %}

      <div class="roadmap-item take2{% if item.complete == true %} complete{% endif %}">
        <div>
          <h3>{{ item.title }}</h3>
          <span class="date">
            {{ item.date | date:'%B %Y' }}
          </span>
          <div class="content">{{ item.content}} </div>
        </div>
      </div>
      {% endfor %}
    </div>

  </div>
</div>