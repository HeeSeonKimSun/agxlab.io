---
layout: page
title: projects
permalink: /projects/
description: Creative, industry, and international collaborations, newest first. Exhibitions, screenings, and talks credited to Hee Seon Kim alone are the PI’s own works.
nav: true
nav_order: 3
---

{% assign items = site.data.projects | where_exp: "p", "p.draft != true" | sort: "start" | reverse %}
<div class="projects-list">
{% for p in items %}
  <div class="project">
    <div class="project-when">{{ p.period }}</div>
    <div class="project-body">
      <div class="project-title">{% if p.url %}<a href="{{ p.url }}">{{ p.title }}</a>{% else %}{{ p.title }}{% endif %}{% if p.status == "ongoing" or p.status == "upcoming" %} <span class="project-status">{{ p.status }}</span>{% endif %}</div>
      <div class="project-meta">{{ p.kind }}{% if p.partners %} · {{ p.partners }}{% endif %}</div>
      <p class="project-desc">{{ p.description }}</p>
      {% if p.people %}<div class="project-meta">Lab members: {{ p.people }}</div>{% endif %}
    </div>
  </div>
{% endfor %}
</div>

## International partnerships

- **Academy of Media Arts Cologne (KHM), Germany.** Cooperation agreement between Chung-Ang University and KHM signed on September 16, 2025; seminar by KHM vice-rector Zilvinas Lilas for our students on September 15, 2025. Joint student seminars: Martian Chronicles (2024) and VANISHING LIFE (2026).
- **Vilnius Academy of Arts, Lithuania.** Erasmus+ inter-institutional agreement with the College of Arts signed in 2026; Re-Animation 2026 summer school at Nida Art Colony.
- **Anant National University, India.** Cooperation agreement between the College of Arts and the School of Design in preparation. Invited talk by Hee Seon Kim, "Constructed Feeling: How Animation and Games Shape the Architecture of Emotion", at the Mooo 1.0 Students' Moving Image Festival, November 29, 2025.
