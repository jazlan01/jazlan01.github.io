---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<div class="cv-contact-bar">
  <span>📧 <a href="mailto:{{ site.data.cv_basic.contact.email }}">{{ site.data.cv_basic.contact.email }}</a></span> • 
  <span>📍 {{ site.data.cv_basic.contact.location }}</span> • 
  <span>🎓 {{ site.data.cv_basic.contact.institution }}</span>
</div>

## 🎓 Education

<div class="cv-section">
{% for education in site.data.cv_education %}
  <div class="cv-item">
    <div class="cv-item-header">
      <h3>{{ education.degree }}</h3>
      <span class="cv-date">{{ education.period }}</span>
    </div>
    <p class="cv-institution">{{ education.institution }}</p>
    <p class="cv-details">
      <strong>Focus:</strong> {{ education.focus }}<br>
      <strong>Advisors:</strong> {{ education.advisors }}
    </p>
  </div>
{% endfor %}
</div>

## 🎯 Research Interests

<div class="research-interests">
{% for interest in site.data.cv_interests %}
  <div class="interest-tag">{{ interest }}</div>
{% endfor %}
</div>

## 🔬 Research Experience

<div class="cv-section">
{% for research in site.data.cv_research %}
  <div class="cv-item{% if research.type == 'highlight' %} highlight{% endif %}{% if research.type == 'special' %} special{% endif %}">
    <div class="cv-item-header">
      <h3>{{ research.position }}</h3>
      <span class="cv-date">{{ research.period }}</span>
    </div>
    <p class="cv-institution">{{ research.institution }}</p>
    <ul class="cv-achievements">
    {% for achievement in research.achievements %}
      <li>{{ achievement }}</li>
    {% endfor %}
    </ul>
  </div>
{% endfor %}
</div>

## 👨‍🏫 Teaching Experience

<div class="cv-section">
{% for teaching in site.data.cv_teaching %}
  <div class="cv-item{% if teaching.type == 'highlight' %} highlight{% endif %}{% if teaching.type == 'special' %} special{% endif %}">
    <div class="cv-item-header">
      <h3>{{ teaching.position }}</h3>
      <span class="cv-date">{{ teaching.period }}</span>
    </div>
    <p class="cv-institution">{{ teaching.institution }}</p>
    {% if teaching.courses %}
    <div class="teaching-courses">
      <h4>Courses:</h4>
      <ul class="cv-achievements">
      {% for course in teaching.courses %}
        <li><strong>{{ course }}</strong></li>
      {% endfor %}
      </ul>
    </div>
    {% endif %}
    {% if teaching.responsibilities %}
    <div class="teaching-responsibilities">
      <h4>Key Responsibilities:</h4>
      <ul class="cv-achievements">
      {% for responsibility in teaching.responsibilities %}
        <li>{{ responsibility }}</li>
      {% endfor %}
      </ul>
    </div>
    {% endif %}
    {% if teaching.details %}
    <ul class="cv-achievements">
      {% for detail in teaching.details %}
      <li>{{ detail }}</li>
      {% endfor %}
    </ul>
    {% endif %}
  </div>
{% endfor %}
</div>

## 🛠️ Technical Skills

<div class="skills-grid">
{% for skill in site.data.cv_skills %}
  <div class="skill-category">
    <h4>{{ skill.category }}</h4>
    <p>{{ skill.skills }}</p>
  </div>
{% endfor %}
</div>

<style>
.cv-contact-bar {
  text-align: center;
  padding: 1rem 0;
  margin-bottom: 2rem;
  font-size: 0.95rem;
  color: #666;
  background: #F8FBFF;
  border-radius: 8px;
  border: 1px solid #E8F4FF;
}

.cv-contact-bar a {
  color: #4A6FA5;
  text-decoration: none;
  transition: color 0.2s ease;
}

.cv-contact-bar a:hover {
  color: #2E5A87;
  text-decoration: underline;
}

.cv-section {
  margin-bottom: 2rem;
}

.cv-item {
  background: #fff;
  border: 1px solid #e9ecef;
  border-radius: 10px;
  padding: 1.5rem;
  margin-bottom: 1.5rem;
  transition: all 0.3s ease;
  box-shadow: 0 2px 4px rgba(0,0,0,0.05);
}

.cv-item:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(74, 111, 165, 0.15);
  border-color: #B8D4FF;
}

.cv-item.highlight {
  background: linear-gradient(135deg, #E8F4FF 0%, #F5F9FF 100%);
  border-color: #B8D4FF;
}

.cv-item.special {
  background: linear-gradient(135deg, #F0F6FF 0%, #F8FBFF 100%);
  border-color: #B8D4FF;
}

.cv-item-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.5rem;
}

.cv-item-header h3 {
  margin: 0;
  color: #333;
  font-size: 1.2rem;
  font-weight: 600;
}

.cv-date {
  color: #4A6FA5;
  font-weight: 600;
  font-size: 0.9rem;
  background: rgba(184, 212, 255, 0.3);
  padding: 0.25rem 0.75rem;
  border-radius: 15px;
  white-space: nowrap;
  border: 1px solid rgba(184, 212, 255, 0.5);
}

.cv-institution {
  color: #666;
  font-size: 1rem;
  font-weight: 500;
  margin: 0.5rem 0;
}

.cv-details {
  color: #555;
  font-size: 0.95rem;
  line-height: 1.5;
  margin: 0.75rem 0 0 0;
}

.cv-achievements {
  margin: 1rem 0 0 0;
  padding-left: 1.5rem;
}

.cv-achievements li {
  margin-bottom: 0.5rem;
  color: #555;
  line-height: 1.5;
}

.cv-achievements li strong {
  color: #333;
  font-weight: 600;
}

.teaching-courses, .teaching-responsibilities {
  margin-bottom: 1rem;
}

.teaching-courses h4, .teaching-responsibilities h4 {
  margin: 0 0 0.5rem 0;
  color: #4A6FA5;
  font-size: 0.95rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.teaching-courses .cv-achievements {
  margin-top: 0.5rem;
}

.teaching-responsibilities .cv-achievements {
  margin-top: 0.5rem;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1.5rem;
  margin: 1.5rem 0;
}

.skill-category {
  background: #F8FBFF;
  padding: 1.5rem;
  border-radius: 10px;
  border-left: 4px solid #B8D4FF;
  border: 1px solid #E8F4FF;
}

.skill-category h4 {
  margin: 0 0 0.75rem 0;
  color: #333;
  font-size: 1rem;
}

.skill-category p {
  margin: 0;
  color: #666;
  font-size: 0.95rem;
  line-height: 1.5;
}

.research-interests {
  display: flex;
  flex-wrap: wrap;
  gap: 0.75rem;
  margin: 1.5rem 0;
}

.interest-tag {
  background: linear-gradient(135deg, #E8F4FF 0%, #D6EAFF 100%);
  color: #4A6FA5;
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-size: 0.9rem;
  font-weight: 500;
  box-shadow: 0 2px 4px rgba(74, 111, 165, 0.15);
  transition: all 0.2s ease;
  border: 1px solid #C4DDFF;
}

.interest-tag:hover {
  transform: translateY(-1px);
  background: linear-gradient(135deg, #D6EAFF 0%, #C4DDFF 100%);
  box-shadow: 0 3px 6px rgba(74, 111, 165, 0.2);
}

@media (max-width: 768px) {
  .cv-contact-bar {
    padding: 0.75rem 0;
    font-size: 0.85rem;
  }
  
  .cv-item-header {
    flex-direction: column;
    align-items: flex-start;
  }
  
  .cv-date {
    margin-top: 0.5rem;
  }
  
  .skills-grid {
    grid-template-columns: 1fr;
  }
  
  .research-interests {
    justify-content: center;
  }
}
</style>
