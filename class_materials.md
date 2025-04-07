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

.language-header {
  cursor: pointer;
  padding: 8px;
  background-color: #e6e6e6;
  border-radius: 4px;
  margin-bottom: 8px;
  margin-left: 20px;
}

.language-header h3 {
  margin: 0;
  font-size: 1.3em;
}

.subcategory {
  margin-left: 40px;
  margin-bottom: 15px;
}

.subcategory-header {
  font-size: 1.2em;
  margin-bottom: 10px;
  color: #333;
  cursor: pointer;
  padding: 5px;
  background-color: #f8f8f8;
  border-radius: 3px;
}

.post-item {
  margin-left: 60px;
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
  <!-- Databases Section -->
  <div class="category-section">
    <div class="category-header" onclick="toggleSection('databases-content')">
      <h2>Databases</h2>
    </div>
    <div id="databases-content" class="collapsed">
      <!-- English Section -->
      <div class="category-section">
        <div class="language-header" onclick="toggleSection('en-content')">
          <h3>EN</h3>
        </div>
        <div id="en-content" class="collapsed">
          <div class="subcategory">
            <div class="subcategory-header" onclick="toggleSection('en-lectures')">Lectures</div>
            <div id="en-lectures" class="collapsed">
              {% for post in site.categories.class_materials reversed %}
                {% if post.categories contains 'databases_en' and post.categories contains 'lecture' %}
                  <div class="post-item">
                    <a href="{{ post.url }}">{{ post.title }}</a>
                  </div>
                {% endif %}
              {% endfor %}
            </div>
          </div>
          
          <div class="subcategory">
            <div class="subcategory-header" onclick="toggleSection('en-practice')">Practice</div>
            <div id="en-practice" class="collapsed">
              {% for post in site.categories.class_materials reversed %}
                {% if post.categories contains 'databases_en' and post.categories contains 'practice' %}
                  <div class="post-item">
                    <a href="{{ post.url }}">{{ post.title }}</a>
                  </div>
                {% endif %}
              {% endfor %}
            </div>
          </div>
          
          <div class="subcategory">
            <div class="subcategory-header" onclick="toggleSection('en-assignments')">Assignments</div>
            <div id="en-assignments" class="collapsed">
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
      </div>

      <!-- Russian Section -->
      <div class="category-section">
        <div class="language-header" onclick="toggleSection('ru-content')">
          <h3>RU</h3>
        </div>
        <div id="ru-content" class="collapsed">
          <div class="subcategory">
            <div class="subcategory-header" onclick="toggleSection('ru-lectures')">Lectures</div>
            <div id="ru-lectures" class="collapsed">
              {% for post in site.categories.class_materials reversed %}
                {% if post.categories contains 'databases_ru' and post.categories contains 'lecture' %}
                  <div class="post-item">
                    <a href="{{ post.url }}">{{ post.title }}</a>
                  </div>
                {% endif %}
              {% endfor %}
            </div>
          </div>
          
          <div class="subcategory">
            <div class="subcategory-header" onclick="toggleSection('ru-practice')">Practice</div>
            <div id="ru-practice" class="collapsed">
              {% for post in site.categories.class_materials reversed %}
                {% if post.categories contains 'databases_ru' and post.categories contains 'practice' %}
                  <div class="post-item">
                    <a href="{{ post.url }}">{{ post.title }}</a>
                  </div>
                {% endif %}
              {% endfor %}
            </div>
          </div>
          
          <div class="subcategory">
            <div class="subcategory-header" onclick="toggleSection('ru-assignments')">Assignments</div>
            <div id="ru-assignments" class="collapsed">
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
    </div>
  </div>
</div>

{% include chat_component.html url="https://astounding-treacle-ae7505.netlify.app/.netlify/functions/lb_ai_girlfriend" %}

<script>
function toggleSection(sectionId) {
  const content = document.getElementById(sectionId);
  content.classList.toggle('collapsed');
}
</script>