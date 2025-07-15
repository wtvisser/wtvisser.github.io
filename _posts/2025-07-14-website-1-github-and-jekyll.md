---
layout:     single
classes:    wide
title:      "How I created this website (1) - Jekyll and Github Pages"
category:   [Website]

tagline: ""
header:
  overlay_image: /assets/images/headers/leaf_1280x325.png
image:
  path: assets/sleepdungeon/leaf_325x325_with_name.png
  width: 325
  height: 325  
---
{% include post_category_and_date.html %}

I recently created this website to share my experience and thoughts on software engineering. 

I was looking for an easy way to create a website. I do not have much time at hands, but also enjoy coding and customizing. [Github Pages](https://pages.github.com/) is a popular way to host static websites. It seems to provide what I need, at least for the time being.

Github Pages works with Jekyll. You can [use Jekyll to create a GitHub Pages site](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll) from your own Github repository.

# Minima as the Jekyll theme
I like the Minimal Mistakes theme: https://mmistakes.github.io/minimal-mistakes/docs/installation/#theme-migration

I replaced the default theme in the `gemfile` with `gem "minimal-mistakes-jekyll"`, ran `bundle` to update the dependencies, and configured it as a remote theme (so that Github Actions can use it) by replacing the default theme in the `_config.yml` file by `remote_theme: mmistakes/minimal-mistakes@4.27.1`. Running `bundle update` install the theme, and we are good to go!

# Github Pages gem
Instead of the jekyll gem, I used the following dependencies: 
* I use this to setup Jekyll: https://github.com/github/pages-gem

in the gemfile, I replaced `gem "jekyll", "~> 4.4.1"` with:
```
source "https://rubygems.org"
gem "github-pages", group: :jekyll_plugins
gem "jekyll-include-cache", group: :jekyll_plugins
```

I ran `bundle` to update the dependencies.

## Creating an author profile
To create  short bio of myself on the website I follow the [mmistakes instructions on how to create an author profile](https://mmistakes.github.io/minimal-mistakes/docs/layouts/#author-profile).

I decided to configure it in the *_config.yaml*.

![Configure the author profile in _config.yaml.](/assets/images/posts/website_site_author1.png){: .align-center}

![Configure the author profile in _config.yaml.](/assets/images/posts/website_site_author2.png){: .align-center}

It looks like this with the Minimal Mistakes theme.

![The author profile with mmistakes.](/assets/images/posts/website_site_author3.png){: .align-center}

## Adding a footer
You can also configure the footer.

![Configure the footer in _config.yaml.](/assets/images/posts/website_footer1.png){: .align-center}

Which then looks like so.

![The footer with mmistakes.](/assets/images/posts/website_footer2.png){: .align-center}

## Creating a feed
Jekyll supports generating an *atom feed* from the blog posts. This is available as a [gem](https://rubygems.org/gems/jekyll-feed/versions/0.17.0?locale=en). Simply add it to the **gemfile**.

![Configure the feed in _config.yaml.](/assets/images/posts/website_feed.png){: .align-center}


## Adding additional pages
The Jekyll and Minimal Mistakes theme provide more functionality than just blog pages. I store my non-blog pages in a separate */_pages/* folder.

To include these in the build, I configured the *_config.yml* accordingly.

![Configure the /_pages/ folder in _config.yaml.](/assets/images/posts/website_pages1.png){: .align-center}

![Configure the /_pages/ folder in _config.yaml.](/assets/images/posts/website_pages2.png){: .align-center}

# This blog series
This blog is part of a larger series:

