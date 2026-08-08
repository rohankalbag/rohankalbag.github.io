---
layout: default
title: Projects
permalink: /projects/
---

<style>
.projects-list .post {
  border-bottom: 1px solid rgba(255, 255, 255, 0.2);
  margin-bottom: 2rem;
  padding-bottom: 2rem;
}

.projects-list .post:last-child {
  border-bottom: 0;
}

.projects-pagination {
  display: flex;
  justify-content: space-between;
  margin: 2rem 0;
  color: gray;
  text-align: center;
}

.projects-pagination button {
  padding: 1rem;
  color: inherit;
  font: inherit;
  background: transparent;
  border: 1px solid var(--border-color);
  cursor: pointer;
}

.projects-pagination button:hover:not(:disabled),
.projects-pagination button:focus-visible {
  background-color: var(--border-color);
}

.projects-pagination button:disabled {
  cursor: default;
  opacity: 0.5;
}
</style>

<div class="posts projects-list">
  {% for post in site.posts %}
  {% unless post.categories contains 'blog' %}
  <article class="post project-item">
    <h2 class="post-title">
      <a href="{{ post.url | relative_url }}">
        {{ post.title }}
      </a>
    </h2>

    <time datetime="{{ post.date | date_to_xmlschema }}" class="post-date">{{ post.date | date_to_string }}</time>

    {{ post.content }}
  </article>
  {% endunless %}
  {% endfor %}
</div>

<div class="projects-pagination" aria-label="Project pagination">
  <button id="projects-previous" type="button">Previous</button>
  <span id="projects-page-number" aria-live="polite"></span>
  <button id="projects-next" type="button">Next</button>
</div>

<script>
  (function () {
    var items = Array.from(document.querySelectorAll('.project-item'));
    var pageSize = 10;
    var page = 1;
    var pageCount = Math.max(1, Math.ceil(items.length / pageSize));
    var previous = document.getElementById('projects-previous');
    var next = document.getElementById('projects-next');
    var pageNumber = document.getElementById('projects-page-number');

    function renderPage() {
      items.forEach(function (item, index) {
        item.hidden = index < (page - 1) * pageSize || index >= page * pageSize;
      });
      pageNumber.textContent = 'Page ' + page + ' of ' + pageCount;
      previous.disabled = page === 1;
      next.disabled = page === pageCount;
    }

    previous.addEventListener('click', function () {
      if (page > 1) {
        page -= 1;
        renderPage();
      }
    });

    next.addEventListener('click', function () {
      if (page < pageCount) {
        page += 1;
        renderPage();
      }
    });

    renderPage();
  }());
</script>
