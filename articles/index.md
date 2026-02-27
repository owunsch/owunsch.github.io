---
title: Articles
permalink: /articles/
---
# Articles

{% assign sorted_articles = site.articles | sort: 'year' | reverse %}

<ul class="article-list">
{% for article in sorted_articles %}
  <li class="article-item">
    <h2><a href="{{ article.url | relative_url }}">{{ article.title }}</a></h2>
    <p class="article-meta">
      {{ article.year }}
      {% if article.venue %} · {{ article.venue }}{% endif %}
      {% if article.book_title %} · {{ article.book_title }}{% endif %}
    </p>
    {% if article.abstract %}
      <p>{{ article.abstract | strip_html | truncate: 180 }}</p>
    {% endif %}
    {% if article.tags and article.tags.size > 0 %}
      <ul class="tag-list">
        {% for tag in article.tags %}
          <li>{{ tag }}</li>
        {% endfor %}
      </ul>
    {% endif %}
  </li>
{% endfor %}
</ul>
