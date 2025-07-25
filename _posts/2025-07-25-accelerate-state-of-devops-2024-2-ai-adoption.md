---
layout:     single
classes:    wide
title:      "Accelerate State of DevOps: AI Adoption"
categories: [Developer Experience]

tagline: "User-centricity can improve software development"
header:
  overlay_image: /assets/images/headers/leaf_1280x325.png
image:
    path: assets/images/opengraph/leaf_325x325_with_name.png
    width: 325
    height: 325  
---
{% include post_category_and_date.html %}

I recently re-read the [2024 DORA Report](https://dora.dev/research/2024/dora-report/). Here are my thoughts on what the report has to say about **AI Adoption**. For more on the DORA Report, see my [other posts in this series](#post-series).

# AI Adoption
## Improvements with AI adoption
The DORA researchers observe improvements in software engineering where AI is used:

> AI seems to improve code quality and reduce code complexity (see below figure). When combined with some potential refactoring of old code, the high-quality, AI-generated code could lead to an overall better codebase. This codebase might be additionally improved by having better access to quality documentation
> 
> ![Software engineering improvements with 25% AI adoption](/assets/images/posts/dora2024_aiadoption_engineeringperformance.jpg){: .align-center}
> Software engineering improvements with 25% AI adoption

I take these results with a grain of salt. Although the DORA Report was published late October 2024 and the data is from earlier that year, which means that AI tooling likely improved since, general quality improvements would strongly depend on the quality processes organizations already have in place. 

If AI-assisted development tooling is introduced in teams where engineering practices are weak or absent, these tools likely do more harm than good. Their non-determinstic nature may also lead to ineffiencies, as iterative prompting may lead developers into a rabbit hole.

I do believe AI helps with documentation quality, mostly because this is often absent or an after thought. AIs can improve documentation comprehension by making it more readable and contribute to its completeness. I don't believe it would be able to close documentation gaps, especially not in regards to design decisions. These engineering tasks heavily depend on business, organizational and technical contexts that are hard for LLMs to understand - mostly because much is often implicit.
 
## AI is hurting delivery performance

The researchers found that using AI does not always help:

> Contrary to our expectations, our findings indicate that AI adoption is negatively impacting software delivery performance.

They assume that AI has a negative impact on best practices, in this case small units of work:

> We hypothesize that the fundamental paradigm shift that AI has produced in terms of respondent productivity and code generation speed may have caused the field to forget one of DORA’s most basic principles — the importance of small batch sizes. 

> That is, since AI allows respondents to produce a much greater amount of code in the same amount of time, it is possible, even likely, that changelists are growing in size. DORA has consistently shown that larger changes are slower and more prone to creating instability.

It is clear to me that engineering rigor needs to be continuously reviewed and adapted with the introduced of new tooling - in this case AI-assisted development tools. The introduction of AIs in the software engineering process must be carefully considered. It is good to experiment and try out new tools, however this should be done in a limited setting. AIs can have a huge impact on software and development, and as such should be tried out in environments where their harm are limited, such as in sandboxes and for prototypes.

## High-performing teams and organizations use AI, but products don’t seem to benefit.

The researchers looked at the impact of AIs on software product quality:

> Product performance, however, does not seem to have an obvious association with AI adoption.
> 
> ![Product performance improvements with 25% AI adoption](/assets/images/posts/dora2024_aiadoption_productperformance.png){: .align-center}
> Product performance improvements with 25% AI adoption
>
> Product performance is defined as the usability, functionality, value, availability, performance (for example, latency), and security of a product.

They postulate that AI contributes to engineering much more than to software quality:

> NFRs and quality characteristics determine product quality much more so than what is currently gained with AI (improvements in development, such as code quality, documentation, and delivery speed)

That makes sense. Software quality, typically defined as quality characteristics and non-functional requirements, are much more abstract and harder to grasp. They are often cross-cutting and materialize as across multiple system components.

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