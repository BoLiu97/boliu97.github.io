---
permalink: /
title: ""
excerpt: "About me"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---


------
I am a PhD student in Computer Science at Cornell Tech, co-advised by [Rajalakshmi Nandakumar](https://infosci.cornell.edu/~rajalakshmi/) and [Thijs Roumen](http://thijsroumen.eu/).

Before pursuing my PhD, I earned a master's degree in [Technology Innovation](https://gix.uw.edu/) at the University of Washington. I conducted research at [Ubicomp Lab](https://ubicomplab.cs.washington.edu/) and [Make4All](https://make4all.org/) advised by Shwetak Patel and Jennifer Mankoff, respectively.

My research has been focused on wearable devices, sensing, and healthcare. I am interested in how sensing technologies can guide physical assembly processes.

<p class="home-research-link"><a href="{{ '/research/' | relative_url }}">Explore selected research →</a> · <a href="{{ '/publications/' | relative_url }}">Publications</a></p>

## News & Updates

<ul class="news-list">
{% for item in site.data.news limit:3 %}{% include news-item.html item=item %}{% endfor %}
</ul>
<details class="news-earlier">
  <summary>Earlier updates</summary>
  <ul class="news-list">
  {% for item in site.data.news offset:3 %}{% include news-item.html item=item %}{% endfor %}
  </ul>
</details>
