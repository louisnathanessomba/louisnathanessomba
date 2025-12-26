---
title: Mathematics
layout: section_with_posts
---

# *Original research in probability, statistics, and applied mathematics.*

This subsection dives into **mathematic experiments** that power my projects. It is here that I apply the skills I learn regularly in mathematics.

---

## **Featured Research**
### **[Bayesian Probability in Industrial Systems]({{ "/Exploring-Frontiers/Independently-Search/mathematics/_posts/bayesian-industry" | relative_url }})**
![Bayesian Industry]({{ "/assets/diagrams/portrait.jpg" | relative_url }})
Using Bayesian statistics to **optimize waste recycling** in Cameroon’s industrial sector—directly applied in [WhirlWing]({{ "/Applied-Works/whirlwing/ethics" | relative_url }}).

### **[Linear Algebra for Edge AI]({{ "/Exploring-Frontiers/Independently-Search/mathematics/_posts/linear-algebra-edge" | relative_url }})**
![Linear Algebra]({{ "/assets/diagrams/linear-algebra-edge.png" | relative_url }})
How **matrix decompositions** enable efficient AI on low-power devices like Raspberry Pi.

---

## **All Mathematics Research**
{% for post in site.exploring_frontiers %}
{% if post.category == "mathematics/_posts" && post <> "index.md" %}
<div class="math-post-block">
  <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
  {% if post.featured_image %}
  ![{{ post.featured_alt }}]({{ post.featured_image | relative_url }})
  {% elsif post.featured_video %}
  <video controls>
    <source src="{{ post.featured_video | relative_url }}" type="video/mp4">
  </video>
  {% endif %}
  <p>{{ post.excerpt }}</p>
  <div class="post-meta">
    {% if post.related_project %}
    <span class="related-link">
      🔗 Related Project: <a href="{{ post.related_project | relative_url }}">{{ post.related_project_title }}</a>
    </span>
    {% endif %}
    {% if post.tags %}
    <span class="tags">
      🏷️ Tags: {{ post.tags | join: ", " }}
    </span>
    {% endif %}
  </div>
  <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
</div>
{% endif %}
{% endfor %}
