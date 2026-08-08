---
layout: page
title: Blogs
permalink: /blogs/
---

<p class="page-intro">Notes, ideas, and technical explorations.</p>

{% assign blog_posts = site.posts | where_exp: "post", "post.categories contains 'blog'" %}

{% if blog_posts.size > 0 %}
<div class="blog-list">
  {% for post in blog_posts %}
  <article class="blog-list-item">
    <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: '%b %-d, %Y' }}</time>
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p>{{ post.excerpt | strip_html | strip_newlines | truncate: 220 }}</p>
    <a class="card-link" href="{{ post.url | relative_url }}">Read post <span aria-hidden="true">→</span></a>
  </article>
  {% endfor %}
</div>
{% else %}
<p class="empty-state">The blog is taking shape. Check back soon.</p>
{% endif %}
