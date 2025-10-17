---
layout: default
title: About
---

<div class="intro-section">
    <div class="intro-content">
        <!-- Profile image placeholder - Steven can add his photo later -->
        <!-- <img src="{{ '/assets/images/profile.jpg' | relative_url }}" alt="Steven T.C. Tung" class="profile-image"> -->

        <h1>Steven T.C. Tung</h1>
        <p class="page-subtitle">Mathematics Undergraduate | Rutgers University</p>

        <div class="intro-text">
            <p>Welcome! I'm a senior mathematics major at Rutgers University with a focus on Partial Differential Equations (PDEs). I'm currently applying for PhD programs in mathematics and actively engaged in research exploring the theoretical and applied aspects of mathematical analysis.</p>

            <p>My academic journey centers around understanding the elegant structures within mathematical analysis, particularly in differential equations and their applications. I'm passionate about both the theoretical foundations and computational aspects of mathematics.</p>

            <p>This website serves as a repository for my academic work, research endeavors, and mathematical notes. Feel free to explore my research projects, publications, and the collection of mathematical notes I've compiled throughout my studies.</p>
        </div>
    </div>
</div>

<div class="recent-updates">
    <h2>Recent Updates</h2>
    <div class="updates-list">
        <!-- This section will be manually updated by Steven -->
        <div class="update-item">
            <span class="update-date">October 2024</span>
            <span class="update-content">Applying for PhD programs in Mathematics</span>
        </div>
        <div class="update-item">
            <span class="update-date">September 2024</span>
            <span class="update-content">Senior year at Rutgers University begins</span>
        </div>
    </div>
</div>

<style>
.recent-updates {
    margin-top: 4rem;
    max-width: 600px;
    margin-left: auto;
    margin-right: auto;
}

.recent-updates h2 {
    text-align: center;
    margin-bottom: 2rem;
    font-size: 1.5rem;
}

.updates-list {
    background-color: #f8f9fa;
    border-radius: 8px;
    padding: 2rem;
}

.update-item {
    display: flex;
    gap: 2rem;
    margin-bottom: 1rem;
    padding-bottom: 1rem;
    border-bottom: 1px solid #e9ecef;
}

.update-item:last-child {
    margin-bottom: 0;
    padding-bottom: 0;
    border-bottom: none;
}

.update-date {
    font-weight: 600;
    color: #34495e;
    min-width: 120px;
    font-size: 0.9rem;
}

.update-content {
    color: #555;
}

@media (max-width: 600px) {
    .update-item {
        flex-direction: column;
        gap: 0.25rem;
    }

    .update-date {
        min-width: auto;
    }
}
</style>