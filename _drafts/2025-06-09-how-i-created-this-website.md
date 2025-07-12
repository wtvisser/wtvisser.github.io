---
layout: single
title:  "How I created this website"
date:   2025-06-09 17:24:42 +0000
# categories: website
---

# Codespaces
I decided to use Github Codespaces as my IDE. Setup was easy. See * Setup in Codespaces https://www.matthewcanderson.com/codespace-for-jekyll/

# Github-pages gem
Instead of the jekyll gem, I used the following dependencies: 
* I use this to setup Jekyll: https://github.com/github/pages-gem

in the gemfile, I replaced `gem "jekyll", "~> 4.4.1"` with:
```
source "https://rubygems.org"
gem "github-pages", group: :jekyll_plugins
gem "jekyll-include-cache", group: :jekyll_plugins
```

I ran `bundle` to update the dependencies.

# Minimal Mistakes theme
I like the Minimal Mistakes theme: https://mmistakes.github.io/minimal-mistakes/docs/installation/#theme-migration

I replaced the default theme in the `gemfile` with `gem "minimal-mistakes-jekyll"`, ran `bundle` to update the dependencies, and configured it as a remote theme (so that Github Actions can use it) by replacing the default theme in the `_config.yml` file by `remote_theme: mmistakes/minimal-mistakes@4.27.1`. Running `bundle update` install the theme, and we are good to go!

# Run as localhost
You can give the website a test by running it as localhost in Codespaces using `bundle exec jekyll serve`.

# Headers

# Mindmap

# Notice blocks
https://mmistakes.github.io/minimal-mistakes/post%20formats/post-notice/

# Images
Creative Commons
 
https://mister-chad.com/graphic+design+resources/free+images+for+commercial+use

# OpenGraph

# Link Previews
https://github.com/ysk24ok/jekyll-linkpreview

# Google Analytics


# Gems - Raindrop

# Books
https://help.goodreads.com/s/article/How-do-I-add-a-widget-to-my-blog-1553870933491
https://www.goodreads.com/user/edit?ref=nav_profile_settings
