---
title: Book
permalink: /book/
---
# Book

## {{ site.book.title }}

<p class="book-meta">{{ site.book.publisher }}, {{ site.book.year }} ({{ site.book.status }})</p>

{% if site.book.description and site.book.description != "" %}
{{ site.book.description }}
{% else %}
Brief description placeholder. Add a short summary of the book's argument and scope.
{% endif %}

### Purchase / Library Links

- Publisher: {% if site.book.links.publisher != "" %}[Link]({{ site.book.links.publisher }}){% else %}TBD{% endif %}
- Amazon: {% if site.book.links.amazon != "" %}[Link]({{ site.book.links.amazon }}){% else %}TBD{% endif %}
- WorldCat: {% if site.book.links.worldcat != "" %}[Link]({{ site.book.links.worldcat }}){% else %}TBD{% endif %}
- Other: {% if site.book.links.other and site.book.links.other.size > 0 %}{% for item in site.book.links.other %}[{{ item.label }}]({{ item.url }}) {% endfor %}{% else %}TBD{% endif %}
