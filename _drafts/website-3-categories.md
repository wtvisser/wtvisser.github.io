---
layout:     single
classes:    wide
title:      "How I created this website (3) - Categories"
categories: website
tags: 
  - skills

tagline: ""
header:
  overlay_image: /assets/images/headers/leaf_1280x325.png
image:
  path: assets/sleepdungeon/leaf_325x325_with_name.png
  width: 325
  height: 325  
---

https://emmatheeng.github.io/projects/blog_setup/blog-categories.html
https://github.com/emmatheeng/emmatheeng.github.io/blob/master/docs/projects/index.html

https://jekyllrb.com/docs/posts/#categories
https://jekyllrb.com/docs/collections/

https://blog.webjeda.com/jekyll-categories/#categories-count

# Needs
I want each project to have its own little overview page and description, and I want blog posts to be accessible through their category.

# Tags and Categories
There two ways of doing this:

1. Tags: Jekyll Tags are one or more attributes set for a given post. Tags can be added to Jekyll posts using the frontmatter keys tag or tags.
2. Categories: Jekyll Categories are similar to tags and can be set in frontmatter using keys category or categories. Other than tags however they work “more hierarchical” - if a post is in a directory other than _posts, every directory will be treated as another post category. Jekyll Categories are a way of structuring blog posts in a hierarchical way. Blog posts within one category are grouped together and relevant for one main project or goal.

# Implementation
To implement categories on my blog posts, and add overview pages for each category, I need to implement the following things:

* adding categories to the post itself and showing them on the post page
* adding the overview page per category that shows general information about the given category
