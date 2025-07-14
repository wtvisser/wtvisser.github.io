---
layout:     single
classes:    wide
title:      "Accelerate State of DevOps 2024 (2): AI Adoption"
categories: blog
tags: 
  - ai

tagline: "And what it means for software engineering"
header:
  overlay_image: /assets/images/headers/leaf_1280x325.png
image:
    path: assets/images/opengraph/leaf_325x325_with_name.png
    width: 325
    height: 325  
---

# Excerpts from summary findings

**High-levels of software delivery performance are achievable**
The highest performing teams excel across all four software delivery metrics (change lead time, deployment frequency, change fail percentage, and failed deployment recovery  time) while the lowest performers perform poorly across all four. We see teams from every industry vertical in each of the performance clusters.

**Platform engineering can boost productivity**
Platform engineering has a positive impact on productivity and organizational performance, but there are some cautionary signals for software delivery performance.


**Cloud enables infrastructure flexibility**
Flexible infrastructure can increase organizational performance. However, moving to the cloud without adopting the flexibility that cloud has to offer may be more harmful than  emaining in the data center. Transforming approaches, processes, and technologies is required for a successful migration.

# The promising impact of AI on development workflows
**Code Complexity**
The degree to which code’s intricacy and sophistication hinders productivity.

**Technical Debt**
The extent to which existing technical debt within the primary application or service has hindered productivity over the past six months.

**Code review speed**
The average time required to complete a code review for the primary application or service.

**Approval speed**
The typical duration from proposing a code change to receiving approval for production use in the primary application or service.

**Cross-functional (XFN) coordination**
The level of agreement with the statement: "Over the last three months, I have been able to effectively collaborate with cross-functional team members.”

**C**ode quality**
The level of satisfaction or dissatisfaction with the quality of code underlying the primary service or application in the last six months.

**Documentation quality**
The perception of internal documentation (manuals, readmes, code comments) in terms of its reliability, findability, updatedness, and ability to provide support.

![Improvements with 25% AI adoption](/assets/images/posts/improvements_with_25percent_AI_adoption.jpg){: .align-center}

AI seems to improve code quality and reduce code complexity (Figure 9). When combined with some potential refactoring of old code, the high-quality, AI-generated code could  ead to an overall better codebase. This codebase might be additionally improved by having better access to quality documentation

Better code is easier to review and
approve. Combined with AI-assisted
code reviews, we can get faster reviews
and approvals,

 
# AI is hurting delivery performance

Contrary to our expectations, our
findings indicate that AI adoption is
negatively impacting software delivery
performance

we hypothesize that the fundamental
paradigm shift that AI has produced in
terms of respondent productivity and
code generation speed may have caused
the field to forget one of DORA’s most
basic principles—the importance of
small batch sizes. That is, since AI allows
respondents to produce a much greater
amount of code in the same amount
of time, it is possible, even likely, that
changelists are growing in size. DORA
has consistently shown that larger
changes are slower and more prone to
creating instability.

Considered together, our data
suggest that improving the
development process does not
automatically improve software
delivery—at least not without proper
adherence to the basics of successful
software delivery, like small batch sizes
and robust testing mechanisms.

--> Takeaway: engineering rigor becomes even more important

# High-performing teams and organizations use AI, but products don’t seem to benefit.

**Product performance**
This is a factor score that accounts for the usability, functionality, value, availability, performance (for example, latency), and security of a product.

Product performance, however, does
not seem to have an obvious association
with AI adoption.

> NFRs and quality characteristics determine product quality much more so than what is currently gained with AI (improvements in development, such as code quality, documentation, and delivery speed)

# Links
published October 2024
https://dora.dev/research/2024/dora-report/