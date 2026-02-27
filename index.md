---
title: Home
---
<figure class="home-headshot">
  <img
    src="{{ '/assets/img/headshot-optimized.jpg' | relative_url }}"
    alt="Oliver Wunsch"
    loading="lazy">
</figure>

# {{ site.site_owner.name }}

{{ site.home_intro.short_blurb }}

{% if site.site_owner.affiliation %}
{{ site.site_owner.affiliation }}
{% endif %}

- [Book]({{ '/book/' | relative_url }})
- [Articles]({{ '/articles/' | relative_url }})
