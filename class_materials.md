---
layout: page
title: Class Materials
permalink: /class_materials/
---

<div style="margin-bottom: 20px;">
  <select id="languageFilter" onchange="filterPosts()">
    <option value="all">All Languages</option>
    <option value="databases_en">English</option>
    <option value="databases_ru">Russian</option>
  </select>

  <select id="typeFilter" onchange="filterPosts()">
    <option value="all">All Types</option>
    <option value="lecture">Lecture</option>
    <option value="practice">Practice</option>
    <option value="assignment">Assignment</option>
  </select>
</div>

<div id="posts-container">
  {% for post in site.categories.class_materials reversed %}
    <article class="post-item" 
      data-language="{% if post.categories contains 'databases_en' %}databases_en{% elsif post.categories contains 'databases_ru' %}databases_ru{% endif %}"
      data-type="{% if post.categories contains 'lecture' %}lecture{% elsif post.categories contains 'practice' %}practice{% elsif post.categories contains 'assignment' %}assignment{% endif %}">
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    </article>
  {% endfor %}
</div>

<script>
function filterPosts() {
  const languageFilter = document.getElementById('languageFilter').value;
  const typeFilter = document.getElementById('typeFilter').value;
  const posts = document.getElementsByClassName('post-item');

  for (let post of posts) {
    const language = post.getAttribute('data-language');
    const type = post.getAttribute('data-type');
    
    const languageMatch = languageFilter === 'all' || language === languageFilter;
    const typeMatch = typeFilter === 'all' || type === typeFilter;
    
    post.style.display = languageMatch && typeMatch ? 'block' : 'none';
  }
}
</script>