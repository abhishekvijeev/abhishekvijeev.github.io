---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi! I'm a PhD student in Computer Science at UT Austin, advised by [Prof. Vijay Chidambaram](https://www.cs.utexas.edu/~vijay//). My research interests lie broadly in computer systems.


## Publications

<style>
.home-publications {
  font-size: 0.9em;
  line-height: 1.35;
}

.home-publications .publication {
  margin-bottom: 0.65rem;
}

.home-publications .publication-title {
  display: block;
  font-weight: 600;
  margin-bottom: 0.1rem;
}

.home-publications .publication-meta {
  display: block;
  font-size: 0.88em;
  color: var(--global-text-color-dark);
  /* color: black; */
}

.home-publications .publication-authors {
  display: block;
  max-width: 80%;
  white-space: normal;
  overflow-wrap: break-word;
}

.home-publications .publication-authors::-webkit-scrollbar {
  display: none; /* Chrome, Safari, Edge */
}
</style>




{% assign recent_publications = site.publications | sort: "date" | reverse %}

<div class="home-publications">
{% for post in recent_publications limit: 5 %}
  <div class="publication">

    {% if post.paperurl %}
      <a class="publication-title"
        href="{{ post.paperurl | relative_url }}"
        target="_blank"
        rel="noopener noreferrer">
        {{ post.title }}
      </a>
    {% else %}
      <span class="publication-title">
        {{ post.title }}
      </span>
    {% endif %}

    <span class="publication-meta publication-authors">
      {{ post.authors }}
    </span>

    <span class="publication-meta">
      {{ post.venue }}
    </span>

  </div>
{% endfor %}
</div>







<!-- {% assign recent_publications = site.publications | sort: "date" | reverse %}

{% for post in recent_publications limit: 5 %}
  {% include archive-single.html %}
{% endfor %}

[View all publications]({{ '/publications/' | relative_url }}) -->