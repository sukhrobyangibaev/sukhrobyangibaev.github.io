---
layout: page
title: Class Materials
permalink: /class_materials/
---
<style>
.category-section {
  margin-bottom: 20px;
}

.category-header {
  cursor: pointer;
  padding: 10px;
  background-color: #f0f0f0;
  border-radius: 4px;
  margin-bottom: 10px;
}

.category-header h2 {
  margin: 0;
  font-size: 1.5em;
}

.subcategory {
  margin-left: 20px;
  margin-bottom: 15px;
}

.subcategory-header {
  font-size: 1.2em;
  margin-bottom: 10px;
  color: #333;
}

.post-item {
  margin-left: 40px;
  margin-bottom: 8px;
}

.post-item a {
  text-decoration: none;
  color: #0366d6;
}

.post-item a:hover {
  text-decoration: underline;
}

.collapsed {
  display: none;
}
</style>

<div id="materials-container">
  <!-- English Section -->
  <div class="category-section">
    <div class="category-header" onclick="toggleSection('en-content')">
      <h2>Databases EN</h2>
    </div>
    <div id="en-content">
      <div class="subcategory">
        <div class="subcategory-header">Lectures</div>
        {% for post in site.categories.class_materials reversed %}
          {% if post.categories contains 'databases_en' and post.categories contains 'lecture' %}
            <div class="post-item">
              <a href="{{ post.url }}">{{ post.title }}</a>
            </div>
          {% endif %}
        {% endfor %}
      </div>
      
      <div class="subcategory">
        <div class="subcategory-header">Practice</div>
        {% for post in site.categories.class_materials reversed %}
          {% if post.categories contains 'databases_en' and post.categories contains 'practice' %}
            <div class="post-item">
              <a href="{{ post.url }}">{{ post.title }}</a>
            </div>
          {% endif %}
        {% endfor %}
      </div>
      
      <div class="subcategory">
        <div class="subcategory-header">Assignments</div>
        {% for post in site.categories.class_materials reversed %}
          {% if post.categories contains 'databases_en' and post.categories contains 'assignment' %}
            <div class="post-item">
              <a href="{{ post.url }}">{{ post.title }}</a>
            </div>
          {% endif %}
        {% endfor %}
      </div>
    </div>
  </div>

  <!-- Russian Section -->
  <div class="category-section">
    <div class="category-header" onclick="toggleSection('ru-content')">
      <h2>Databases RU</h2>
    </div>
    <div id="ru-content">
      <div class="subcategory">
        <div class="subcategory-header">Lectures</div>
        {% for post in site.categories.class_materials reversed %}
          {% if post.categories contains 'databases_ru' and post.categories contains 'lecture' %}
            <div class="post-item">
              <a href="{{ post.url }}">{{ post.title }}</a>
            </div>
          {% endif %}
        {% endfor %}
      </div>
      
      <div class="subcategory">
        <div class="subcategory-header">Practice</div>
        {% for post in site.categories.class_materials reversed %}
          {% if post.categories contains 'databases_ru' and post.categories contains 'practice' %}
            <div class="post-item">
              <a href="{{ post.url }}">{{ post.title }}</a>
            </div>
          {% endif %}
        {% endfor %}
      </div>
      
      <div class="subcategory">
        <div class="subcategory-header">Assignments</div>
        {% for post in site.categories.class_materials reversed %}
          {% if post.categories contains 'databases_ru' and post.categories contains 'assignment' %}
            <div class="post-item">
              <a href="{{ post.url }}">{{ post.title }}</a>
            </div>
          {% endif %}
        {% endfor %}
      </div>
    </div>
  </div>
</div>

<script>
function toggleSection(sectionId) {
  const content = document.getElementById(sectionId);
  content.classList.toggle('collapsed');
}

// Initialize all sections as expanded
document.addEventListener('DOMContentLoaded', function() {
  const sections = ['en-content', 'ru-content'];
  sections.forEach(section => {
    document.getElementById(section).classList.remove('collapsed');
  });
});
</script>