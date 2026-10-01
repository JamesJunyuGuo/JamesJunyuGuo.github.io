---
title: "Curriculum Vitae"
permalink: /cv/
eyebrow: "CV"
redirect_from:
  - /resume
  - /resume.html
---
<p><a class="btn" href="{{ site.author.cv | relative_url }}">Download PDF {% include icon.html name="download" %}</a></p>

{% assign sections = "education,experience,teaching,awards" | split: "," %}
{% assign titles = "Education,Experience,Teaching and research appointments,Honors and awards" | split: "," %}
{% for key in sections %}
<h2 class="subhead">{{ titles[forloop.index0] }}</h2>
<ul class="cv-list">
  {%- for item in site.data.cv[key] %}
  <li class="reveal">
    <span class="when">{{ item.when }}</span>
    <div>
      <h3>{{ item.title }}</h3>
      {% if item.place %}<p>{{ item.place }}</p>{% endif %}
      {% if item.note %}<p>{{ item.note }}</p>{% endif %}
    </div>
  </li>
  {%- endfor %}
</ul>
{% if key == "teaching" %}
<h2 class="subhead">Publications and preprints</h2>
<ul class="cv-list">
  {%- for p in site.data.publications %}
  <li class="reveal">
    <span class="when">{% if p.venue == "Preprint" %}{{ p.year }}{% else %}{{ p.venue }} {{ p.year }}{% endif %}</span>
    <div>
      <h3>{% if p.links %}<a href="{{ p.links[0].url }}">{{ p.title }}</a>{% else %}{{ p.title }}{% endif %}</h3>
      <p>{{ p.authors }}</p>
    </div>
  </li>
  {%- endfor %}
</ul>
{% endif %}
{% endfor %}
