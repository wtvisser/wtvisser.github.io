---
layout:     single
classes:    wide
title:      "How I created this website (2) - Codespaces"
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

I decided to use [Github Codespaces](https://docs.github.com/en/codespaces/about-codespaces/what-are-codespaces) as my IDE. It is Visual Studio Code hosted in the browsers connected to a cloud-hosted VM that runs the *devcontainer* with the development environment. 

![Codespaces are cloud-hosted Github's devcontainers accessible from VS Code.](https://docs.github.com/assets/cb-68851/mw-1440/images/help/codespaces/codespaces-diagram.webp)
*Codespaces are cloud-hosted Github's devcontainers accessible from VS Code (image belongs to [Github Docs](https://docs.github.com/en/codespaces/about-codespaces/what-are-codespaces)).*

# Why Codespaces?
Using *devcontainers* is the modern approach. The benefits are obvious. No need to install anything locally, all dependencies are available, and git flow is integrated. I can access it from anywhere, on any device (although preferably a proper dev setup with multiple monitors).

It is also a good option to experience working with [devcontainers](https://containers.dev/overview) an as engineer. [Github's engineering team](https://github.blog/engineering/githubs-engineering-team-moved-codespaces/) has moved to using Codespaces a few years ago. DevContainers are definitely the way to go as they remove all the hustle with setting up development environments. It is Docker for developers. I am though a bit skeptical using Github Codespaces for professional development, but for a private venture this would be sufficient.

It comes with some drawbacks though. I can only use up to three Codespaces environments, for example if we want to work with multiple branches at the same time (e.g. for prototyping). I need internet, which means that working with Codespaces during travel may not always be possible. Integration with tools that Github does not natively support may be a challenge and require effort to configure or workarounds. It limits the possibility to customize the development environments.

# Setting up Codespaces
I used Codespaces to create this website (see [the blog series](#This-blog-series) how I did that). The setup was easy. 

<!-- See https://www.matthewcanderson.com/codespace-for-jekyll/ -->

## Create a Codespaces environment
I created the Codespaces environment from the Github repo using the Code menu and click **Create**.

![Creating a codespace from the Github repository.](/assets/images/posts/codespaces_create_environment.png){: .align-center}

## Add a devcontainer
Next, I added a devcontainer to the environments using the command palette. Click the *Codespaces* button in the bottom-left corner of the IDE and run the **Add Dev Container Configuration Files** option. I selected **New Configuration**.

![Create the devcontainer.](/assets/images/posts/codespaces_create_devcontainer.png){: .align-center}

I chose the **Jekyll devcontainer** as configuration and the default **bullseye** Debian OS. I didn't install any additional features.

![Choosing the Jekyll configuration for the container.](/assets/images/posts/codespaces_create_devcontainer_jekyll.png){: .align-center}

Next, I rebuild the container when Codespaces prompts it.

![Rebuild the container.](/assets/images/posts/codespaces_rebuild_devcontainer.png){: .align-center}

With the development environment available, I could create a new Jekyll website in Codespaces and add additional gems.

![Rebuild the container.](/assets/images/posts/codespaces_create_jekyll_website.png){: .align-center}

# Run as localhost
You can give the website a test by running it as localhost in Codespaces using `bundle exec jekyll serve`.

**Important:** I had to move the website files from */mywebsite/* to the repository root so that Github Pages could find it during build. I haven't found a way to configure the build to target a custom directory.

<p class="notice--info">
<strong>Important:</strong> I had to move the website files from */mywebsite/* to the repository root so that Github Pages could find it during build. I haven't found a way to configure the build to target a custom directory.
</p>

# This blog series
This blog is part of a larger series:

