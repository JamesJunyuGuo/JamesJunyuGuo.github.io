---
title: "Courses"
permalink: /course/
eyebrow: "Coursework"
lead: "Courses I have taken and the textbooks they used."
---
{% for g in site.data.courses %}
<h2 class="subhead">{{ g.group }}</h2>
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
