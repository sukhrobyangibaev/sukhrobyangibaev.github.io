---
layout: default
pagination:
  enabled: true
---

<ul class="post-list">
  {% for item in paginator.docs %}
    {% if item.categories contains 'class_materials' %}{% continue %}{% endif %}
    {% if item.url contains "/tweets/" %}
      <!-- Tweet item -->
      <li class="tweet-item">
        <div class="tweet-date">{{ item.date | date: "%b %-d, %Y" }}</div>
        <div class="tweet-content">{{ item.content }}</div>
        {% if item.audio %}
          <div class="tweet-media">
            <audio controls src="{{ item.audio }}"></audio>
          </div>
        {% endif %}
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

{% if paginator.total_pages > 1 %}
<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path | relative_url }}" class="previous">Previous</a>
  {% else %}
    <span class="previous">Previous</span>
  {% endif %}

  <span class="page_number ">Page: {{ paginator.page }} of {{ paginator.total_pages }}</span>

  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path | relative_url }}" class="next">Next</a>
  {% else %}
    <span class="next">Next</span>
  {% endif %}
</div>
{% endif %}