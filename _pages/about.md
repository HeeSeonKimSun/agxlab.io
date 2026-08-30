---
layout: about
title: about
permalink: /
subtitle: <b>Affective Game Experience Lab</b> · Chung-Ang University

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
  <img class="agx-mark" src="{{ '/assets/img/agx_pixel_happy.gif' | relative_url }}" width="64" height="64" alt="AGX Lab pixel mark" loading="eager">
  <p>We seek to explore how emotion and cognition interact within games and interactive media. Grounded in affective game computing and cognitive science, our research aims to understand how affective signals and cognitive processes shape play, decision-making, and multimodal experience through experimental and creative approaches. Alongside empirical studies, the lab takes part in creative production in animation and games with industry and international partners.</p>
</div>

## research areas

<div class="area">
  <div class="area-title">Affective–Cognitive Interaction in Games</div>
  <p>Exploring how emotion and cognition interact to shape play, perception, and decision-making in interactive game environments through affective loops and behavioral modeling. Grounded in affective game computing, we model player affect computationally and design affective feedback loops that sense emotional and cognitive states from behavioral logs and physiological signals and feed them back into gameplay.</p>
</div>

<div class="area">
  <div class="area-title">Embodied Interaction and Multimodal Player Analytics</div>
  <p>Investigating embodied and predictive processes in gameplay using multimodal behavioral data, such as player choices, reaction time, interaction patterns, and physiological signals, together with the telemetry and analysis pipelines needed to capture and interpret them.</p>
</div>

<div class="area">
  <div class="area-title">Affective Experience through Animation and Interactive Media</div>
  <p>Exploring how emotional experience is formed and communicated through narrative, animation, and interactive media, to understand how affect shapes perception and meaning in digital environments. Animation and interaction design are also how we work: creative production runs alongside experiments, so prototypes, films, and games serve as both research instruments and outcomes.</p>
</div>

See the [research]({{ '/research/' | relative_url }}) page for key research outputs and the [projects]({{ '/projects/' | relative_url }}) page for collaborations.

<h2><a href="{{ '/news/' | relative_url }}" style="color: inherit">news</a></h2>

{% include news.liquid limit=true %}

<h2><a href="{{ '/research/' | relative_url }}" style="color: inherit">recent projects &amp; publications</a></h2>

{% include selected_papers.liquid %}

## join our lab

AGX Lab welcomes students and researchers interested in emotion, cognition, and interactive media. We explore affective game computing and embodied experience through both creative and empirical approaches. No prior experience is required: you can grow from the basics through research and projects.

AGX Lab, Chung-Ang University (Da Vinci Campus, Anseong, Korea). For applications or inquiries, please contact [heeseonkim@cau.ac.kr](mailto:heeseonkim@cau.ac.kr).
