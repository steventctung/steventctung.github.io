---
layout: page
title: Curriculum Vitae
subtitle: Academic background and achievements
---

<div class="cv-download">
    <p><a href="{{ '/assets/pdfs/steven_tung_cv.pdf' | relative_url }}" class="btn btn-primary" target="_blank">Download PDF Version</a></p>
</div>

## Education

<div class="cv-section">
    <div class="cv-item">
        <div class="cv-item-header">
            <span class="cv-item-title">Bachelor of Arts in Mathematics</span>
            <span class="cv-item-date">Expected May 2025</span>
        </div>
        <div class="cv-item-subtitle">Rutgers University, New Brunswick, NJ</div>
        <div class="cv-item-description">
            <p>Concentration in Pure Mathematics with focus on Partial Differential Equations</p>
            <p><strong>Relevant Coursework:</strong> Real Analysis, Complex Analysis, Abstract Algebra, Differential Equations, Topology, Mathematical Physics</p>
        </div>
    </div>
</div>

## Research Experience

<div class="cv-section">
    {% for project in site.data.research %}
    <div class="cv-item">
        <div class="cv-item-header">
            <span class="cv-item-title">{{ project.title }}</span>
            <span class="cv-item-date">{{ project.period }}</span>
        </div>
        {% if project.advisor %}
        <div class="cv-item-subtitle">Advisor: {{ project.advisor }}</div>
        {% endif %}
        <div class="cv-item-description">
            <p>{{ project.description }}</p>
            {% if project.skills %}
            <p><strong>Methods:</strong> {{ project.skills | join: ", " }}</p>
            {% endif %}
        </div>
    </div>
    {% endfor %}
</div>

## Academic Achievements

<div class="cv-section">
    <div class="cv-item">
        <div class="cv-item-header">
            <span class="cv-item-title">Dean's List</span>
            <span class="cv-item-date">Fall 2023, Spring 2024</span>
        </div>
        <div class="cv-item-description">
            <p>Recognition for academic excellence with GPA above 3.5</p>
        </div>
    </div>

    <div class="cv-item">
        <div class="cv-item-header">
            <span class="cv-item-title">Mathematics Department Scholarship</span>
            <span class="cv-item-date">2023-2024</span>
        </div>
        <div class="cv-item-description">
            <p>Merit-based scholarship for outstanding performance in mathematics courses</p>
        </div>
    </div>
</div>

## Publications & Presentations

<div class="cv-section">
    {% assign cv_publications = site.data.publications %}
    {% if cv_publications.size > 0 %}
        {% for publication in cv_publications %}
        <div class="cv-item">
            <div class="cv-item-header">
                <span class="cv-item-title">{{ publication.title }}</span>
                <span class="cv-item-date">{{ publication.year }}</span>
            </div>
            <div class="cv-item-subtitle">
                {{ publication.authors | join: ", " }}
                {% if publication.journal %} - {{ publication.journal }}{% endif %}
                {% if publication.conference %} - {{ publication.conference }}{% endif %}
            </div>
        </div>
        {% endfor %}
    {% else %}
    <div class="cv-item">
        <div class="cv-item-description">
            <p><em>Publications and presentations will be listed here as they become available.</em></p>
        </div>
    </div>
    {% endif %}
</div>

## Teaching & Mentoring

<div class="cv-section">
    <div class="cv-item">
        <div class="cv-item-header">
            <span class="cv-item-title">Undergraduate Teaching Assistant</span>
            <span class="cv-item-date">Fall 2024</span>
        </div>
        <div class="cv-item-subtitle">Calculus I, Rutgers University</div>
        <div class="cv-item-description">
            <p>Assisted students during recitation sessions, graded assignments, and held office hours</p>
        </div>
    </div>

    <div class="cv-item">
        <div class="cv-item-header">
            <span class="cv-item-title">Peer Tutor</span>
            <span class="cv-item-date">2023-2024</span>
        </div>
        <div class="cv-item-subtitle">Mathematics Learning Center, Rutgers University</div>
        <div class="cv-item-description">
            <p>Provided individual and group tutoring for undergraduate mathematics courses</p>
        </div>
    </div>
</div>

## Skills & Technical Proficiencies

<div class="cv-section">
    <div class="cv-item">
        <div class="cv-item-title">Mathematical Software</div>
        <div class="cv-item-description">
            <p>MATLAB, Mathematica, Python (NumPy, SciPy, SymPy), R</p>
        </div>
    </div>

    <div class="cv-item">
        <div class="cv-item-title">Programming Languages</div>
        <div class="cv-item-description">
            <p>Python, C++, Java, LaTeX</p>
        </div>
    </div>

    <div class="cv-item">
        <div class="cv-item-title">Languages</div>
        <div class="cv-item-description">
            <p>English (Native), Mandarin Chinese (Conversational)</p>
        </div>
    </div>
</div>

## Professional Activities

<div class="cv-section">
    <div class="cv-item">
        <div class="cv-item-header">
            <span class="cv-item-title">Member, Mathematical Association of America</span>
            <span class="cv-item-date">2023-Present</span>
        </div>
    </div>

    <div class="cv-item">
        <div class="cv-item-header">
            <span class="cv-item-title">President, Mathematics Club</span>
            <span class="cv-item-date">2024-Present</span>
        </div>
        <div class="cv-item-subtitle">Rutgers University</div>
        <div class="cv-item-description">
            <p>Organized weekly seminars and social events for mathematics students</p>
        </div>
    </div>
</div>

## References

<div class="cv-section">
    <div class="cv-item">
        <div class="cv-item-description">
            <p>References available upon request. Please <a href="{{ '/contact/' | relative_url }}">contact me</a> for reference information.</p>
        </div>
    </div>
</div>

---

<div class="cv-note">
    <p><strong>Last Updated:</strong> {{ 'now' | date: "%B %Y" }}</p>
    <p>For the most current version of my CV, please download the PDF version above or <a href="{{ '/contact/' | relative_url }}">contact me</a> directly.</p>
</div>

<style>
.cv-download {
    text-align: center;
    margin-bottom: 3rem;
    padding: 1.5rem;
    background-color: #f8f9fa;
    border-radius: 8px;
}

.cv-download p {
    margin-bottom: 0;
}

.cv-note {
    background-color: #f8f9fa;
    padding: 1.5rem;
    border-radius: 8px;
    margin-top: 2rem;
    font-size: 0.9rem;
    color: #666;
}

.cv-note p {
    margin-bottom: 0.5rem;
}

.cv-note p:last-child {
    margin-bottom: 0;
}
</style>