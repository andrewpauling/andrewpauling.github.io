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

<h2>Accepted</h2>
{% for post in site.publication reversed %}
   {% if post.pubtype == 'accepted' %}
      {% include archive-single.html %}
   {% endif %}
{% endfor %}

<h2>Under Review</h2>
{% for post in site.publications reversed %}
   {% if post.pubtype == 'review' %}
      {% include archive-single.html %}
   {% endif %}
{% endfor %}

<h2>Submitted</h2>
{% for post in site.publications reversed %}
   {% if post.pubtype == 'submitted' %}
      {% include archive-single.html %}
   {% endif %}
{% endfor %}

<h2>Published</h2>
{% for post in site.publications reversed %}
  {% if post.pubtype == 'published' %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
