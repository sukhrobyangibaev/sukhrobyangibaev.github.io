---
layout: default
---

<div class="tweets-container">
  <h1>Recent Thoughts</h1>
  
  {% for tweet in site.tweets reversed limit:10 %}
  <div class="tweet-item">
    <div class="tweet-date">{{ tweet.date | date: "%b %-d, %Y" }}</div>
    <div class="tweet-content">{{ tweet.content }}</div>
    {% if tweet.image %}
      <div class="tweet-media">
        <img src="{{ tweet.image }}" alt="{{ tweet.image_alt }}">
      </div>
    {% endif %}
    {% if tweet.video %}
      <div class="tweet-media">
        <video controls src="{{ tweet.video }}"></video>
      </div>
    {% endif %}
  </div>
  {% endfor %}
  
  {% if site.tweets.size > 10 %}
    <div class="tweets-archive-link">
      <a href="/tweets/">View all tweets</a>
    </div>
  {% endif %}
</div>
