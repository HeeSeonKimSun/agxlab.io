---
layout: about
title: About
permalink: /
subtitle: <b>정서 게임 경험 연구실</b> · <b>Affective Game Experience Lab</b> · Chung-Ang University

selected_papers: false # rendered in the body below so that section order can be controlled
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # rendered in the body below; limit/scrollable are still read by news.liquid
  scrollable: true
  limit: 3

latest_posts:
  enabled: false
---

<div class="agx-hero">
  <img class="agx-mark" src="{{ '/assets/img/agx_tile_lab.svg' | relative_url }}" width="56" height="56" alt="AGX Lab mark" loading="eager">
  <p>We seek to explore how emotion and cognition interact within games and interactive media. Grounded in affective game computing and cognitive science, our research aims to understand how affective signals and cognitive processes shape play, decision-making, and multimodal experience through experimental and creative approaches. Alongside empirical studies, the lab takes part in creative production in animation and games with industry and international partners.</p>
</div>

## Research Areas

<div class="area">
  <div class="area-title">Affective–Cognitive Interaction in Games</div>
  <p class="area-keywords">Affective game computing · Affective feedback loops · Behavioral modeling · Decision-making in play</p>
</div>

<div class="area">
  <div class="area-title">Embodied Interaction and Multimodal Player Analytics</div>
  <p class="area-keywords">Multimodal behavioral data · Reaction time and interaction patterns · Physiological signals · Telemetry and analysis pipelines</p>
</div>

<div class="area">
  <div class="area-title">Affective Experience through Animation and Interactive Media</div>
  <p class="area-keywords">Narrative and animation · Interactive media · Creative production as research method · Perception and meaning</p>
</div>

See the [research]({{ '/research/' | relative_url }}) page for the full description of each area and for key research outputs.

<h2><a href="{{ '/news/' | relative_url }}" style="color: inherit">News</a></h2>

{% include news.liquid limit=true %}

<h2><a href="{{ '/research/' | relative_url }}" style="color: inherit">Recent Projects &amp; Publications</a></h2>

{% include selected_papers.liquid %}

## Join Our Lab

AGX Lab welcomes students and researchers interested in emotion, cognition, games, animation, and interactive media. We explore affective game computing and embodied experience through both creative and empirical approaches. No prior experience is required: you can grow from the basics through research and projects.

The [contact]({{ '/contact/' | relative_url }}) page explains who we are looking for, what scholarships and funding are available, and where to find us, in English, Korean, and Chinese. For applications or enquiries, write to {{ "heeseonkim@cau.ac.kr" | encode_email }}.
