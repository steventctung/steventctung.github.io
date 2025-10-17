---
layout: page
title: Publications
subtitle: Academic papers, preprints, and mathematical contributions
permalink: /publications/
---

## Journal Articles

{% assign journal_papers = site.data.publications | where: "type", "journal" %}
{% if journal_papers.size > 0 %}
{% for paper in journal_papers %}
<div class="publication-item">
    <h3 class="item-title">{{ paper.title }}</h3>
    <div class="item-meta">
        <strong>Authors:</strong> {{ paper.authors | join: ", " }} |
        <strong>{{ paper.journal }}</strong>
        {% if paper.volume %}, Vol. {{ paper.volume }}{% endif %}
        {% if paper.pages %}, pp. {{ paper.pages }}{% endif %}
        ({{ paper.year }})
    </div>
    <div class="item-description">
        {% if paper.abstract %}
        <p>{{ paper.abstract }}</p>
        {% endif %}
        {% if paper.links %}
        <div class="publication-links">
            {% for link in paper.links %}
            <a href="{{ link.url }}" target="_blank" class="btn btn-primary">{{ link.title }}</a>
            {% endfor %}
        </div>
        {% endif %}
    </div>
</div>
{% endfor %}
{% else %}
<p class="no-publications">Journal publications will be listed here as they become available.</p>
{% endif %}

## Preprints

{% assign preprints = site.data.publications | where: "type", "preprint" %}
{% if preprints.size > 0 %}
{% for paper in preprints %}
<div class="publication-item">
    <h3 class="item-title">{{ paper.title }}</h3>
    <div class="item-meta">
        <strong>Authors:</strong> {{ paper.authors | join: ", " }} |
        {% if paper.arxiv %}
        <strong>arXiv:</strong> {{ paper.arxiv }} |
        {% endif %}
        <strong>Year:</strong> {{ paper.year }}
        {% if paper.status %}
        | <strong>Status:</strong> {{ paper.status }}
        {% endif %}
    </div>
    <div class="item-description">
        {% if paper.abstract %}
        <p>{{ paper.abstract }}</p>
        {% endif %}
        {% if paper.links %}
        <div class="publication-links">
            {% for link in paper.links %}
            <a href="{{ link.url }}" target="_blank" class="btn btn-primary">{{ link.title }}</a>
            {% endfor %}
        </div>
        {% endif %}
    </div>
</div>
{% endfor %}
{% else %}
<p class="no-publications">Preprints and working papers will be listed here as they become available.</p>
{% endif %}

## Conference Presentations

{% assign presentations = site.data.publications | where: "type", "presentation" %}
{% if presentations.size > 0 %}
{% for presentation in presentations %}
<div class="publication-item">
    <h3 class="item-title">{{ presentation.title }}</h3>
    <div class="item-meta">
        <strong>{{ presentation.conference }}</strong> |
        <strong>{{ presentation.location }}</strong> |
        <strong>{{ presentation.date }}</strong>
        {% if presentation.type_detail %}
        | <strong>Type:</strong> {{ presentation.type_detail }}
        {% endif %}
    </div>
    <div class="item-description">
        {% if presentation.abstract %}
        <p>{{ presentation.abstract }}</p>
        {% endif %}
        {% if presentation.links %}
        <div class="publication-links">
            {% for link in presentation.links %}
            <a href="{{ link.url }}" target="_blank" class="btn btn-primary">{{ link.title }}</a>
            {% endfor %}
        </div>
        {% endif %}
    </div>
</div>
{% endfor %}
{% else %}
<p class="no-publications">Conference presentations will be listed here as they become available.</p>
{% endif %}

## Thesis and Major Projects

{% assign theses = site.data.publications | where: "type", "thesis" %}
{% if theses.size > 0 %}
{% for thesis in theses %}
<div class="publication-item">
    <h3 class="item-title">{{ thesis.title }}</h3>
    <div class="item-meta">
        <strong>{{ thesis.degree }}</strong> |
        <strong>{{ thesis.institution }}</strong> |
        <strong>{{ thesis.year }}</strong>
        {% if thesis.advisor %}
        | <strong>Advisor:</strong> {{ thesis.advisor }}
        {% endif %}
    </div>
    <div class="item-description">
        {% if thesis.abstract %}
        <p>{{ thesis.abstract }}</p>
        {% endif %}
        {% if thesis.links %}
        <div class="publication-links">
            {% for link in thesis.links %}
            <a href="{{ link.url }}" target="_blank" class="btn btn-primary">{{ link.title }}</a>
            {% endfor %}
        </div>
        {% endif %}
    </div>
</div>
{% endfor %}
{% else %}
<p class="no-publications">Senior thesis and major projects will be listed here upon completion.</p>
{% endif %}

---

<div class="publication-note">
    <p><strong>Note:</strong> This page will be updated regularly as new publications, preprints, and presentations become available. For the most current information, please check my <a href="{{ '/cv/' | relative_url }}">CV</a> or <a href="{{ '/contact/' | relative_url }}">contact me</a> directly.</p>
</div>

<style>
.no-publications {
    font-style: italic;
    color: #666;
    text-align: center;
    padding: 2rem;
    background-color: #f8f9fa;
    border-radius: 8px;
    margin-bottom: 2rem;
}

.publication-links {
    margin-top: 1rem;
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
}

.publication-note {
    background-color: #f8f9fa;
    border-left: 4px solid #34495e;
    padding: 1.5rem;
    border-radius: 4px;
    margin-top: 2rem;
}

.publication-note p {
    margin-bottom: 0;
}

@media (max-width: 600px) {
    .publication-links {
        flex-direction: column;
    }
}
</style>