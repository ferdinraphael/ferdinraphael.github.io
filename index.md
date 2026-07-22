---
layout: landing
title: 'Ferdin Raphael'
description: 'Writing, software, simple websites, project clarity, and practical experiments by Ferdin Raphael.'
permalink: /
eyebrow: 'Writing · Software · Experiments'
hero_title: 'Thinking deeply. Building practically.'
hero_subtitle: 'I use this space to think through ideas, build small useful things, and share what I learn along the way.'
hero_panel_badge: 'From thought to form'
hero_panel_title: 'Thoughts become pages. Ideas take form.'
hero_panel_text: 'A place for what I’m thinking through, building, and slowly making useful.'

# Optional public updates.
# Leave these unset until there is a real, public destination to link to.
#
# new_work:
#   eyebrow: 'New work'
#   title: 'Website in 2 Days is now live'
#   text: 'A focused service for creating clear, practical websites within a tightly defined scope.'
#   type: 'Service'
#   button_text: 'Visit the service'
#   url: 'https://example.com/'
#
# site_note:
#   date: '02 Aug 2026'
#   title: 'Technical work now has its own space'
#   text: 'Projects, repositories, technical writing, and services can now be found in a dedicated technical section.'
#   button_text: 'Visit the technical space'
#   url: '/tech/'
---

{% assign latest_post = site.posts | first %}
{% assign recent_posts = site.posts | slice: 1, 2 %}

{% if latest_post %}

<section class="page-section home-writing" aria-labelledby="latest-writing-title">
  <div class="container">
    <div class="section-heading home-section-heading">
      <p class="eyebrow" id="latest-writing-title">Latest writing</p>
    </div>

    <div class="writing-feature">
      <article class="writing-feature__main">
        {% assign current_year = site.time | date: "%Y" %}
        {% assign post_year = latest_post.date | date: "%Y" %}
        <p class="writing-meta">
          {{ latest_post.slice | default: "Identity" }} ·
          {% if post_year == current_year %}
            {{ latest_post.date | date: "%b %-d" }}
          {% else %}
            {{ latest_post.date | date: "%b %-d, %Y" }}
          {% endif %}
        </p>

        <h3>
          <a href="{{ latest_post.url | relative_url }}">
            {{ latest_post.title }}
          </a>
        </h3>

        {% if latest_post.description %}
          <p>{{ latest_post.description }}</p>
        {% else %}
          <p>{{ latest_post.excerpt | strip_html | truncate: 190 }}</p>
        {% endif %}

        <a class="text-link" href="{{ latest_post.url | relative_url }}">
          Read the latest post
        </a>
      </article>

      {% if recent_posts.size > 0 %}
      <div class="writing-feature__recent" aria-label="More recent writing">
        {% for post in recent_posts %}
        <article class="writing-compact">
          {% assign post_year = post.date | date: "%Y" %}
          <p class="writing-meta">
            {{ post.slice | default: "Identity" }} ·
            {% if post_year == current_year %}
              {{ post.date | date: "%b %-d" }}
            {% else %}
              {{ post.date | date: "%b %-d, %Y" }}
            {% endif %}
          </p>
          <h3>
            <a href="{{ post.url | relative_url }}">
              {{ post.title }}
            </a>
          </h3>
        </article>
        {% endfor %}

        <a class="text-link" href="{{ '/blog/' | relative_url }}">
          All posts →
        </a>
      </div>
      {% endif %}
    </div>

  </div>
</section>
{% endif %}

{% if page.new_work %}

<section class="page-section section-muted" aria-labelledby="new-work-title">
  <div class="container">
    <article class="new-work-block">
      <div>
        <p class="eyebrow">{{ page.new_work.eyebrow | default: "New work" }}</p>
        <h2 id="new-work-title">{{ page.new_work.title }}</h2>
        {% if page.new_work.text %}
          <p>{{ page.new_work.text }}</p>
        {% endif %}
      </div>

      <div class="new-work-block__action">
        {% if page.new_work.type %}
          <p class="writing-meta">{{ page.new_work.type }}</p>
        {% endif %}
        {% if page.new_work.button_text and page.new_work.url %}
          <a class="text-link" href="{{ page.new_work.url | relative_url }}">
            {{ page.new_work.button_text }}
          </a>
        {% endif %}
      </div>
    </article>

  </div>
</section>
{% endif %}

{% if page.site_note %}

<section class="page-section home-site-note-section" aria-labelledby="site-note-title">
  <div class="container">
    <aside class="site-note">
      <div>
        <p class="eyebrow">
          Site note{% if page.site_note.date %} · {{ page.site_note.date }}{% endif %}
        </p>
        <h2 id="site-note-title">{{ page.site_note.title }}</h2>
        {% if page.site_note.text %}
          <p>{{ page.site_note.text }}</p>
        {% endif %}
      </div>

      {% if page.site_note.button_text and page.site_note.url %}
        <a class="text-link" href="{{ page.site_note.url | relative_url }}">
          {{ page.site_note.button_text }}
        </a>
      {% endif %}
    </aside>

  </div>
</section>
{% endif %}

<section class="page-section section-muted home-purpose-section" aria-labelledby="thought-to-form-title">
  <div class="container">
    <div class="thought-to-form">
      <p class="status-badge">{{ page.hero_panel_badge }}</p>
      <h2 id="thought-to-form-title">{{ page.hero_panel_title }}</h2>
      <p>
        This is where I collect what I’m thinking through, building, learning,
        and gradually giving shape to.
      </p>
    </div>
  </div>
</section>

<section class="page-section home-explore-section" aria-labelledby="explore-title">
  <div class="container">
    <div class="explore-group">
      <p class="eyebrow home-explore-heading" id="explore-title">Explore</p>

      <a class="explore-card" href="{{ '/blog/' | relative_url }}">
        <div>
          <p class="status-badge">Writing</p>
          <h3>Writing across ideas, work, and life</h3>
          <p>
            Where I slow down, connect ideas, and work out what I think.
          </p>
        </div>
        <span class="explore-card__arrow" aria-hidden="true">→</span>
      </a>
    </div>

  </div>
</section>
