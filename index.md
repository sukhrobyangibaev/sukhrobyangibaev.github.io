---
layout: default
---

{% assign all_posts = '' | split: '' %}
{% for post in site.posts %}
  {% unless post.categories contains 'class_materials' %}
    {% assign all_posts = all_posts | push: post %}
  {% endunless %}
{% endfor %}

{% assign all_items = all_posts | concat: site.tweets | sort: 'date' | reverse %}

<ul class="post-list">
  {% for item in all_items limit:10 %}
    {% if item.url contains "/tweets/" %}
      <!-- Tweet item -->
      <li class="tweet-item">
        <div class="tweet-date">{{ item.date | date: "%b %-d, %Y" }}</div>
        <div class="tweet-content">{{ item.content }}</div>
        {% if item.image %}
          <div class="tweet-media">
            <img src="{{ item.image }}" alt="{{ item.image_alt }}">
          </div>
        {% endif %}
        {% if item.video %}
          <div class="tweet-media">
            <video controls src="{{ item.video }}"></video>
          </div>
        {% endif %}
      </li>
    {% else %}
      <!-- Post item -->
      <li class="tweet-item">
        <div class="tweet-date">{{ item.date | date: "%b %-d, %Y" }}</div>
        <h3>
          <a class="post-link" href="{{ item.url | relative_url }}">
            {{ item.title | escape }}
          </a>
        </h3>
        {% if item.description %}
          <div class="tweet-content">{{ item.description }}</div>
        {% endif %}
        {% if item.image %}
          <div class="tweet-media">
            <img src="{{ item.image }}" alt="{{ item.image_alt }}">
          </div>
        {% endif %}
      </li>
    {% endif %}
  {% endfor %}
</ul>