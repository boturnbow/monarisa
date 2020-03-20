---
layout: page
permalink: /sitemap/
title: Sitemap
---

## Starting Out

If you're a linear person and want to know how this whole drama started, then check out the first two posts to read about [buying a Tiki 21]({% post_url 2019-01-15-every-boat-story-is-a-drama %}) and [then having it fall apart]({% post_url 2019-01-28-the-journey-and-launch %}). After that was a partial rebuild and **then** a full rebuild both detailed below.

[Why "Mona Risa"?]({% post_url 2019-04-05-name %})

I separated blog posts into broad *categories* to help sort them. Categories are roughly building versus sailing. With, hopefully, a lot more sailing posts to come! Categories are listed below.

Blog posts may also have *tags*. Tags are generally a part of the boat or a construction technique. Check out the [list of tags](/tags) to peruse in that manner.

## Post Categories

{%- assign sorted_categories = site.categories | sort -%}
{% for category in sorted_categories %}
  {% capture category_name %}{{ category | first }}{% endcapture %}
  <a name="{{ category_name }}"></a>
  <h3>{{ category_name | capitalize }}</h3>
  <ol>
    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
    {% for post in site.categories[category_name] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a>, {{ page.date | date: date_format }}</li>
    {% endfor %}
  </ol>
{% endfor %}
