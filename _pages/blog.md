---
layout: home # this enables the Recent Posts section
permalink: /blog/
title: Blog
author_profile: true
---
Experience is best internalized by writing it down. Follow my thoughts in these blog posts.

See all posts by category:

<ul class="taxonomy__index">
  {% assign postsByCategory = site.posts | where_exp: "item", "item.hidden != true" | group_by_exp: 'post', 'post.category' %}
  {% for category in postsByCategory %}
    <li>
      <a href="#{{ category.name }}">
        <strong>{{ category.name }}</strong> <span class="taxonomy__count">{{ category.items | size }}</span>
      </a>
    </li>
  {% endfor %}
</ul>

<!-- 
{% assign entries_layout = page.entries_layout | default: 'list' %}
{% assign postsByCategory = site.posts | where_exp: "item", "item.hidden != true" | group_by_exp: 'post', 'post.category' %}
{% for year in postsByCategory %}
  <section id="{{ category.name }}" class="taxonomy__section">
    <h2 class="archive__subtitle">{{ year.name }}</h2>
    <div class="entries-{{ entries_layout }}">
      {% for post in category.items %}
        {% include archive-single.html type=entries_layout %}
      {% endfor %}
    </div>
    <a href="#page-title" class="back-to-top">{{ site.data.ui-text[site.locale].back_to_top | default: 'Back to Top' }} &uarr;</a>
  </section>
{% endfor %} 
-->