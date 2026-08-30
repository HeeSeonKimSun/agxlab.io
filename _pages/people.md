---
layout: page
title: people
permalink: /people/
description: Members of the Affective Game Experience Lab.
nav: true
nav_order: 4
---

{% assign groups = "Faculty|Graduate Students|Undergraduate Research Assistants|Alumni" | split: "|" %}
{% for g in groups %}
  {% assign ms = site.data.members | where: "group", g %}
  {% if ms.size > 0 %}
<h2 class="members-group">{{ g }}</h2>
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
    {% if m.email %}<div class="member-links"><a href="mailto:{{ m.email }}">{{ m.email }}</a></div>{% endif %}
    {% if m.url %}<div class="member-links"><a href="{{ m.url | relative_url }}">{{ m.url_label | default: "Profile" }}</a></div>{% endif %}
  </div>
  {% endfor %}
</div>
  {% endif %}
{% endfor %}

## Join our lab

AGX Lab welcomes students and researchers interested in emotion, cognition, and interactive media. We explore affective game computing and embodied experience through both creative and empirical approaches. No prior experience is required.

For applications or inquiries, please contact [heeseonkim@cau.ac.kr](mailto:heeseonkim@cau.ac.kr).
