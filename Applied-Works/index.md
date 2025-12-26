---
title: Applied Works
layout: section_with_posts
---

# *Data-driven projects applying my theses to real-world challenges.*

This section showcases **scalable, ethical, and ecological projects**—each designed to solve practical problems while aligning with my core principles. Every project is divided into:
- **Intro**: Purpose and vision.
- **Technical Details**: Architecture, tools, and implementation.
- **Ethical/Ecological Thoughts**: Impact, sustainability, and ethical considerations.

---

{% for project in site.applied_works %}
<div class="project-block">
  <h2><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2>

  {% if project.featured_image %}
  ![{{ project.featured_alt }}]({{ project.featured_image | relative_url }})
  {% elsif project.featured_video %}
  <video controls>
    <source src="{{ project.featured_video | relative_url }}" type="video/mp4">
  </video>
  {% endif %}

  <p>{{ project.excerpt }}</p>

  <div class="project-sections">
    <div class="section-nav">
      <a href="{{ project.url | relative_url }}#intro">Intro</a>
      <a href="{{ project.url | relative_url }}#technical">Technical Details</a>
      <a href="{{ project.url | relative_url }}#ethics">Ethics & Ecology</a>
    </div>
  </div>

  <div class="project-meta">
    {% if project.related_thesis %}
    <span class="related-link">
      Related Thesis: <a href="{{ project.related_thesis | relative_url }}">{{ project.related_thesis_title }}</a>
    </span>
    {% endif %}
    {% if project.related_research %}
    <span class="related-link">
      Related Research: <a href="{{ project.related_research | relative_url }}">{{ project.related_research_title }}</a>
    </span>
    {% endif %}
  </div>

  <a href="{{ project.url | relative_url }}" class="read-more">Explore Project →</a>
</div>
{% endfor %}
