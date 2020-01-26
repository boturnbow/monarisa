---
layout: page
permalink: /tags/
title: Tags
---

## Post Tags

<ul>
{% for tag in site.tags %}
  <li>{{ tag[0] }}</li>
{% endfor %}
</ul>

{% for tag in site.tags %}
  {% capture tag_name %}{{ tag | first }}{% endcapture %}
  <a name="{{ tag_name | slugize }}"></a>
  <h3>{{ tag_name }}</h3>
  <ul>
    {% for post in site.tags[tag_name] %}
      <li><a href="{{ post.url }}">{{post.title}}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
