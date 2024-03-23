---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap"> My research Experience is demonstrated as follows, feel free to provide your previous suggestions.</div>
{% endif %}

{%  %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
