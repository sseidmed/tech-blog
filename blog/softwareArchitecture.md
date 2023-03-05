---
title: Fundamentals of Software Architecture/By Mark Richards, Neal Ford
date: 2022-05-10
---

# The definition of a software architect

No good definition of what a software architect is, because it's always evolving.
Different titles for the same role.
8 core expectations of an architect:
	1. Define architecture and design principles to guide technology decisions for the enterprise (key is guide)
	2. Constantly analyze the software enviroment. Is it still viable and up to date with the ongoing changes, example new technologies or other business integrations
	3. Keep up with new technology trends and industry trends
	4. Ensure compliance with the architecture. 
	5. Have exposure to multiple and diverse technologies, platforms and enviroments. You don't have to be an expert, but have enough familiarity. Stretching the comfort zone and take initiative.
	6. Business domain expertise/core business aspects. This is a challenging part, because you have to communicate with business owners.
	7. Interpersonal skills like teamwork, facilitation and negotiation. People skills.
	8. Understand political climate of enterprise and navigate office politics. Communicate your decisions and your design patterns. Understand who cares about those decisions, because those decisions will be challenged.
What is software architechture? Not just the pattern or the structure of your software, but also why certain decisions were made. For instance, certain layers don't have access to other layers in software.

# How to think like an architect
Technical breads vs. depth

stuff you know (maintain)
stuff you know you don't know (focus here, what exists rather than how to implement stuff), focus on wider picture, survey material
stuff you don't know you don't know (make this part smaller)

Where to draw line: architecture and design

1. identify architecture characteristics
2. identify which archictecture patterns (ex: microservices, kernel)
3. identify core components

Then hand it all over to devs, but it's not the end of this process.

That process needs to be bi-directional and collaborative, because architecture is an ongoing process. Have a feedback loop, i.e. back and forth communication.

How to stay active in code base as an architect: Hands on coding vs architecture - find balance
1. Little spikes of coding (Carve out an interesting aspect or functionality of the codebase for yourself to work on, probably something less significant)
2. Pair programming with junior or senior devs
3. Code reviews

# Architect's key responsibilties: they must know the following and more:

Scalability
Availability
Testability (ease and completeness of testing)
Learnability
Deployability (ease and risk of deployment)

They don't come from user stories, but from business.

Business -> business is always changing to meet the demands of the marketplace
Architect's interpretation -> Agility (respond to change fast, be modular)

Business -> Complete end-of-day processing on time
Architect's interpretation -> Performance, Scalability, Reliability (recover from crash), Restartability, Availability

Business -> We need faster time to market to remain competitive
Architect's interpretation -> Agility, Testability, Deployability

Business -> Engage heavility in mergers and acquisitions
Architect's interpretation -> Interoperability, Extensibility, Openness, Scalability, Learnability, Standards-Based, Modularity

Business -> Time timeframe and budget for this project
Architect's interpretation -> Feasability (look below)

Always challenge a business requirement if it gets too diffcult. Sometimes, business gives an architect requirements but really they are solutions instead of requirements. Understand the requirements before forming a solution.  

# Tradeoffs of those architecture characteristics

Trying to do everything/all requirements

Requirement <--> Solution

Need to analyze the tradeoffs

ATAM - Architecture tradeoff analysis method. How to get it to work? Focus on the goals.

1. Discussion with stakeholders
2. Evalution 1 - Finding holes in the architecture, finding balance between '-ibilities'
3. Evaluation 2 -Further refine that tradeoffs

Goals of ATAM
1. Create architecture presentation
2. Validate the architecture and establish tradeoffs
3. Identify and mitigate risk
4. Get stakeholder buy-in (or anyone who has vested interest)

CBAM - Cost-benefits analysis method

Maximize the difference between cost and benefits