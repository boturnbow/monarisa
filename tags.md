---
layout: page
permalink: /tags/
title: Tags
---

<a name="tagslist"></a>

<ul>
{%- assign sorted_tags = site.tags | sort -%}
{% for tag in sorted_tags %}
  {% capture tag_name %}{{ tag[0] }}{% endcapture %}
  <li><a href="#{{ tag_name }}">{{ tag_name }}</a></li>
{% endfor %}
</ul>

{% for tag in sorted_tags %}
  {% capture tag_name %}{{ tag[0] }}{% endcapture %}
  <a name="{{ tag_name }}"></a>
  <h4>{{ tag_name }}</h4>
  <ul>
    {% for post in sorted_tags[tag_name] %}
      <li><a href="{{ post.url }}">{{post.title}}</a></li>
    {% endfor %}
  </ul>
  <a href="#tagslist">Back to list of tags</a>
{% endfor %}
