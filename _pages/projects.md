---
layout: page
title: Projects
permalink: /projects/
description: Research, industry, and international collaborations, and media works.
nav: true
nav_order: 3
---

{% assign items = site.data.projects | where_exp: "p", "p.draft != true" | sort: "start" | reverse %}
{% assign research = items | where: "group", "research" %}
{% assign media = items | where: "group", "media" %}
{% assign screenings = items | where: "group", "screenings" | sort: "country" %}

## Research and Industry Collaborations

<div class="projects-list">
{% for p in research %}
  <div class="project">
    <div class="project-when">{{ p.period }}</div>
    <div class="project-body">
      <div class="project-title">{% if p.url %}<a href="{{ p.url }}">{{ p.title }}</a>{% else %}{{ p.title }}{% endif %}{% if p.status == "ongoing" or p.status == "upcoming" %} <span class="project-status">{{ p.status }}</span>{% endif %}</div>
      <div class="project-meta">{{ p.kind }}{% if p.partners %} · {{ p.partners }}{% endif %}</div>
      {% if p.image %}<img class="project-img" src="{{ p.image | prepend: '/assets/img/projects/' | relative_url }}" alt="{{ p.title }}" loading="lazy">{% endif %}
      <p class="project-desc">{{ p.description }}</p>
      {% if p.people %}<div class="project-meta">Team: {{ p.people }}</div>{% endif %}
    </div>
  </div>
{% endfor %}
</div>

## Media Works and Recognition

<div class="projects-list">
{% for p in media %}{% unless p.compact %}
  <div class="project">
    <div class="project-when">{{ p.period }}</div>
    <div class="project-body">
      <div class="project-title">{% if p.url %}<a href="{{ p.url }}">{{ p.title }}</a>{% else %}{{ p.title }}{% endif %}{% if p.status == "ongoing" or p.status == "upcoming" %} <span class="project-status">{{ p.status }}</span>{% endif %}</div>
      <div class="project-meta">{{ p.kind }}{% if p.partners %} · {{ p.partners }}{% endif %}</div>
      {% if p.image %}<img class="project-img" src="{{ p.image | prepend: '/assets/img/projects/' | relative_url }}" alt="{{ p.title }}" loading="lazy">{% endif %}
      <p class="project-desc">{{ p.description }}</p>
    </div>
  </div>
{% endunless %}{% endfor %}
</div>

<div class="projects-compact">
{% for p in media %}{% if p.compact %}
  <div class="project-line"><span class="project-when">{{ p.period }}</span><span class="project-line-body"><span class="project-line-title">{{ p.title }}</span>{% if p.partners %} · <span class="project-meta">{{ p.partners }}</span>{% endif %}</span></div>
{% endif %}{% endfor %}
</div>

## Awards and Screenings

<p class="section-note">Festival awards, competition selections, and invited screenings, 2015–2021.</p>

<div class="projects-compact">
{% for p in screenings %}
  <div class="project-line"><span class="project-when">{{ p.country }}</span><span class="project-line-body"><span class="project-line-title">{{ p.title }}</span>{% if p.partners %} · <span class="project-meta">{{ p.partners }}</span>{% endif %}</span></div>
{% endfor %}
</div>

## International Partnerships

- **Academy of Media Arts Cologne (KHM), Germany.** Cooperation agreement, 2025.
- **Vilnius Academy of Arts, Lithuania.** Erasmus+ inter-institutional agreement, 2026.
- **Anant National University, India.** Cooperation agreement in preparation.
