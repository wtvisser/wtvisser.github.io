---
layout:     single
classes:    wide
title:      "Accelerate State of DevOps 2024 (3): Platform Engineering"
categories: blog
tags: 
  - platform

tagline: "And what it means for software engineering"
header:
  overlay_image: /assets/images/headers/leaf_1280x325.png
image:
    path: assets/images/opengraph/leaf_325x325_with_name.png
    width: 325
    height: 325  
---

Platform engineering is a sociotechnical
discipline where engineers focus on
the intersection of social interactions
between different teams and the
technical aspects of automation, selfservice,
and repeatability of processes.

In platform engineering, a lot of energy
and focus is spent on improving the
developer experience by building golden
paths, which are highly-automated,
self-service workflows that users of
the platform use when interacting
with resources required to deliver and
operate applications. Their purpose is
to abstract away the complexities of
building and delivering software such
that the developer only needs to worry
about their code.

Some examples of the tasks
automated through golden paths
include new application provisioning,
database provisioning, schema
management, test execution, build and
deployment infrastructure provisioning,
and DNS management.

Concepts in platform engineering: moving a capability down (sometimes
called “shifting down”)2 into a shared
system 

A key factor in the success is to
approach platform engineering with
user-centeredness (users in the context
of an internal developer platform are
developers), developer independence,
and a product mindset.

Internal developer platform
users had 8% higher levels of individual
productivity and 10% higher levels of
team performance. Additionally, an
organization's software delivery and
operations performance increases
6% when using a platform. However,
these gains do not come without
some drawbacks. Throughput and
change stability saw decreases of 8%
and 14%, respectively, which was a
surprising result.

At both the team and individual level we
see a 5% improvement in productivity
when users of the platform are able to
complete their tasks without involving an
enabling team. This finding points back
to one of the key principles of platform
engineering, focusing on enabling selfservice
workflows.

For platform teams, this is key because
it points to an important part of the
platform engineering process, collecting
feedback from users. Survey responses
did not indicate which forms of feedback
are most effective, but common
methods are informal conversations
and issue trackers, followed by ongoing
co-development, surveys, telemetry,
and interviews.

# The unexpected downside

We also
found that throughput and change
stability decreased.

**Throughput**
the added machinery that changes
need to pass through before getting
deployed to production decreases the
overall throughput of changes. In general,
when an internal developer platform is
being used to build and deliver software,
there is usually an increase in the number
of “handoffs” between systems and
implicitly teams.

Second, for respondents who reported,
they are required to “exclusively use the
platform to perform tasks for the entire
app lifecycle,” there was a 6% decrease
in throughput.

To counter this it is important to be
user-centered and work toward
user independence in your platform
engineering initiatives.

--> Developers and team must ahve a level of autonomy to choose standard platform tooling and augment it with their own. Interface is important. Independence is important.

**Change instability and burnout**

When considering the stability of the
changes to applications being developed
and operated when using an internal
developer platform, we observed a
surprising 14% decrease in change
stability. This indicates that the change
failure rate and rate of rework are
significantly increased when a platform
is being used.

Even more interesting, in the results
we discovered that instability in
combination with a platform is linked
to higher levels of burnout.

--> too much stress due to high cognitive load, changing focus, pressure. Reduce this complexity. This also explains the hypotheses below (instability)

the platform enables developers
and teams to push changes with a higher
degree of confidence that if the change
is bad, it can be quickly remediated. In
this instance the higher level of instability
isn’t necessarily a bad thing since
the platform is empowering teams to
experiment and deliver changes, which
results in an increased level of change
failure and rework

A second idea is that the platform
isn’t effective at ensuring the quality
of changes and/or deployments
to production.


With this
hypothesis, platform engineering is
symptomatic of an organization with
burnout and change instability.

-->  I doubt that ans isnt my experience. This is not the main reason to start on a platform team.

**Balancing the Trade-offs**

First, prioritize platform functionality
that enables developer independence
and self-service capabilities. When
doing this, pay attention to the balance
between exclusively requiring the
platform to be used for all aspects of
the application lifecycle, which could
hinder developer independence.

--> the below recommendation aligns with my thought above

As good practice, a platform should
provide methods for users of a platform
to break out of the tools and automations
provided in the platform, which
contributes to independence, however,
it comes at the cost of complexity.
This trade-off can be mitigated with a
dedicated platform team that actively
collaborates with and collects feedback
from users of the platform.

Second, carefully monitor the instability
of your application changes and try
to understand whether the instability
being experienced is intentional or
not. Platforms have the potential to
unlock experimentation in the terms of
instability, increase productivity, and
improve performance at scale.

# Links
published October 2024
https://dora.dev/research/2024/dora-report/