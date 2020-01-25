---
layout: page
permalink: /sitemap/
title: Sitemap
---

## Starting Out

If you're a linear person and want to know how this whole drama started, then check out the first two posts to read about [buying a Tiki 21]({% post_url 2019-01-15-every-boat-story-is-a-drama %}) and [then having it fall apart]({% post_url 2019-01-28-the-journey-and-launch %}). After that was a partial rebuild and then a full rebuild which you can find below.

## My Sailing Life .. So Far!

 * 1992 - College sailing class with Sunfish and small beach catamaran in Waco, Tx
 * 2002 - 2003 - Crewed on an E-scow on Canyon Ferry Reservoir, MT
 * 2003 - 2008 - Member of True North Sail Club on Canyon Ferry
 * 2008 - 2015 - Owned a MacGregor 22 - *Blue Mona*
 * 2015 - Purchased a Tiki 21 in Eastern Canada
 * 2016 - Retrieved the new boat only to have it fall apart in the water
 * 2017 - Rebuilt some of the parts of the boats
 * 2018 - Decided to rebuild the entire boat but didn't get finished before winter
 * 2018 - 2019 - Spent the winter in Ghana working on another Tiki 21
 * 2019 - 2020 - Spent the winter finishing my rebuild
 * 2020 - The first splash for [*Mona Risa*](% post_url 2019-04-05-name %) (I hope!)

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
