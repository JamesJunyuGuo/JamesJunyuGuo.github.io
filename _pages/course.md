---
title: "Teaching & Courses"
permalink: /course/
eyebrow: "Teaching &amp; coursework"
lead: "Courses I have helped teach, and courses I have taken with the textbooks they used."
---
<h2 class="subhead">Teaching</h2>
<ul class="course-list">
  {%- for t in site.data.teaching %}
  <li class="reveal">
    <div>
      <h3>{% if t.code %}<small>{{ t.code }}</small>{% endif %}{{ t.name }}</h3>
      <p>{{ t.role }} · {{ t.where }}</p>
    </div>
    {% if t.link %}<a class="btn btn--ghost btn--small" href="{{ t.link }}" rel="noopener">Course page {% include icon.html name="arrow-up-right" %}</a>{% endif %}
  </li>
  {%- endfor %}
</ul>

{% for g in site.data.courses %}
<h2 class="subhead">Courses taken: {{ g.group | downcase }}</h2>
<ul class="course-list">
  {%- for c in g.courses %}
  <li class="reveal">
    <div>
      <h3>{% if c.code %}<small>{{ c.code }}</small>{% endif %}{{ c.name }}</h3>
      <p>{{ c.where }}</p>
    </div>
    {% if c.textbook %}<a class="btn btn--ghost btn--small" href="{{ c.textbook }}" rel="noopener">Textbook {% include icon.html name="arrow-up-right" %}</a>{% endif %}
  </li>
  {%- endfor %}
</ul>
{% endfor %}
