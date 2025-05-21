---
layout: page
title: Archive
permalink: /tweets/
---

<div class="tweets-archive">
  {% for tweet in site.tweets reversed %}
  <div class="tweet-item">
    <div class="tweet-date">{{ tweet.date | date: "%b %-d, %Y" }}</div>
    <div class="tweet-content">{{ tweet.content }}</div>
    {% if tweet.image %}
      <div class="tweet-media">
        <img src="{{ tweet.image }}" alt="{{ tweet.image_alt }}">
      </div>
    {% endif %}
  </div>
  {% endfor %}
</div>