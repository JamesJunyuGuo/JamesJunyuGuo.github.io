---
title: "Notes"
permalink: /notes/
eyebrow: "Reading &amp; study notes"
lead: "Working notes on topics I am learning about. They are informal, and corrections are welcome."
redirect_from:
  - /portfolio/
---
<div class="grid grid--2">
  {%- for note in site.portfolio %}
  <a class="card reveal" href="{{ note.url | relative_url }}" style="--d: {{ forloop.index0 | times: 80 }}ms">
    <div class="card__meta"><span class="tag">Note</span></div>
    <h3>{{ note.title }}</h3>
    <p>{{ note.content | strip_html | truncatewords: 34 }}</p>
    <span class="card__cta">Read note {% include icon.html name="arrow-right" %}</span>
  </a>
  {%- endfor %}
</div>
