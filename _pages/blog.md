---
title: "Blog"
permalink: /blog/
eyebrow: "Posts"
lead: "Occasional posts about life as a Ph.D. student at Berkeley."
redirect_from:
  - /year-archive/
---
{%- assign by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" -%}
{% for year in by_year %}
<h2 class="subhead">{{ year.name }}</h2>
<ul class="post-list">
  {%- for post in year.items %}
  <li class="reveal">
    <a href="{{ post.url | relative_url }}">
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%b %-d" }}</time>
      <h3>{{ post.title }}</h3>
      {% include icon.html name="arrow-right" %}
      <p>{{ post.content | strip_html | truncatewords: 30 }}</p>
    </a>
  </li>
  {%- endfor %}
</ul>
{% endfor %}
<p style="margin-top: 32px"><a class="more-link" href="{{ '/feed.xml' | relative_url }}">{% include icon.html name="rss" %} Subscribe via RSS</a></p>
