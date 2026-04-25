---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% assign papers = site.publications | where_exp: "p", "p.category == nil" | sort: "date" | reverse %}
{% assign journals = site.publications | where: "category", "journal" | sort: "date" | reverse %}
{% assign patents = site.publications | where: "category", "patent" | sort: "date" | reverse %}

{% for post in papers %}
  {% include archive-single.html %}
{% endfor %}

{% if journals.size > 0 %}
<h2>Journal</h2>

{% for post in journals %}
  {% include archive-single.html %}
{% endfor %}
{% endif %}

{% if patents.size > 0 %}
<h2>Patents</h2>

{% for post in patents %}
  {% include archive-single.html %}
{% endfor %}
{% endif %}
