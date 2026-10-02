---
title: "Service"
permalink: /service/
eyebrow: "Academic service"
lead: "Reviewing for the machine learning community. I started reviewing in 2026 and try to give every paper the careful, grounded read I would want for my own."
---
<h2 class="subhead">Conference reviewing</h2>
<ul class="course-list">
  {%- for s in site.data.service.reviewing %}
  <li class="reveal">
    <div>
      <h3><small>{{ s.when }}</small>{{ s.role }}, {{ s.venue }}</h3>
      {% if s.note %}<p>{{ s.note }}</p>{% endif %}
    </div>
    {% if s.link %}<a class="btn btn--ghost btn--small" href="{{ s.link }}" rel="noopener">Conference {% include icon.html name="arrow-up-right" %}</a>{% endif %}
  </li>
  {%- endfor %}
</ul>
