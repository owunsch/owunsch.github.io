---
title: Articles
permalink: /articles/
---
# Articles

{% assign sorted_articles = site.articles | sort: 'year' | reverse %}

<ul class="article-list">
{% for work in sorted_articles %}
  <li class="article-item">
    <div class="work-card{% if work.image and work.image != '' %} has-thumb{% else %} no-thumb{% endif %}">
      {% if work.image and work.image != "" %}
        <a class="work-thumb" href="{{ work.url | relative_url }}">
          <img src="{{ work.image | relative_url }}" alt="{{ work.title }}">
        </a>
      {% endif %}
      <div class="work-head">
        <h2 class="work-title"><a href="{{ work.url | relative_url }}">{{ work.title }}</a></h2>
        {% if work.kind and work.kind != "" %}
          <p class="work-kind article-meta">
            {% if work.kind == "journal-article" %}Journal Article{% elsif work.kind == "book-chapter" %}Book Chapter{% else %}{{ work.kind }}{% endif %}
          </p>
        {% endif %}
      </div>
      <div class="work-details">
        {% if work.citation_display and work.citation_display != "" %}
          <div class="work-citation citation-line">{{ work.citation_display | markdownify }}</div>
        {% endif %}
        {% if work.abstract and work.abstract != "" %}
          <p class="work-abstract">{{ work.abstract | strip_html | truncate: 220 }}</p>
        {% endif %}
        {% if (work.pdf and work.pdf != "") or (work.doi and work.doi != "") %}
          <p class="work-links">
            {% if work.pdf and work.pdf != "" %}<a href="{{ work.pdf | relative_url }}">PDF</a>{% endif %}
            {% if work.pdf and work.pdf != "" and work.doi and work.doi != "" %} · {% endif %}
            {% if work.doi and work.doi != "" %}<a href="https://doi.org/{{ work.doi }}">DOI</a>{% endif %}
          </p>
        {% endif %}
      </div>
    </div>
  </li>
{% endfor %}
</ul>
