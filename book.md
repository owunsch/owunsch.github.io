---
title: Book
permalink: /book/
reviews:
  - quote: "In an era of scholarship drunk on the sociological demystification of art, Oliver Wunsch’s book offers us that rare thing—a study of the social forces shaping art that illuminates aesthetic achievement."
    reviewer: "Michael W. Clune"
    publication: "Critical Inquiry"
    url: "https://criticalinquiry.uchicago.edu/michael_clune_reviews_a_delicate_matter/"
  - quote: "Wunsch’s elegant, jargon-free writing deftly integrates voices from numerous primary sources and presents complex ideas with a remarkable balance of clarity and nuance."
    reviewer: "Mimi Hellman"
    publication: "CAA Reviews"
    url: "https://www.caareviews.org/reviews/4255"
  - quote: "Central to Wunsch’s remarkably tight-focused book is the suggestion that the perishability of art, long seen by art historians as little more than an impediment to research, is a subject of interest in itself; a feature, rather than a bug."
    reviewer: "Kirsten Tambling"
    publication: "Apollo Magazine"
    url: "https://apollo-magazine.com/delicate-matter-18th-century-french-art-oliver-wunsch-review/"
  - quote: "Wunsch describes the ongoing struggle to create desirable art objects that would resist the vagaries of fashion. With its organisation according to medium, the book unfolds under the sign of the material turn in the field of art history. Yet it is as much a book about the discursive work that arose in the wake of technical experimentation, as critics and artists sought to resist the pleasure of things, the thingness of artworks, and the delirium of consumption."
    reviewer: "Marika Takanishi Knowles"
    publication: "French History"
    url: "https://academic.oup.com/fh/article-abstract/38/4/510/7821507?redirectedFrom=fulltext"
  - quote: "[Wunsch] shows that material impermanence is not just the bane of conservators, or a cause for regret, but deserves investigation as a cultural phenomenon in its own right. . . . A Delicate Matter succeeds in combining a meticulous discussion of visual and material forms with eighteenth-century philosophical reflection and wider sociocultural shifts. It is concise, tightly argued, beautifully designed and provocative"
    reviewer: "Tom Stammers"
    publication: "Burlington Magazine"
    url: "https://www.burlington.org.uk/archive/back-issues/202412"
  - quote: "A Delicate Matter is an important contribution to the material history of eighteenth-century French art, and its focus on major artists, combined with its sharp assessment of the new social and economic dynamics governing the eighteenth-century art world, also makes it an essential reading for non-specialists, who will appreciate its clear and vivid prose."
    reviewer: "Frédérique Baumgartner"
    publication: "Journal for Eighteenth-Century Studies"
    url: "https://doi.org/10.1111/1754-0208.12978"
  - quote: "This handsomely designed and illustrated volume is an original, concise, and brilliant study of the concept and nature of delicacy across four eighteenth-century French case-studies and an epilogue."
    reviewer: "Mark Ledbury"
    publication: "Journal of the History of Collections"
    url: "https://academic.oup.com/jhc/advance-article-abstract/doi/10.1093/jhc/fhaf039/8371856"
---
# Book

## {{ site.book.title }}

<p class="book-meta">{{ site.book.publisher }}, {{ site.book.year }}</p>

{% if site.book.description and site.book.description != "" %}
{{ site.book.description }}
{% else %}
Brief description placeholder. Add a short summary of the book's argument and scope.
{% endif %}

{% if page.reviews and page.reviews.size > 0 %}
## Selected Reviews

<section class="reviews-list" aria-label="Selected reviews">
  {% for review in page.reviews %}
    <article class="review-item">
      <p class="review-quote">{{ review.quote }}</p>
      <p class="review-attribution">&mdash; {{ review.reviewer }}, <a href="{{ review.url }}" target="_blank" rel="noopener noreferrer">{{ review.publication }}</a></p>
    </article>
  {% endfor %}
</section>
{% endif %}

### Purchase / Library Links

- Publisher: {% if site.book.links.publisher != "" %}[Link]({{ site.book.links.publisher }}){% else %}TBD{% endif %}
- WorldCat: {% if site.book.links.worldcat != "" %}[Link]({{ site.book.links.worldcat }}){% else %}TBD{% endif %}
