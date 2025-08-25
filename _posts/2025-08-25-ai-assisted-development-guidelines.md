---
layout:     single
# classes:    wide      # wide doesn't work with right-side TOC
title:      "Guidelines for AI-Assisted Development"
categories: [AI]

toc: true
toc_icon: "cog"
toc_sticky: true

tagline: "Divide and conquer"
header:
  overlay_image: /assets/images/headers/leaf_1280x325.png
image:
    path: assets/images/opengraph/leaf_325x325_with_name.png
    width: 325
    height: 325  
---
{% include post_category_and_date.html %}

I collect the development guidelines and best practices for AI-assisted development here. These are based on my own experience using LLMs as well as those from others.

{% capture notice-1 %}
<div style="float:left;"><span style="color:Dodgerblue"><i class="fa-solid fa-lightbulb fa-3x" style="vertical-align: middle" aria-hidden="true"></i></span></div>
<div><span>Key skills are in the LLM age (as before) are <b>critical thinking</b>, <b> adaptability</b> and <b>first principles thinking</b>.</span><div>
{% endcapture %}
<div class="notice">{{ notice-1 | markdownify }}</div>

# Setup

## Tech Stack
* **Use a common tech stack.** LLMs will likely had a lot of training data on common tech stacks.
* **Use a runtime framework that can do a lot of heavy lifting.** That way the LLM needs to generate less code.
* **Use application topologies that have clearly established patterns.** It is relatively easy to give LLMs a set of patterns to follow. For example, controller, service, repository, entity.

## Tooling
* **Use coding assistants that can access the code base.** LLMs need access to the code base to their work properly. They need to read and search the codebase, react to linting errors, retry when it fails, etc.
* **Use coding assistants that can create subtasks.** This provides a multi-agent coding setup without having to build something from scratch. Examples are Claude Code, Roo Code, Kile Code.

# Using LLMs

## General
* **Start with a high-level architecture generation.**
* **Start with a test before code implementation.** This is the TDD methodology.

## Context Engineering
* **Provide just-enough context.** Too little context leads to hallucinations. Too much context causes the AI to focus on unimportant aspects or becomes overwhelmed (it doesn't have an attention mechnanism humans have).
* **Recursive generation.** Recursive generation: Generate changes in stages, focusing on different aspects. Apply changes gradually in smaller commits — this is particularly important to help the human reviewing the change to be able to digest the changes.
* **Directed focus.** Only include the parts of the code directly relevant to the modification
* **Assign roles and perspectives to LLMs.** This increases quality of the results.
* **Ensure the LLM asks for confirmation before every change.** You don't want it to divert from your goal.
* **Restart coding sessions as frequently as possible.** LLMs generation results still become more hit and miss the longer a session becomes.
* **Use example code snippets for patterns.** This enforces the LLM to use patterns (e.g. entity, repository) libraries of our choice, rather than just choosing one for his liking. This also helps with maintaining the code, as it would allow to change to different libraries much easier.
* **Use a reference application.** This provides sample code and connect to to the LLM through an MCP server. It ensures that the samples we provide compile and are consistent.

## Code Reviews
* **Use AI-powered code reviews for grunt work.** They can automatically flag duplicate code and bad patterns. It can also enforce style guides and carry out routine checks. It can speed up deployment and democratize expertise by sharing its knowledge.
* **Ensure human accountability.** Code reviews work because there are two people responsible for code quality. Their collaboration results in consensus and constructive feedback rather than pride and 'doing it right'. AIs cannot be held or consider accountable as they lack context and are not human (they don't judge).
* **Provide oversight.** Experience shows that 60% of the time goes into preparing context for the AI: code snippets, documentation, explaining the change. The AI must be guided through the review, and its output must be verified. (But it leads to a more thorough review in the same amount of time.)
* **Use tools like CodeRabbit.** These tools generate rweview comments on your pull requests. It can generate a PR summary, scan for vulnerabilities, check naming conventions, and identify missing test cases. (CodeRabbit integrates with GitHub and GitLab.)
* **Context Enrichment.** Use a cloned repo, focus on changes only, discard changes to ancillary files (e.g. auto-generated code and dependencies), construct a code graph to understand how files interrelate, learn from past review (store results intermittently), include open and past PRs, and use linters and SAST tools.
* **AI as pair programmer.** AIs are better at evaluation than design. Checking for errors and comparing code against best practices is more straightforward than creative design.
* **Use a review agent.** Use a review agent to double check the LLM's work against the original prompts. This catches mistakes and ensures the generated code adheres to the requirements and instructions.

## CI Integration
* **Automated PR generation.** Create PRs to group code modifications associated with each specification
* **Test validation.** Run tests automatically on generated changes.
* **Human review prompts.** Generate explanations for human reviewers.

# When and where to LLMs
* **Use manual techniques to provide structure when you have a simple CLI.** For example to bootstrap the scaffolding (e.g. a Spring Boot application).
* **Use for prototypes, internal tools, or MVPs.**
* **Use traditional development practices for mission-critical systems.** So not use vibe coding for important systems, e.g. healthcare, finance, aerospace. Possibly augment with AI tools like Copilot Workspace or Cursor for productivity gains.
* **Vibe coming should be considered only for throw-away projects.** The practice produces bad software that does not scale, is not secure, and doesn't meet exact requirements. It leads to Shadow IT.

# Advice to Engineering Leaders

## Meaningful Experimentation
* **Guide the engineers** by understanding the real impact of AI tools and make sure they are on board with the direction. Some engineers are over-eager and need to be toned down, others are skeptical and stay away from using the tools.
> Engineers need to learn how to compensate for the limitations and resist the siren call of sloppy software design.
> 
> The best way to move your own engineering org towards this middle path is by encouraging engineers to meaningfully engage with this technology, in order to collectively understand both its capabilities, and its limitations.
* **Keep the pace** because the AI technology is evolving very fast. The tools and techniques that are state-of-the-art today will very likely be old hat within a year or two. To keep up, a strong culture of ongoing experimentation and knowledge sharing is required. 
* **Empower teams** with auotnomy around exactly how they can meaningfully experiment with AI-assisted coding.
* **Define objective measures** which track progress towards adoption.
* **Provide organizational support** through training, making sure everyone has access to whatever tools and services they need, and establish peer support via a Community of Practice.
* **Establish KPIs** which clearly communicate current state and target state - where we are and where we want to get to. Use metrics that indicate 
* **Use metrics** that measure whether teams are making meaningful investment in trailing AI-assisted coding and share what they learn.
> Useful metrics may include
> * Number of tools piloted by each team, categorized by type
> * Has the team done an AI tool retro in the last month
> * How much activity is there in the community channels (e.g. Slack, Viva)
> * What is attendance like for Community of Practice meetings 
* **Communicate a clear target** to the teams, starting with the Experimentation metrics and gradually expanding to Adoption and Impact as teams progress. 
> Example: “By the end of the month we expect all teams to have piloted at least two tools in each of these categories, held an internal retro, and identified next steps for experimentation”.
* **Provide a training program** to accelerate skill development.

## Adoption
* **Use metrics** that measure the actual adoption of AI tooling. This may vary across teams as their goals and focus differs.
> Useful metrics may include
> * Usage of tools - which teams are using which tools for which tasks (code completion, agentic coding, code review, UX prototyping, etc).
> * Sentiment - Does AI make you more productive?
* **Communicate the adoption target.** This should include objective feedback on their progress while still giving the teams autonomy on how to achieve that goal.
> Example: “Here’s where you are today according to the most recent AI adoption survey. Here’s how those metrics compare to other teams, and here’s how it compares to our goal for the end of the quarter.
>
> What are your plans for achieving that goal, and what can the organization do to support you?”
* **Support AI adoption** by providing some lightly-prescriptive guidance, particularly at the start. Provide them with direction, but allow them to be autonomous and choose a different approach if that's what they want.
> This can be done in various ways:
> * A kickoff session to discuss the program, share goals, and brainstorm ideas
> * Scheduled informal brown bag sessions to share what people are doing
> * An AI-dedicated team retro

## Impact
* **Use metrics** that measure the impact of the AI tooling. What does AI assistance do in terms of productivity, quality, agility, etc. 
> The best approach here is to use the same sort of general metrics you’d use for engineering productivity - things like DORA, SPACE, etc.
> 
> If you’re also measuring AI adoption for teams then you can combine these two sets of metrics to figure out whether AI adoption affects things like Change Failure Rate, Lead Time, MTTR, etc.

## Remove Organizational Impediments
* **Budget.** Demistify cost concerns by comparion the license cost against a fully loaded cost of an engineer and the boost they can get from AI assistance. The license is really a marginal cost. Make sure teams have budget approvals.
* **Compliance.** Get clearance for at least a "pilot program" level of access to the latest tools. Choose tools that support self-hosted or dedicated-tenant deployment models in case you will need that.
* **Provide time.** Work with leadership to ensure the engineers actually have time to start working with the AI tools. Ask for executive championing. Let the teams know that they have the time (or else they may just continue with the every business activities).
* **Create a Community of Practice.** This can provide a significant boost in the adoption. These should be grass-rooted and centered on practitioners, however leaders should plan to provide initial support. Assign someone for clear accountability to bootstrap the CoP (meetings, touch-points, leading).
* **Lead with empathy** to show to engineers that you understand their concerns around AI and address it heads-on. Also ensure that the metrics are not misinterpreted or misused. Don't share granular metrics with leadership.
* **Communicate progress** to teams to help them understand how they are progressing, and report the overall progress to people outside engineering.

# Sources
* [MartinFolwer.com - How far can we push AI autonomy in code generation?](https://martinfowler.com/articles/pushing-ai-autonomy.html)
* [Medium - Generating Code with LLMs: A Developer’s Guide](https://mskadu.medium.com/generating-code-with-llms-a-developers-guide-part-1-0c381dc3e57a)
* [Korny Sietsma - A real-world AI coding case sample](https://blog.korny.info/2025/07/18/a-real-world-ai-coding-case-sample)
* [iDesign Alumni - #1 Skill in the Age of AI: Critical Thinking](https://groups.google.com/g/idesign-alumni/c/Hkb7W4VJswo) (private thread)
* [Milan Milanović - How to do code reviews with AI tools](https://newsletter.techworld-with-milan.com/p/how-to-do-code-reviews-with-ai-tools)
* [CodeRabbit - The art and science of context engineering for AI code reviews](https://www.coderabbit.ai/blog/the-art-and-science-of-context-engineering?utm_source=fnf&utm_medium=newsletter&utm_campaign=coderabbit-august&utm_term=lmezzalira&utm_content=context-engineering-blog)
* [Steve Fenton - Vibe Coding: The Shadow IT Problem No One Saw Coming](https://thenewstack.io/vibe-coding-the-shadow-it-problem-no-one-saw-coming/)
* [Pete Hodgson - Leading your engineers towards an AI-assisted future](https://blog.thepete.net/blog/2025/06/26/leading-your-engineers-towards-an-ai-assisted-future/)