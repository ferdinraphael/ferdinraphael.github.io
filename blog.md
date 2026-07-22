---
layout: page
title: 'Writing'
description: 'Notes and reflections by Ferdin Raphael.'
permalink: /blog/
---

This is where I slow down, connect ideas, and work out what I think.

Some posts may be practical. Some may be exploratory. Over time, this page will collect the ideas and patterns I keep returning to.

{% if site.posts.size > 0 %}

  <div class="grid mt-xl">
    {% for post in site.posts %}
      {% include blog-card.html post=post %}
    {% endfor %}
  </div>
{% else %}
  <p class="empty-state">The first post will be added soon.</p>
{% endif %}
