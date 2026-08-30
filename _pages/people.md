---
layout: page
title: People
permalink: /people/
description: Members of the Affective Game Experience Lab.
nav: true
nav_order: 1
---

{% assign groups = "Faculty|Graduate Students|Undergraduate Research Assistants|Alumni" | split: "|" %}
{% for g in groups %}
  {% assign ms = site.data.members | where: "group", g %}
  {% if ms.size > 0 %}
<h2 class="members-group">{{ g }}</h2>
{% if g == "Faculty" %}
  {% for m in ms %}
<div class="faculty-row">
  <div class="member">
    {% if m.image %}
    <img class="member-photo" src="{{ m.image | prepend: '/assets/img/members/' | relative_url }}" alt="{{ m.name }}" loading="lazy">
    {% endif %}
    <div class="member-name">{{ m.name }}</div>
    <div class="member-role">{{ m.role }}</div>
    {% if m.email %}<div class="member-links">{{ m.email | encode_email }}</div>{% endif %}
  </div>
  <div class="faculty-info">
    <div class="faculty-affil">{{ m.affiliation | newline_to_br }}</div>
    {% if m.research %}
    <div class="faculty-research">
      <div class="member-research-label">Research Area</div>
      {% assign areas = m.research | split: ", " %}
      <ul>
        {% for a in areas %}<li>{{ a | capitalize }}</li>{% endfor %}
      </ul>
    </div>
    {% endif %}
  </div>
</div>
  {% endfor %}
{% else %}
<div class="members-grid">
  {% for m in ms %}
  <div class="member">
    {% if m.image %}
    <img class="member-photo" src="{{ m.image | prepend: '/assets/img/members/' | relative_url }}" alt="{{ m.name }}" loading="lazy">
    {% else %}
    {% assign parts = m.name | split: " " %}
    <div class="member-photo member-placeholder" aria-hidden="true">{{ parts.first | slice: 0 }}{{ parts.last | slice: 0 }}</div>
    {% endif %}
    <div class="member-name">{{ m.name }}</div>
    <div class="member-role">{{ m.role }}</div>
    <div class="member-affil">{{ m.affiliation }}</div>
    {% if m.research %}<div class="member-research"><span class="member-research-label">Research Area</span> {{ m.research }}</div>{% endif %}
    {% if m.email %}<div class="member-links">{{ m.email | encode_email }}</div>{% endif %}
  </div>
  {% endfor %}
</div>
{% endif %}
  {% endif %}
{% endfor %}

## Join Our Lab

AGX Lab welcomes students and researchers interested in emotion, cognition, games, animation, and interactive media. We explore affective game computing and embodied experience through both creative and empirical approaches. No prior experience is required.

For applications or inquiries, please contact {{ "heeseonkim@cau.ac.kr" | encode_email }}.
