---
layout: page
title: people
permalink: /people/
description: Members of the Affective Game Experience Lab.
nav: true
nav_order: 2
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
    {% endif %}
    <div class="member-name">{{ m.name }}</div>
    <div class="member-role">{{ m.role }}</div>
    <div class="member-affil">{{ m.affiliation }}</div>
    {% if m.email %}<div class="member-links"><a href="mailto:{{ m.email }}">{{ m.email }}</a></div>{% endif %}
  </div>
  {% endfor %}
</div>
  {% endif %}
{% endfor %}

## Join our lab

AGX Lab welcomes students and researchers interested in emotion, cognition, and interactive media. We seek to explore affective game computing and embodied experience through both creative and empirical approaches.

<p class="ko">AGX Lab에 참여하세요! 감정, 인지, 게임과 애니메이션을 포함한 인터랙티브 미디어에 관심 있는 학생과 연구자를 모집합니다. 사전 경험이 없어도 참여 가능하며, 연구와 프로젝트를 통해 기초부터 성장할 수 있습니다.</p>

For applications or inquiries, please contact [heeseonkim@cau.ac.kr](mailto:heeseonkim@cau.ac.kr).
