---
permalink: /
title: "About"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<div class="hero-section">
  <h1 class="hero-title">👋 Hi, I'm Jazlan</h1>
  <p class="hero-subtitle">PhD Student in Privacy and Systems</p>
</div>

I am a first-year PhD student in **Computer Science** at the [University of California, Davis](https://www.ucdavis.edu/), where I work on cutting-edge **anti-tracking frameworks** and **privacy-preserving networks**. My research sits at the intersection of network security, privacy, and systems design.

I'm advised by [Prof. Zubair Shafiq](https://web.cs.ucdavis.edu/~zubair/) and [Prof. Alexander Gamero-Garrido](https://www.gamero-garrido.com).

### 🎓 **Background**
Prior to UC Davis, I completed my undergraduate studies at [Lahore University of Management Sciences (LUMS)](https://lums.edu.pk/), where I worked on systems research under the guidance of [Prof. Zafar Qazi](https://web.lums.edu.pk/~zafar/) and [Prof. Ihsan Qazi](https://www.ihsanqazi.com). My undergraduate research focused on building systems to improve edge latency in the 5G control plane.

## Recent News
{% assign recent_news = site.data.news | sort: "date" | reverse | limit: 4 %}
<div class="recent-news">
{% for news_item in recent_news %}
  <div class="news-item-compact">
    <div class="news-date-compact">{{ news_item.date | date: "%b %Y" }}</div>
    <div class="news-content-compact">
      <strong>{{ news_item.title }}</strong>
      <p>{{ news_item.description }}</p>
    </div>
  </div>
{% endfor %}
  <div class="news-more">
    <a href="/news/" class="btn">View All News →</a>
  </div>
</div>



## 🏎️ **Beyond Research**

When I'm not debugging network protocols or analyzing privacy frameworks, you'll find me:

- **🏁 Formula 1 Enthusiast** - Weekends are for race analysis (don't try reaching me during race hours!)
- **📱 Tech Explorer** - Following the latest developments in mobile and server technologies
- **🌐 Systems Tinkerer** - Always curious about how complex systems work under the hood

<style>
.hero-section {
  text-align: center;
  margin: 2rem 0 3rem 0;
  padding: 2rem 0;
  background: linear-gradient(135deg, #F8FBFF 0%, #F0F6FF 100%);
  border-radius: 15px;
  border: 1px solid #E0EFFF;
}

.hero-title {
  font-size: 2.2rem;
  margin: 0 0 0.5rem 0;
  color: #212529;
  font-weight: 700;
}

.hero-subtitle {
  font-size: 1.1rem;
  color: #6c757d;
  margin: 0;
  font-weight: 500;
}



.recent-news {
  margin: 1.5rem 0 2rem 0;
}

.news-item-compact {
  display: flex;
  align-items: flex-start;
  margin-bottom: 1rem;
  padding-bottom: 1rem;
}

.news-item-compact:last-of-type {
  margin-bottom: 0;
  padding-bottom: 0;
}

.news-date-compact {
  flex-shrink: 0;
  width: 80px;
  font-size: 0.85rem;
  color: #666;
  font-weight: 500;
  margin-right: 1rem;
  margin-top: 0.2rem;
}

.news-content-compact {
  flex: 1;
}

.news-content-compact strong {
  color: #333;
  font-size: 1rem;
  line-height: 1.4;
}

.news-content-compact p {
  margin: 0.3rem 0 0 0;
  color: #555;
  font-size: 0.9rem;
  line-height: 1.4;
}

.news-more {
  text-align: center;
  margin-top: 1.5rem;
  padding-top: 1rem;
  border-top: 1px solid #f0f0f0;
}

.news-more .btn {
  display: inline-block;
  color: #666;
  text-decoration: none;
  font-size: 0.85rem;
  font-weight: 400;
  transition: color 0.3s ease;
}

.news-more .btn:hover {
  color: #4A6FA5;
  text-decoration: underline;
}

@media (max-width: 768px) {
  .hero-title {
    font-size: 1.8rem;
  }
  
  .news-item-compact {
    flex-direction: column;
  }
  
  .news-date-compact {
    width: auto;
    margin-right: 0;
    margin-bottom: 0.5rem;
    font-weight: 600;
  }
  

}
</style>