---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
excerpt: "Selected publications by Bo Liu in human-computer interaction, sensing, and digital fabrication."
---

<p>Selected publications. See also <a href="{{ site.author.googlescholar }}">Google Scholar</a> and <a href="{{ '/research/' | relative_url }}">selected research projects</a>.</p>

{% assign sorted_publications = site.data.publications | sort: 'year' | reverse %}
{% assign years = sorted_publications | map: 'year' | uniq %}
{% for year in years %}
<section class="publication-year" aria-labelledby="year-{{ year }}">
  <h2 id="year-{{ year }}">{{ year }}</h2>
  {% assign year_publications = site.data.publications | where: 'year', year %}
  {% for publication in year_publications %}{% include publication-entry.html publication=publication %}{% endfor %}
</section>
{% endfor %}
