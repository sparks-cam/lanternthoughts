---
layout: page
title: Tech
permalink: /tech/
---

Thoughtful reviews, tools, and notes on technology I actually use.

{% assign posts = site.posts
  | where_exp: "p", "p.tags contains 'tech'"
  | sort: "date"
  | reverse %}

<div class="container">
  <div class="row">
    {% if posts.size == 0 %}
      <div class="col col-12">
        <p>No tech posts yet.</p>
      </div>
    {% endif %}

    {% for post in posts %}
      {% include article.html %}
    {% endfor %}
  </div>
</div>
