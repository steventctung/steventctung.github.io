---
layout: page
title: Research
subtitle: Current projects and research interests in mathematics
---

## Research Interests

My primary research interests lie at the intersection of mathematical analysis and partial differential equations. I am particularly drawn to:

- **Partial Differential Equations (PDEs)**: Theoretical foundations and analytical methods
- **Mathematical Analysis**: Real analysis, functional analysis, and measure theory
- **Applied Mathematics**: Computational approaches to solving differential equations
- **Mathematical Physics**: Applications of PDEs in physical systems

## Current Research

### Undergraduate Research Projects

{% for project in site.data.research %}
<div class="research-item">
    <h3 class="item-title">{{ project.title }}</h3>
    <div class="item-meta">
        {% if project.advisor %}
        <strong>Advisor:</strong> {{ project.advisor }} |
        {% endif %}
        <strong>Period:</strong> {{ project.period }}
        {% if project.status %}
        | <strong>Status:</strong> {{ project.status }}
        {% endif %}
    </div>
    <div class="item-description">
        <p>{{ project.description }}</p>
        {% if project.skills %}
        <p><strong>Skills/Methods:</strong> {{ project.skills | join: ", " }}</p>
        {% endif %}
        {% if project.links %}
        <div class="project-links">
            {% for link in project.links %}
            <a href="{{ link.url }}" target="_blank" class="btn btn-primary">{{ link.title }}</a>
            {% endfor %}
        </div>
        {% endif %}
    </div>
</div>
{% endfor %}

## Future Directions

As I transition into graduate studies, I am eager to deepen my understanding of:

- Advanced techniques in PDE theory
- Numerical methods for solving complex differential equations
- Applications of mathematical analysis to real-world problems
- Collaboration with researchers in applied mathematics and related fields

## Research Philosophy

Mathematics, at its core, is about discovering patterns and structures that govern our universe. Through my research in PDEs, I aim to contribute to our understanding of how mathematical models can capture and predict complex phenomena. I believe in the power of rigorous mathematical analysis combined with computational tools to solve challenging problems.

---

*If you're interested in discussing research opportunities or collaborations, please feel free to [contact me]({{ '/contact/' | relative_url }}).*