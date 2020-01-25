---
layout: page
permalink: /sitemap/
title: Sitemap
---

## Starting Out

If you're a linear person and want to know how this whole drama started, then check out the first two posts to read about [buying a Tiki 21]({% post_url 2019-01-15-every-boat-story-is-a-drama %}) and [then having it fall apart]({% post_url 2019-01-28-the-journey-and-launch %}). After that was a partial rebuild and then a full rebuild which you can find below.

## Post Categories

{% for category in site.categories %}
  {% capture category_name %}{{ category | first }}{% endcapture %}
  <a name="{{ category_name | slugize }}"></a>
  <h3>{{ category_name | capitalize }}</h3>
  <ul>
    {% for post in site.categories[category_name] %}
      <li><a href="{{ post.url }}">{{post.title}}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

## Post Tags

{% for tag in site.tags %}
  {% capture tag_name %}{{ tag | first }}{% endcapture %}
  <a name="tag-{{ tag_name | slugize }}"></a>
  <h3>{{ tag_name }}</h3>
  <ul>
    {% for post in site.tags[tag_name] %}
      <li><a href="{{ post.url }}">{{post.title}}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
