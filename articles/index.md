---
title: Articles
permalink: /articles/
---
# Articles

{% assign sorted_articles = site.articles | sort: 'year' | reverse %}

<ul class="article-list">
{% for work in sorted_articles %}
  <li class="article-item">
    <div class="work-card{% unless work.image and work.image != '' %} work-card--no-thumb{% endunless %}">
      {% if work.image and work.image != "" %}
        <a class="work-thumb" href="{{ work.url | relative_url }}">
          <img src="{{ work.image | relative_url }}" alt="{{ work.title }}">
        </a>
      {% endif %}
      <div class="work-body">
        <h2><a href="{{ work.url | relative_url }}">{{ work.title }}</a></h2>
        {% if work.kind and work.kind != "" %}
          <p class="article-meta">
            {% if work.kind == "journal-article" %}Journal Article{% elsif work.kind == "book-chapter" %}Book Chapter{% else %}{{ work.kind }}{% endif %}
          </p>
        {% endif %}
        {% if work.citation_display and work.citation_display != "" %}
          <div class="citation-line">{{ work.citation_display | markdownify }}</div>
        {% endif %}
        {% if work.abstract and work.abstract != "" %}
          <p>{{ work.abstract | strip_html | truncate: 220 }}</p>
        {% endif %}
      </div>
    </div>
  </li>
{% endfor %}
</ul>
