---
layout: page
permalink: /tags/
title: Tags
---

<a name="#tagslist"></a>
## Post Tags

<ul>
{% for tag in site.tags %}
  {% capture tag_name %}{{ tag[0] }}{% endcapture %}
  <li><a href="#{{ tag_name }}">{{ tag_name }}</a></li>
{% endfor %}
</ul>

{% for tag in site.tags %}
  {% capture tag_name %}{{ tag[0] }}{% endcapture %}
  <a name="{{ tag_name }}"></a>
  <h3>{{ tag_name }}</h3>
  <ul>
    {% for post in site.tags[tag_name] %}
      <li><a href="{{ post.url }}">{{post.title}}</a></li>
    {% endfor %}
  </ul>
  <a href="#tagslist">Back to list of tags</a>
{% endfor %}
