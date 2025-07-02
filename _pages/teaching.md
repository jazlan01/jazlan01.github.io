---
permalink: /teaching/
title: "Teaching Experience"
author_profile: true
---

<div class="teaching-header">
  <h1>👨‍🏫 Teaching Experience</h1>
  <p class="teaching-subtitle">Passionate about education and helping students learn computer science fundamentals</p>
</div>

## 🎯 Current Positions

<div class="teaching-section">
{% for position in site.data.teaching.current_positions %}
  <div class="teaching-card current">
    <div class="teaching-card-header">
      <h3>{{ position.role }}</h3>
      <span class="teaching-period">{{ position.period }}</span>
    </div>
    <div class="course-info">
      <div class="course-details">
        <span class="course-code">{{ position.course_code }}</span>
        <span class="course-name">{{ position.course_name }}</span>
      </div>
      <p class="institution">{{ position.institution }}</p>
      <span class="level-badge">{{ position.level }}</span>
    </div>
  </div>
{% endfor %}
</div>

## 🏗️ Course Design & Development

<div class="teaching-section">
{% for course in site.data.teaching.course_design %}
  <div class="teaching-card special">
    <div class="teaching-card-header">
      <h3>{{ course.role }}</h3>
      <span class="teaching-period">{{ course.period }}</span>
    </div>
    <div class="course-info">
      <div class="course-details">
        <span class="course-code">{{ course.course_code }}</span>
        <span class="course-name">{{ course.course_name }}</span>
      </div>
      <p class="institution">{{ course.institution }}</p>
      {% if course.collaborator %}
        <p class="collaborator">
          Collaborated with <a href="{{ course.collaborator_link }}" target="_blank">{{ course.collaborator }}</a>
        </p>
      {% endif %}
      {% if course.description %}
        <p class="course-description">{{ course.description }}</p>
      {% endif %}
    </div>
  </div>
{% endfor %}
</div>

## 📚 Teaching Assistant Roles

<div class="teaching-section">
  <div class="ta-grid">
  {% for position in site.data.teaching.past_positions %}
    <div class="ta-card">
      <div class="ta-course-header">
        <span class="course-code">{{ position.course_code }}</span>
        <span class="course-name">{{ position.course_name }}</span>
      </div>
      <p class="institution">{{ position.institution }}</p>
      <div class="periods">
        {% for period in position.periods %}
          <span class="period-tag">{{ period }}</span>
        {% endfor %}
      </div>
    </div>
  {% endfor %}
  </div>
</div>

## 🎓 Teaching Philosophy

<div class="philosophy-section">
  <div class="philosophy-card">
    <h3>🌟 My Approach to Teaching</h3>
    <p>I believe in making complex computer science concepts accessible and engaging. My teaching philosophy centers on:</p>
    <ul class="philosophy-list">
      <li><strong>Hands-on Learning:</strong> Practical exercises and real-world applications</li>
      <li><strong>Student-Centered Approach:</strong> Adapting to different learning styles and paces</li>
      <li><strong>Collaborative Environment:</strong> Encouraging peer learning and discussion</li>
      <li><strong>Problem-Solving Focus:</strong> Building critical thinking skills beyond memorization</li>
    </ul>
  </div>
</div>

<style>
.teaching-header {
  text-align: center;
  padding: 2rem 0;
  margin-bottom: 2rem;
  background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
  border-radius: 15px;
  border: 1px solid #dee2e6;
}

.teaching-header h1 {
  font-size: 2.5rem;
  margin: 0 0 0.5rem 0;
  color: #212529;
  font-weight: 700;
}

.teaching-subtitle {
  font-size: 1.1rem;
  color: #6c757d;
  margin: 0;
  font-weight: 500;
}

.teaching-section {
  margin-bottom: 3rem;
}

.teaching-card {
  background: #fff;
  border: 1px solid #e9ecef;
  border-radius: 12px;
  padding: 2rem;
  margin-bottom: 1.5rem;
  transition: all 0.3s ease;
  box-shadow: 0 2px 4px rgba(0,0,0,0.05);
}

.teaching-card:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 16px rgba(0,0,0,0.1);
  border-color: #007acc;
}

.teaching-card.current {
  background: linear-gradient(135deg, #e3f2fd 0%, #f8f9fa 100%);
  border-color: #007acc;
  border-width: 2px;
}

.teaching-card.special {
  background: linear-gradient(135deg, #f3e5f5 0%, #f8f9fa 100%);
  border-color: #7b1fa2;
  border-width: 2px;
}

.teaching-card-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 1rem;
}

.teaching-card-header h3 {
  margin: 0;
  color: #333;
  font-size: 1.3rem;
  font-weight: 600;
}

.teaching-period {
  color: #007acc;
  font-weight: 600;
  font-size: 0.9rem;
  background: rgba(0, 122, 204, 0.1);
  padding: 0.3rem 0.8rem;
  border-radius: 15px;
  white-space: nowrap;
}

.course-details {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 0.5rem;
}

.course-code {
  font-weight: 700;
  color: #333;
  font-size: 1rem;
  background: #f8f9fa;
  padding: 0.3rem 0.8rem;
  border-radius: 6px;
  border: 1px solid #dee2e6;
}

.course-name {
  color: #555;
  font-weight: 500;
  font-size: 1.1rem;
}

.institution {
  color: #666;
  font-size: 0.95rem;
  margin: 0.5rem 0;
  font-style: italic;
}

.level-badge {
  background: linear-gradient(135deg, #28a745 0%, #20c997 100%);
  color: white;
  padding: 0.3rem 0.8rem;
  border-radius: 12px;
  font-size: 0.8rem;
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.collaborator {
  color: #555;
  font-size: 0.9rem;
  margin: 0.5rem 0;
}

.collaborator a {
  color: #007acc;
  text-decoration: none;
  font-weight: 500;
}

.collaborator a:hover {
  text-decoration: underline;
}

.course-description {
  color: #555;
  font-size: 0.95rem;
  line-height: 1.5;
  margin: 0.75rem 0 0 0;
}

.ta-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem;
}

.ta-card {
  background: #fff;
  border: 1px solid #e9ecef;
  border-radius: 10px;
  padding: 1.5rem;
  transition: all 0.3s ease;
  box-shadow: 0 2px 4px rgba(0,0,0,0.05);
}

.ta-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  border-color: #007acc;
}

.ta-course-header {
  margin-bottom: 1rem;
}

.ta-card .course-code {
  display: block;
  margin-bottom: 0.5rem;
  width: fit-content;
}

.ta-card .course-name {
  display: block;
  font-size: 1rem;
  margin-bottom: 0.5rem;
}

.periods {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-top: 1rem;
}

.period-tag {
  background: #f8f9fa;
  color: #495057;
  padding: 0.25rem 0.6rem;
  border-radius: 12px;
  font-size: 0.8rem;
  font-weight: 500;
  border: 1px solid #dee2e6;
}

.philosophy-section {
  margin-top: 3rem;
}

.philosophy-card {
  background: linear-gradient(135deg, #fff3cd 0%, #f8f9fa 100%);
  border: 1px solid #ffeaa7;
  border-radius: 12px;
  padding: 2rem;
}

.philosophy-card h3 {
  margin: 0 0 1rem 0;
  color: #333;
  font-size: 1.2rem;
}

.philosophy-list {
  margin: 1rem 0 0 0;
  padding-left: 1.5rem;
}

.philosophy-list li {
  margin-bottom: 0.75rem;
  color: #555;
  line-height: 1.5;
}

.philosophy-list strong {
  color: #333;
}

@media (max-width: 768px) {
  .teaching-header h1 {
    font-size: 2rem;
  }
  
  .teaching-card-header {
    flex-direction: column;
    align-items: flex-start;
  }
  
  .teaching-period {
    margin-top: 0.5rem;
  }
  
  .course-details {
    flex-direction: column;
    align-items: flex-start;
    gap: 0.5rem;
  }
  
  .ta-grid {
    grid-template-columns: 1fr;
  }
}
</style> 