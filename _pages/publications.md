---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---
<h3>Journals</h3>
23. Anoop, T. V., Vladimir Bobkov, and Pavel Drábek,"[Reverse Faber-Krahn and Szegő-Weinberger type inequalities for annular domains under Robin-Neumann boundary conditions]
(https://doi.org/10.1016/j.jde.2025.113354)", Journal of Differential Equations (2025), pp 40.   

<!-- New style rendering if publication categories are defined -->
{% if site.publication_category %}
  {% for category in site.publication_category  %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h2>{{ category[1].title }}</h2><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}



