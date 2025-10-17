---
layout: page
title: Mathematical Notes
subtitle: Course notes, research notes, and mathematical explorations
---

<div class="notes-intro">
    <p>This collection contains notes from my mathematical studies, organized by topic but listed chronologically within each section. All notes are available as PDF downloads and cover various areas of mathematics that I've explored during my undergraduate studies.</p>
</div>

## Notes by Topic

{% assign notes_by_topic = site.data.notes | group_by: "topic" | sort: "name" %}

{% for topic_group in notes_by_topic %}
<div class="topic-section">
    <h3 class="topic-title">{{ topic_group.name }}</h3>

    {% assign topic_notes = topic_group.items | sort: "date" | reverse %}
    <ul class="note-list">
        {% for note in topic_notes %}
        <li class="note-item">
            {% if note.url %}
            <a href="{{ note.url | relative_url }}" class="note-link">
            {% elsif note.pdf %}
            <a href="{{ '/assets/pdfs/' | append: note.pdf | relative_url }}" class="note-link" target="_blank">
            {% else %}
            <div class="note-link">
            {% endif %}
                <div class="note-title">{{ note.title }}</div>
                <div class="note-meta">
                    <span class="note-date">{{ note.date | date: "%B %Y" }}</span>
                    {% if note.course %}
                    <span class="note-course"> • {{ note.course }}</span>
                    {% endif %}
                    {% if note.pages %}
                    <span class="note-pages"> • {{ note.pages }} pages</span>
                    {% endif %}
                </div>
                {% if note.description %}
                <div class="note-description">{{ note.description }}</div>
                {% endif %}
            {% if note.url or note.pdf %}
            </a>
            {% else %}
            </div>
            {% endif %}
        </li>
        {% endfor %}
    </ul>
</div>
{% endfor %}

{% if site.data.notes.size == 0 %}
<div class="no-notes">
    <p>Mathematical notes will appear here as they are added to the collection. Check back soon for updates!</p>
</div>
{% endif %}

## All Notes (Chronological)

{% assign all_notes = site.data.notes | sort: "date" | reverse %}

<div class="chronological-notes">
    <h3>Complete Timeline</h3>
    <div class="timeline">
        {% for note in all_notes %}
        <div class="timeline-item">
            <div class="timeline-date">{{ note.date | date: "%b %Y" }}</div>
            <div class="timeline-content">
                {% if note.url %}
                <a href="{{ note.url | relative_url }}" class="timeline-title">{{ note.title }}</a>
                {% elsif note.pdf %}
                <a href="{{ '/assets/pdfs/' | append: note.pdf | relative_url }}" class="timeline-title" target="_blank">{{ note.title }}</a>
                {% else %}
                <span class="timeline-title">{{ note.title }}</span>
                {% endif %}
                <div class="timeline-meta">
                    <span class="timeline-topic">{{ note.topic }}</span>
                    {% if note.course %}
                    <span class="timeline-course"> • {{ note.course }}</span>
                    {% endif %}
                </div>
            </div>
        </div>
        {% endfor %}
    </div>
</div>

{% if site.data.notes.size == 0 %}
<div class="no-notes">
    <p>The chronological timeline will appear here as notes are added.</p>
</div>
{% endif %}

---

<div class="notes-info">
    <h3>About These Notes</h3>
    <p>These notes represent my ongoing mathematical journey and serve multiple purposes:</p>
    <ul>
        <li><strong>Learning Documentation:</strong> Recording key concepts and theorems for future reference</li>
        <li><strong>Problem-Solving:</strong> Working through challenging problems and solutions</li>
        <li><strong>Research Preparation:</strong> Building foundations for advanced research topics</li>
        <li><strong>Knowledge Sharing:</strong> Making mathematical insights accessible to fellow students</li>
    </ul>
    <p>All notes are written in LaTeX and compiled to PDF for optimal mathematical notation rendering. If you find any errors or have questions about the content, please feel free to <a href="{{ '/contact/' | relative_url }}">reach out</a>.</p>
</div>

<style>
.notes-intro {
    background-color: #f8f9fa;
    padding: 1.5rem;
    border-radius: 8px;
    margin-bottom: 3rem;
    border-left: 4px solid #34495e;
}

.notes-intro p {
    margin-bottom: 0;
}

.no-notes {
    text-align: center;
    padding: 3rem 2rem;
    background-color: #f8f9fa;
    border-radius: 8px;
    margin: 2rem 0;
}

.no-notes p {
    font-style: italic;
    color: #666;
    margin-bottom: 0;
}

.chronological-notes {
    margin-top: 4rem;
    padding-top: 3rem;
    border-top: 2px solid #eee;
}

.timeline {
    margin-top: 2rem;
}

.timeline-item {
    display: flex;
    margin-bottom: 1.5rem;
    padding: 1rem;
    background-color: #f8f9fa;
    border-radius: 6px;
    transition: background-color 0.3s ease;
}

.timeline-item:hover {
    background-color: #e9ecef;
}

.timeline-date {
    min-width: 80px;
    font-weight: 600;
    color: #34495e;
    font-size: 0.9rem;
}

.timeline-content {
    flex: 1;
    margin-left: 1rem;
}

.timeline-title {
    font-size: 1.1rem;
    font-weight: 500;
    color: #2c3e50;
    text-decoration: none;
    border: none;
}

.timeline-title:hover {
    color: #34495e;
}

.timeline-meta {
    font-size: 0.85rem;
    color: #666;
    margin-top: 0.25rem;
}

.timeline-topic {
    background-color: #34495e;
    color: white;
    padding: 0.2rem 0.6rem;
    border-radius: 12px;
    font-size: 0.75rem;
}

.notes-info {
    background-color: #f8f9fa;
    padding: 2rem;
    border-radius: 8px;
    margin-top: 3rem;
}

.notes-info h3 {
    margin-top: 0;
    color: #2c3e50;
}

.notes-info ul {
    margin: 1rem 0;
    padding-left: 1.5rem;
}

.notes-info li {
    margin-bottom: 0.5rem;
}

@media (max-width: 600px) {
    .timeline-item {
        flex-direction: column;
    }

    .timeline-content {
        margin-left: 0;
        margin-top: 0.5rem;
    }

    .timeline-date {
        min-width: auto;
    }
}
</style>