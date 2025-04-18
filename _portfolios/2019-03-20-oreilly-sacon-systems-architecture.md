---
title: 'Content systems architecture: approaches in a decoupled world'
subtitle: "O'Reilly Software Architecture Conference 2019"
date: 2019-02-06 00:00:00
featured_image: '/images/2019-oreilly-csa/2019-oreilly-csa.001.jpeg'
excerpt: “Talk synopsis and slides from session at O'Reilly Software Architecture Conference NYC 2019”.
link:
---
### Description
Ten years ago, content “systems” were primarily content management applications and their kin; wikis, commerce sites, closed-box print applications, etc. Architecture was software solutioning and scaling the infrastructure to handle more traffic. DevOps meant “add Jenkins”. Eight months of development work generally required a week or two of architectural deliverables, even when third-party services were involved.

Last year, as content systems architect for The Economist, Diana Montalion and her colleagues invested six months articulating the capabilities of the current system and crafting technology recommendations across the multiple engineering and architectural teams. Then they spent another six months designing the high-level target architecture.

What changed between then and now? The difference between legacy and modern content systems is as conceptual as it is technical. Architecting emergent systems requires an evolution from strategic planning to collaborative strategic thinking – everyone seeing the parts through the lens of the whole. Architecture, and the role of architect, isn’t simply AWS certification. We are also a systems integrator, mirroring the desired qualities of the system and telling it’s story.

----

![](/images/2019-oreilly-csa/2019-oreilly-csa.002.jpeg)

### Once upon a time …
Once upon a time, in 1993, the Mosaic browser adds the `<img>` tag to Tim Berners-Lee hypertext language and the world wide web (as a content system) is born. Over time, CSS emerges and hypertext gets some style.

Then, applications that create dynamic websites arrive. PHP. Relational databases. In 2006, Automattic trademarks Wordpress and I enter this profession full time through the doorway of web content management systems. I love them. I download Drupal and want to figure out how to use it. So I find a client who needs a web content tool, The Missoula YWCA.

A few years later, I’m living in little Silicon Valley (Austin) and working with a team who is stretching open-source applications beyond their comfort zone. For example: Integrating MediaWiki with the custom donation system built my colleague and add credit card processing to handle millions of transactions a month. That’s integrated with CiviCRM to manage the gazillion records but it can’t dedupe them yet. That's fun! Some of the work is hell but mostly, I learn a lot and enjoy the people.

The first time I fly to London to meet *The Economist* editors with my colleagues, we are CMS software architects and devs helping them build their new Drupal website. *The Economist* ecosystem is a print publication and a cold-fusion website. Moving to Drupal is moving them towards daily publishing. The website will become the biggest Drupal site at the time, so there's complexity. For 18 months, we build features, like the homepage and Topics and Events. I integrate with their internal teams during weekly leadership meetings and daily cross-team code reviews.  One codebase gives us visibility into what others are doing. I adore them. Then, I move on to other roles with other teams.

Fast forward five years. The Drupal site now runs over 400 custom modules. In addition to the print publication and the website there are five device-specific apps and approx. forty other products or destinations for content. Multiple teams are working on multiple code bases creating multiple product authoring tools that operate within separate ecosystems. A product is publishing content in Mandarin. There are films and podcasts, interactive infographics, and what seems like a million 3rd party integrations.

So ... they are decoupling. There will be a React front end for the website and a microservices content distribution platform that will gather content from multiple authoring tools, beginning with Drupal, and serve content to the products and platforms. (I still think this was a brilliant move.) Continuous integration. Cloud hosting. Canonical content model. Context.

Simultaneously, I am moving to NYC, planning to take a few months off after a challenging year. The CTO offers me chartreuse and a contract. I am lured by the challenge of structuring an approach to system architecture. Even though my first task will be to get Drupal to throw up content onto the microservices architecture.

We deliver the initiative (a story for another day) and I take the originally-intended time off. Then. I rejoin the team as the content systems architect. Our teensy tiny little goal is to replace the print authoring software and Drupal and numerous other attached pieces with a modern content authoring system that will integrate with the content platform. Also, move the apps to using the content platform. Also, rearchitect the image and graphics distribution architecture (and integrate it with the DAM).

Essential goal: The weekly edition has come out every week since 1843. Don’t break that streak.

The first step is to model the current system and analyze it’s breaky bits. I discover two things: the model would be … undigestible. And nobody knows how it all works anymore. Everyone knows the part they know, including me.

So, we write a story, The Article Journey. My partner in disruption, Phil Kenny (Head of Graphics) makes a graphical depiction with breaky bits icons to attach. Now, at least, we can enable everyone to begin by understanding where we are, without shared specialized knowledge. Honestly, despite the flaws, the system is quite miraculous.

Very few people outside of our small team and the CTO want this change. One editor says, “you can have my tools when you pull them out of my cold dead hands”. The few that do want the upgrade don’t want it now. Eighteen months later, everyone including Editor in Chief and CEO says, “this is a strategic imperative.” How did that happen?

Hard work, good people collaborating and luck. Mostly, we approached it differently from all earlier initiative. That is the argument I’m here to make today:

![Software architecture must evolve towards systems thinking in order to meet the needs of emergent content systems.](/images/2019-oreilly-csa/2019-oreilly-csa.003.jpeg)

### Important: Define things

Many times, I've been misunderstood because I thought everyone understood words or concepts the same way. They didn't and they don't. One of the best practices to develop in systems architecture is to define what you mean and ask others what they mean.

![Content systems consist of cohesive yet distinct entities that are interrelated and interdependent, forming a whole which has a structure and purpose that defines its boundary.](/images/2019-oreilly-csa/2019-oreilly-csa.004.jpeg)

This might include, for example, multiples web CMSs and asset managers.

![Systems thinking is the fuzzy area of understanding the boundaries that distinguish it from other systems and defining what interrelated and interdependent mean within those boundaries.](/images/2019-oreilly-csa/2019-oreilly-csa.005.jpeg)

![“The ecosystem in which the content shares branding and editorial oversight and the entities communicate, rely on and/or react to each other somehow.”](/images/2019-oreilly-csa/2019-oreilly-csa.006.jpeg)

My definition of a content system is still a work in progress.

![Emergent means greater than the sum of its parts because it depends not on individual elements but on the structure of relationships between them.](/images/2019-oreilly-csa/2019-oreilly-csa.007.jpeg)



### The New York Times 2020 Report
The [NYT published a report](https://www.nytimes.com/projects/2020-report/index.html) outlining their strategy for doubling their digital revenue by 2020, to $800 million, by increasing digital subscriptions. It illustrates the “emerging constant system.” I admire them from afar but I don’t know them - that’s why I pick this. The report is a song I hear sung by many organizations.

#### Some highlights:
![They value visual and digital media native reporting. They value journalists who code. They envision an ecosystem of digital products. Success does not equal page views.](/images/2019-oreilly-csa/2019-oreilly-csa.008.jpeg)

* They value visual and digital media native reporting. They're software hinders this.
* They value journalists who code. Can you imagine the workflow required?
* They envision an ecosystem of digital products like Daily Briefing, Cooking, Wirecutter. Delivery requires vision-driven journalism that creates a context and emergent teams to build the systems.
* Success does not equal page views. They are subscription driven but more importantly, they are relationship driven. Readers have valuable experiences they can’t have anywhere else. Engaging readers is also essential (including and beyond comments).

### tl;dr
Three most valuable lessons I learned weren't "technical". Over my career, the tech has constantly changed. These three have only grown more consistently valuable:

![Make discussions transparent. Partner with subject matter experts and people who have complimentary skills. Define words. ](/images/2019-oreilly-csa/2019-oreilly-csa.010.jpeg)

1. Make discussions transparent. Discuss once, ever after, send a link.
2. Partner with subject matter experts and people who have complimentary skills. You need them.
3. Define words. Especially when you think the concepts are obvious.  

### And the winner of Most Valuable Lesson is ...
Everything we’ll talk about is focused more on cultivating emergent behavior than on *which tools you use to do it.* The beginning tools I’ll recommend seem simple, perhaps even obvious, but they are powerful ways to create that synergy.

![Teams that cultivate emergent behavior build emergent systems](/images/2019-oreilly-csa/2019-oreilly-csa.011.jpeg)

We succeed when we create a structure in which interaction and cooperation between different viewpoints delivers a better outcome or solution than isolation or command.

![Architects are system integrators](/images/2019-oreilly-csa/2019-oreilly-csa.012.jpeg)

### Architects are system integrators
The role of the architect is contentious and endlessly debatable. There are as many types of architects as there are people architecting. How close to the code are you? Do you own decisions? At this wonderful conference, there are many discussions about technologies like Kubernetes and Microservices and approaches like Domain Driven Design. That’s all good. That’s all *part* of what we are talking about. Somewhere in every toolbox is an AWS model.

I encourage exploring those and frameworks like TOGAF and join the discussion on Lean Architecture. Whatever tools you use, they are always woven together with systems thinking. Cultivating systems thinking is what we’ll explore.

![You are not and don’t need to be the expert on everything.
You are the expert at *integrating* everything.](/images/2019-oreilly-csa/2019-oreilly-csa.013.jpeg)

My premise: You are not and don’t need to be the expert on everything.
You are the expert at *integrating* everything.

You look for the blind spots, stuck places, noisy conflicted OIL CAN places, inconsistent and unreasoned thinking. And resolve them. Sometimes with tech but more often _with people’s thinking about tech_.

Do not swim alone! Architects are vulnerable. We speak truth to power, our job is to uncover blindspots and Conway’s law is inescapable. Partner with people who’s work you trust.

![Thanksgiving with the architect](/images/2019-oreilly-csa/2019-oreilly-csa.014.jpeg)

### Thanksgiving with the architect
What is a “systems integrator”? To illustrate ... Imagine Thanksgiving dinner. If you aren’t American, imagine a holiday meal. One approach to organizing the meal, with it’s familiar parts like cranberry sauce, turkey, stuffing, pumpkin pie, etc is to have someone in charge of cooking and delegating tasks. The “What can I bring?” method. When you ask "what can I bring?", the cook might say “a bottle of red wine” or “a pumpkin pie”or “avoid nuts, Aunt Jill is allergic”. Without this person, you might end up with ...

![five pumpkin pies](/images/2019-oreilly-csa/2019-oreilly-csa.015.jpeg)

At the table, you are grateful to him / her for all their hard work.

A systems integrator approach would be different. The goal is to leverage the creativity and expertise of everyone involved. The integrator ensures that everything fits together and there isn’t five pies.

But the integrator also combines and coordinates the efforts so that the sum is greater than the parts. Who makes fabulous pies? Enlist them. Shall we order rolls from that amazing bakery? Vegans are coming?! No problem! We'll adapt the context to include vegan favorites while still creating a “thanksgiving” experience. The goal is more catalytic than delegatory.

The host's role is to structure cooperation, minimize conflict and most importantly, craft _a delicious, satisfying, and enjoyable meal_. Yes, this means being very good at food. Added to that is cultivating conceptual integrity. At that table, the convergence of special and unique elements simply combine to make an *excellent thanksgiving dinner*. The hosts role, in this case, is harder to see but ultimately valuable to the process.

![turkey frying fire](/images/2019-oreilly-csa/2019-oreilly-csa.016.jpeg)
Unless there is turkey frying … honestly, I don’t understand this. Don't do this.

### Architects create conceptual integrity by structuring argumentation
Argumentation is collective decision making and cooperative problem solving undertaken when conditions are uncertain. In content systems, conditions are *always* uncertain and changing. The goal of argumentation is to discover the best possible solution(s) under the circumstances. Which means understanding, first and foremost, “best” and “possible solutions” and “the circumstances”. Reasons are given to support (or not) the best possible solution. Preparation is required to ensure those reasons are strong. Everyone involved considers ways to strengthen the reasons (argumentation is collaborative, not fighting.)

![](/images/2019-oreilly-csa/2019-oreilly-csa.017.jpeg)

Imagine a small group of people with differing views gathered together to make a technology-related decision. Without structure, these discussions can go in endless circles and often rely on power rather than reason. I’ve seen teams significantly increase decision-making efficiency and minimizing noise (and war) by using a top-down elaboration (TDEs) model. TDEs are really documents but that word frightens people.

Simpler is better, one-page is usually enough and it will evolve as the situation evolves.

Anyone can make one and whenever two or more are gathered, someone should. We *all* jump right into *how* when solving issues or build things. We wouldn't be architects if we didn't love *how*. The tricky part is - the people in discussion are often solving different problems, for different reasons and don’t know it. Or worse, there *isn’t* a reason to be discussing it. TDEs keep everyone on the same page.

![](/images/2019-oreilly-csa/2019-oreilly-csa.018.jpeg)

#### Summary
What is the best possible solution under the circumstances and what are the highest-value reasons that support this conclusion? (Usually, 3-5.) The summary can be at the top, the bottom ("Therefore,") or implicit throughout the TDE.

#### WHY?
Describing WHY is difficult. We usually don't aim high enough. Most of our WHY reasons are really WHAT reasons. "A world-class solution for our customers" is a WHAT. WHY does "world-class" *matter* and how do we measure it?  A general rule is: Everyone who reads the WHY will understand the value

> Imagine Frodo throwing The Ring into the river of molten lava. Imagine a woman standing beside a river on a spring day, taking off her wedding ring and throwing it in. Imagine a man in the midnight shadows walking along a river, sirens and police lights in the distance, taking a ring and other trinkets from his pocket and throwing them into the water. Same WHAT - entirely different WHYs.

#### WHAT?
What —exactly— are we talking about? Usually, this section describes what the solution will do and how it delivers on the WHY.

#### WHO?
Who is impacted and how do they benefit from the WHAT? Who will do the work? Including users and doers and perhaps decision makers defines the circle of people involved and how they will participate.

#### HOW?
How will we do, build, design and/or continue to explore the WHAT? How will we measure the value? Keep this discussion relatively high-level, linking to deeper materials. Here is where I describe any assumptions, issues, blockers, challenges or risks that convey an honest picture of the situation.

#### WHEN?
Everyone wants to know, first and foremost, “when will it be delivered and how much will it cost?” In reality, WHEN is the *last* piece of relevant information that can be understood. Describe how the answer will be discovered. Are there any timing issues or real-world deadlines? (Note: "We want this by April" is not a WHEN, it requires a reason.)

![Architects tell stories about what is and what could be by structuring the point of view](/images/2019-oreilly-csa/2019-oreilly-csa.024.jpeg)

When I imagine a content system, this is mostly what I see …

![Code repositories, AWS services, performance, scalability, infrastructure, CACHING, UX and design, testing, versioning, continuous deployment, QA, redundancy, resiliancy, security, 3rd party integration, version control, microservices, APIs, decouple, GraphQL, semantic tagging, search, CACHING, content architecture, responsive images, WYSIWYG](/images/2019-oreilly-csa/2019-oreilly-csa.025.jpeg)

While the tech will always be my first love and focus yet content systems are kaleidoscopes that shift depending on how you look at them.

![](/images/2019-oreilly-csa/2019-oreilly-csa.026.jpeg)

#### Money
How do you monetize content so people can pay their mortgages? Ads? Subscribers?
Readers
Who are the readers, what do they want? How do they want it - which devices do they read on? How do you measure reader engagement meaningfully?  *Where* do you measure it when engagement happens across the internet? Are comments dead?

#### Editorial
What is the editorial mission? How do content creators and editors create, edit, shape, approve, adapt and preview content? In a distributed system, preview it *where*?

#### Visual elements
How do images and interactives and graphical assets move through the system? Can they?

#### Associations
How do you relate content to each other? Taxonomies and lists are old school - wiki data. On the lowest level relationships are transforming.

#### Distribution
C.O.P.E. - do you need a system? What role does social media platforms, AMP, etc play?  What are the boundaries and interdependencies when you have 40 different products, multiple teams and six different authoring tools?

### Architects tell stories about what is and what could be by structuring the point of view
Two tried-and-true structures for approaching content systems architecture happen before diving too deeply into tech. Having a strong story, vision, of what people do with the system and what the system does is essential. Remember, we all love to jump into how. That is important. But not first. First, there is task analysis and Process modeling.

![Task analysis](/images/2019-oreilly-csa/2019-oreilly-csa.032.jpeg)

The first time I saw user testing of a web feature I'd built, I was shocked. Many people didn't interact *at all* the way I expected or designed the feature to work. Phil Kenny (remember him from the opening story?) made me sit down and watch how every senior editor did their job. I didn't want to -- now I always will. Doing the same process with designers saved us all a lot of confusion. Focus on *what* do people are doing, not how they do it. Understand why.

I know many technologists don't consider this "technical" work. But systems thinkers - they know better.

![Task analysis example](/images/2019-oreilly-csa/2019-oreilly-csa.033.jpeg)

![Task analysis example](/images/2019-oreilly-csa/2019-oreilly-csa.034.jpeg)

While the system delivering content from multiple sources to multiple destinations might be complex, the business process is usually simple: Publish Article. Read Article. Use these words that everyone understands can tell the story at whatever level of detail is appropriate.

![Process model example](/images/2019-oreilly-csa/2019-oreilly-csa.035.jpeg)

Note: You want people to use the tools and they won’t if they must learn complicated techniques. If you require them, teach them too.

![Therefore](/images/2019-oreilly-csa/2019-oreilly-csa.036.jpeg)

### Therefore,
* Software architecture must evolve towards systems thinking in order to meet the needs of emergent content systems.
* Cultivate emergent behavoir with collective decision making and collaborative problem solving (aka argumentation).
* Architects are system integrators who create conceptual integrity by structuring argumentation.
* Architects tell stories about where we are and where we are heading from multiple points of view.

### Equifinality
![](/images/2019-oreilly-csa/2019-oreilly-csa.037.jpeg)

I hope that we agree that there a many paths to the same place. A framework that supports system thinking is emerging. My cohorts and I are writing a book on it but there is brilliant thinking everywhere here. The point is not to elucidate One Way but instead, to apply the right constraints that ensure the system has integrity. And that emergent behaviors are creating emergent systems.

I wish you luck on your journey and thank you for sharing mine.
