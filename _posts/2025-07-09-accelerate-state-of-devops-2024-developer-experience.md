---
layout:     single
title:      "Accelerate State of DevOps: Developer Experience"
categories: [Developer Experience]

# classes:    wide      # wide doesn't work with right-side TOC
toc: true
toc_icon: "cog"
toc_sticky: true

tagline: "User-centricity can improve software development"
header:
  overlay_image: /assets/images/headers/leaf_1280x325.png
image:
    path: assets/images/opengraph/leaf_325x325_with_name.png
    width: 325
    height: 325  
---
{% include post_category_and_date.html %}

I recently re-read the [2024 DORA Report](https://dora.dev/research/2024/dora-report/). Here are my thoughts about what the report has to say about **Developer Experience**. For more on the DORA Report, see my [other posts in this series](#post-series).

# Developer Experience
## Provide direction to obtain drive

Guess what, Software Engineers are human too. `(/sarcasm)` The report mentioned:

> A recent survey showed that 93% of workers reported that it’s important to have a job where they feel the work they do is meaningful.

No surprise, of course. We are motivated and excel to new heights if we see meaning in our work, for example if we can change people or society for the better - however small that may be. 

This means that leaders must provide a clear sense of direction.

> Instead of shipping arbitrary features and guessing whether users might use them, developers can rely on user feedback to help them prioritize what to build.

Fast feedback is important. Product management and leadership should enable this. This is only possible if we have short feedback cycles, which in turn means we must automate and streamline our software delivery. The classic DevOps approach.

## Foster a culture of documentation

The DORA authors share an interesting position about documentation. 

> The Agile manifesto advocates for "working software over comprehensive documentation". We continue to find, however, that quality  documentation is a key component of working software.

This aligns with my thoughts as an architect. Working software is, of course, our primary deliverable, and so rightly should be prioritized. However, we don't just write software and deliver once. We have to maintain it, extend it, deploy elsewhere. The team may change, and stakeholders need to be informed regularly. All this requires knowledge to be available about the software and our ways of creating it. Not just in our minds, but more importantly written down somewhere. 

We should, however, document only that what is important. Technical decisions (using ADRs), architectural aspects, key use cases and requirements, guides and guidelines, etc. We need a healthy documentation culture. It should be part of our development best practices, for example as part of the *Definition of Done*. 

We should foster a healthy culture of documentation in our teams by following the practices the DORA authors identified to create quality documentation:

> * Documenting critical use cases.
> * Taking training in technical writing.
> * Defining ownership and processes to update the documentation.
> * Distributing documentation work within the team.
> * Maintaining documentation as part of the software development lifecycle.
> * Deleting out-of-date or redundant documentation.
> * Recognizing documentation work in performance reviews and promotions.

Documentation in itself has some quality attributes:

> Measure of quality documentation includes attributes like findability and reliability of the documentation.

{% capture idea %}
<span style="vertical-align: middle"><i class="fa-solid fa-lightbulb fa-2x" style="color:#FFD700;" aria-hidden="true"></i>&emsp;I may write a post on how these quality attributes for documentation could be best achieved.</span>
{% endcapture %}
<div class="notice">{{ idea | markdownify }}</div>

We have to be careful not to misuse or abuse documentation, i.e. use it for the wrong purposes:

> Problematic documentation includes documentation that is created only for bureaucratic purposes, or to paper over mistrust between management and employees. An unhealthy documentation culture can also include writing documentation, but not maintaining or consolidating the documentation.

The DORA report highlights that documentation can also help provide user-centricity to the development team:

> The combination of good docs and a user-centered approach to software development is a powerful one. [...] Documentation helps propagate user signals and feedback across the team and into the product itself. [...] If a team has a high quality internal documentation then user signals included in it will have a higher impact on product performance.

## Increases cross-functional collaboration

The report also mentioned that cross-functional collaboration is important. 

> Responsibilities extend beyond simply shipping software. This approach to software development can help developers break out of silos, seek alignment, foster teamwork, and create opportunities to learn more from others.

This aligns with user-driven (and value-driven) development. Breaking silos is important; software engineering, and everything around it, is too big and complex for a single team to solve in most organizations. 
 
# What else?

There is more in the DORA report which I won't be covering here. Those are important topics, such as AI Adoption, Platform Engineering, Shifting Priotities, Transformational Leadership, (and what skills a leader must have to be effective).

{% capture notice-2 %}
<a target="_blank" rel="noopener noreferrer" href="https://dora.dev/research/2024/dora-report/" class="btn" title="Accelerate State of DevOps | 2024 DORA Report" style="font-size: 1em;"><i class="fa-solid fa-link fa-3x" style="vertical-align: middle" aria-hidden="true"></i><span>&emsp;Accelerate State of DevOps | 2024 DORA Report</span></a>
{% endcapture %}
<div class="notice">{{ notice-2 | markdownify }}</div>

# Post Series
This post is part of a larger series.

* [Accelerate State of DevOps: Developer Experience](/developer%20experience/2025/07/09/accelerate-state-of-devops-2024-developer-experience.html)
* [Accelerate State of DevOps: AI Adoption](/developer%20experience/2025/07/25/accelerate-state-of-devops-2024-2-ai-adoption.html)