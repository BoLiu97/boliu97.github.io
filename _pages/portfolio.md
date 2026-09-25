---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
excerpt: "Selected research on sensing, physical assembly, fabrication, and interactive systems."
---

<div class="research-intro">
  <p class="research-kicker">Selected projects</p>
  <p>I explore how sensing and interactive tools can support physical tasks, from assembly and fabrication to wearable and accessible interaction.</p>
  <a href="{{ '/publications/' | relative_url }}">View all publications <span aria-hidden="true">→</span></a>
</div>

<div class="research-projects">
{% assign featured_projects = site.data.projects | where: 'featured', true %}
{% for project in featured_projects %}{% include research-card.html project=project %}{% endfor %}
</div>

<details class="research-earlier">
  <summary>Earlier projects</summary>
  <ul>
    <li><a href="{{ '/portfolio/SmartRecorder/' | relative_url }}">SmartRecorder</a> — Creating smartphone video tutorials from demonstrations.</li>
    <li><a href="{{ '/portfolio/SoundShirt/' | relative_url }}">SoundShirt</a> — Exploring e-textiles for body movement tracking.</li>
    <li><a href="{{ '/portfolio/microbiome/' | relative_url }}">Microbiome</a> — Studying experiences with digestive-health tracking tools.</li>
  </ul>
</details>
