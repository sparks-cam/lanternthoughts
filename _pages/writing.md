---
layout: page
title: Writing
permalink: /writing/
---

Essays and reflections on life, parenting, work, and creativity.

{% assign posts = site.posts
  | where_exp: "p", "p.tags contains 'writing'"
  | sort: "date"
  | reverse %}

<div class="container">
  <div class="row">
    {% if posts.size == 0 %}
      <div class="col col-12">
        <p>No writing posts yet.</p>
      </div>
    {% endif %}

    {% for post in posts %}
      {% include article.html %}
    {% endfor %}
  </div>
</div>
