---
permalink: /news/
title: "News"
author_profile: true
breadcrumbs: false
---

{% assign news_by_year = site.data.news | group_by_exp: "item", "item.date | date: '%Y'" | sort: "name" | reverse %}

<div class="news-container">
{% for year_group in news_by_year %}
  <h2 class="news-year">{{ year_group.name }}</h2>
  
  {% assign sorted_news = year_group.items | sort: "date" | reverse %}
  {% for news_item in sorted_news %}
    <div class="news-item">
      <div class="news-date">
        <span class="month">{{ news_item.date | date: "%b" }}</span>
        <span class="day">{{ news_item.date | date: "%d" }}</span>
      </div>
      <div class="news-content">
        <h3 class="news-title">{{ news_item.title }}</h3>
        <p class="news-description">{{ news_item.description }}</p>
        {% if news_item.category %}
          <span class="news-category news-category--{{ news_item.category }}">{{ news_item.category | capitalize }}</span>
        {% endif %}
      </div>
    </div>
  {% endfor %}
{% endfor %}
</div>

<style>
.news-container {
  max-width: 800px;
}

.news-year {
  color: #333;
  border-bottom: 2px solid #e0e0e0;
  padding-bottom: 0.5rem;
  margin: 2rem 0 1rem 0;
  font-size: 1.5rem;
}

.news-item {
  display: flex;
  margin-bottom: 1.5rem;
  padding: 1rem;
  border-left: 3px solid #f0f0f0;
  transition: border-color 0.3s ease;
}

.news-item:hover {
  border-left-color: #B8D4FF;
}

.news-date {
  flex-shrink: 0;
  width: 80px;
  text-align: center;
  margin-right: 1.5rem;
  background: #f8f9fa;
  border-radius: 8px;
  padding: 0.5rem;
  height: fit-content;
}

.news-date .month {
  display: block;
  font-size: 0.9rem;
  font-weight: bold;
  color: #666;
  text-transform: uppercase;
}

.news-date .day {
  display: block;
  font-size: 1.4rem;
  font-weight: bold;
  color: #333;
}

.news-content {
  flex: 1;
}

.news-title {
  margin: 0 0 0.5rem 0;
  color: #333;
  font-size: 1.2rem;
  font-weight: 600;
}

.news-description {
  margin: 0 0 0.75rem 0;
  color: #555;
  line-height: 1.5;
}

.news-category {
  display: inline-block;
  padding: 0.25rem 0.75rem;
  font-size: 0.8rem;
  font-weight: 500;
  border-radius: 15px;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.news-category--academic {
  background-color: #e3f2fd;
  color: #1976d2;
}

.news-category--research {
  background-color: #f3e5f5;
  color: #7b1fa2;
}

.news-category--teaching {
  background-color: #e8f5e8;
  color: #388e3c;
}

.news-category--award {
  background-color: #fff3e0;
  color: #f57c00;
}

.news-category--conference {
  background-color: #fce4ec;
  color: #c2185b;
}

@media (max-width: 600px) {
  .news-item {
    flex-direction: column;
  }
  
  .news-date {
    width: auto;
    margin-right: 0;
    margin-bottom: 0.75rem;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 0.5rem 1rem;
  }
  
  .news-date .month {
    margin-right: 0.5rem;
  }
  
  .news-date .day {
    font-size: 1.2rem;
  }
}
</style> 