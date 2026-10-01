---
title: "Research"
permalink: /research/
eyebrow: "Papers &amp; projects"
lead: "I work on reinforcement learning, the reasoning of large language models, and trustworthy AI. Papers are listed newest first."
redirect_from:
  - /publications/
---
<h2 class="subhead">Papers</h2>
<ul class="papers">
  {%- for paper in site.data.publications %}
  {% include paper.html paper=paper %}
  {%- endfor %}
</ul>

{% if site.data.working_papers.size > 0 %}
<h2 class="subhead">Under review</h2>
<ul class="papers">
  {%- for w in site.data.working_papers %}
  <li class="paper reveal">
    <div class="paper__year" aria-hidden="true">…</div>
    <div>
      <div class="paper__tags"><span class="tag tag--plain">{{ w.status }}</span></div>
      <h3>{{ w.title }}</h3>
      <p class="paper__authors">With {{ w.with }}</p>
      <p class="paper__summary" style="margin-bottom: 0">{{ w.summary }}</p>
    </div>
  </li>
  {%- endfor %}
</ul>
{% endif %}
