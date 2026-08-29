---
layout: default
title: "Blog Feed"
permalink: /esu/
---

<section class="band">
  <div class="section-head">
    <h2>Blog Posts</h2>
  </div>
  
  <div class="archive-list" style="margin-top: 2rem;">
    {% for post in site.posts %}
      {% if post.category == "ESU" %}
        <div class="archive-item" style="padding: 1.5rem 0; border-bottom: 1px solid var(--rule-color, #eee);">
          <div class="kicker" style="margin-bottom: 0.25rem;">ESU · {{ post.date | date: "%d %B %Y" | upcase }}</div>
          <h3 style="margin: 0 0 0.5rem 0;"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          <p style="margin: 0; color: var(--text-muted);">{{ post.dek }}</p>
        </div>
      {% endif %}
    {% endfor %}
  </div>
</section>
