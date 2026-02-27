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
    {% if article.citation_display and article.citation_display != "" %}
      <div class="citation-line">{{ article.citation_display | markdownify }}</div>
    {% endif %}
    {% if article.abstract and article.abstract != "" %}
      <p>{{ article.abstract | strip_html | truncate: 220 }}</p>
    {% endif %}
  </li>
{% endfor %}
</ul>
