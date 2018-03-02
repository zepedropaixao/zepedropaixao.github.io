---
title: LeanHub
permalink: projects/leanhub/
breadcrumb: LeanHub
---

![Logo](/assets/imgs/leanhub/logo.png){:class="project-logo-leanhub"}

# What is it?

LeanHub aims to bring kaizen methodologies to distributed teams.

{% include youtube.html url="https://www.youtube.com/embed/ODrifsL7J2I?rel=0" description="LeanHub - Lean Deployment with Benefits Tracking" %}

Nowadays teams are becoming more and more remote and distributed. It's not uncommon to have management teams in one country and operational teams in another.

Kaizen has been very effective in implementing continuous improvement methodologies with local teams. Kaizen boards (physical) are very effective on natural teams, because they directly show how the team is progressing and they create a sense of urgency to go back on track. 

But with distributed / remote teams all around the world, this physical board loses its meaning.

This is where LeanHub came in.

It is the kaizen board online, according to official Kaizen Institute rules, as it was a joint-venture project between us and Kaizen Institute.


# My path at LeanHub

I was the person responsible for designing the initial version of LeanHub, sell the project to Kaizen Institute and manage the tech team to build what we had sold in time.

Despite being the one responsible for LeanHub, I only dedicated 80% of my time to LeanHub, the other 20% were dedicated to SIMI to try to get investment for it.

## Inception

My two partners at SIMI were also kaizen consultants working for Kaizen Institute. When the acquisition deal of SIMI was off and we stayed without any funds, we rapidly had to find a solution to be able to keep the team. We realized that our efforts, alone, going door to door selling SIMI wouldn't be fast enough for us to keep the team. 

So, we looked around us and tried to find a venture that would sustain the SIMI team, at least for a while, until SIMI could be invested.

LeanHub was a perfect fit, because we had the tech skills required to build it, and exclusive access to kaizen knowledge.

## Keeping the SIMI Team

The main objective was to keep the SIMI team while developing something that could improve the technical skills of the team.

In the end, we managed to build LeanHub where we gave our time and technical skills while Kaizen Institute would provide the knowledge and fund the whole project. We managed to keep some equity of this project, thus the joint-venture.

## The definition of the joint-venture 8 sprints

In the beginning, to convince the upper management of Kaizen Institute (KI) about this joint-venture, we had to define exactly what we would do, how long it would take, how much it would cost and which feature increments would be available after each sprint.

I was responsible for defining and designing which features would be available after each sprint. After some final adjustments done with the KI team, the 8 initial sprints were approved and the development started.

## Management, Marketing & Sales

Although I was responsible for the product definition and implementation, I was also responsible for managing the whole team, for the KI and LeanHub interactions (I had weekly meetings with the head of Kaizen Institute Iberia) and all our marketing & sales strategies to have a smooth go to market when the time came.

We implemented a landing page that allowed clients to subscribe to our newsletter to try to guarantee interest around the product.

{% include figure.html url="/assets/imgs/leanhub/landingpage.jpeg" description="LeanHub's landing page was designed to assess interest during the development." %}

While the development of the platform was being done we also created a blog where KI consultants would regularly post articles with knowhow about kaizen methodologies, to create the sense that we, LeanHub, were the goto place for knowhow. It's easier to sell if you've already established that you are the goto place for knowhow on the thing you want to sell.

{% include figure.html url="/assets/imgs/leanhub/blog.jpg" description="LeanHub's blog ascertained our position as a goto place for knowhow on Kaizen Methodologies." %}

## Software Engineering

For each sprint we would do a complete Design Sprint, just like the [Google Ventures Design Sprint](http://www.gv.com/sprint/), with a few customizations to our needs but still including all the steps originally defined in this design sprint, meaning, we would do all the diverge and design steps, we would make a functional prototype and finally test the design even before implementing it.

After defining exactly what would be done on the development sprint and distributing the tasks, a new sprint would begin. At the end of each development sprint a new release would be made and presented personally to the Head of KI.

## Technical challenges

The idea was to keep the practical functionality of a real physical board, because we knew Kaizen Methodologies worked good when the team could get continuously the sense of how they were doing according to what was planned. Besides that we didn't want to lose the practical effect a board has on meetings. We wanted to bring the physical board to distributed teams.

So we figured, why not use those digital boards that are used in schools? Just this time adapted to work for Kaizen Methodologies. Although it would be nice for it to work on whiteboards, this software had to work everywhere, meaning, a person on a train travelling to a certain city, with his phone or tablet can join in the meeting and participate.

Due to these requirements, we knew we had a challenge ahead of us. We used the [Atmosphere framework](https://github.com/Atmosphere/atmosphere) because it would provide an easy interface with WebSockets for our back-end made in [Play! Framework](https://www.playframework.com/) and also our frontend made in JavaScript. With WebSockets we could create real time interaction with the board. Each team member that would join in a meeting would see in real time what all the others were seeing and interact with the meeting also in real time.

{% include figure.html url="/assets/imgs/leanhub/digital-board.jpg" description="The white board flexibility was a must." %}

We wanted to keep the flexibility of a white board but also ally it to the tech world capabilities, meaning automatically calculating workloads, sent smart warning, store everything in a central place allowing for every member of the team to have access to KPI's and data anywhere. So, despite being able to freely draw inside a meeting session in LeanHub, each other action you would make, like assign a task to someone, would actually have repercussions in planed times, workload, etc, and a message would be automatically sent to the person to which the task was assigned, warning him of a new todo task.

## Outsourcing design, not usability

Since we had no designer in our team, we needed to get it from somewhere else. We used [99designs](https://99designs.com) to create online contests according to briefs I used to write.

Even our identity was conceived this way, with a brief that defined our core values the persona we wanted to represent and the target clients we wanted to get.

{% include figure.html url="/assets/imgs/leanhub/logo-contest.png" description="LeanHub's logo was developed using 99designs." %}

For the design of new features, after the definition of our requirements in our Design Sprint, we would send the final mockups to our designer in 99designs and obtain the final designs.

{% include figure.html url="/assets/imgs/leanhub/mockup.jpeg" description="LeanHub's mockup example that was sent to the design team." %}

All our mockup design was made in-house in our design sprints, where we would even test the usability of our proposed new features with real potential clients. Just the "beautification" of the mockups was done as an outsourced service.

## Go to Market

Our first clients were, naturally, clients that had undergoing projects with Kaizen Institute's direct consultancy. New KI clients that were starting projects with them were the most natural target audience to be introduced to LeanHub. The consultant, who is being paid to create change in a company, is the one with the best position to introduce LeanHub to clients as part of the necessary change.

Despite counting mostly with KI to deal with the initial go to market, especially because they already had a name and reputation amongst the most important clients, we also made our move in regards to the go to market strategy.

I figured that if I wanted to target distributed teams, the easiest way to do it would be to go to all the international chambers of commerce here in Portugal. All the affiliate companies connected to these chambers of commerce were naturally already multi-national companies and there was a higher chance that they would feel more the pain of having distributed and remote teams. So I visited the German Chamber of Commerce here in Porto and was really well received, managing to schedule an appointment with Kirchhoff Portugal to go a present them LeanHub. Even being just a Software Developer with no previous know how in the area, I managed to find a way to interact with the right people to get what I needed.

## My exit

After delivering what I promised to KI (the 8 sprints), and even continuing with several extra sprint to better complete the product, it was time for me to go. 

I had finally gotten the necessary investment for SIMI and decided to go back and head this project as it desperately required my attention.

Nonetheless it was a very good experience, to lead and build LeanHub in such a short period of time. Overall it felt like a big win, managing to support the SIMI team with a parallel project that also went really great.

## Ironical paradox

It makes you wonder, when you successfully build a project that actually generates revenue and pays itself just to support another one that doesn't pay itself yet.

I would say that at least it is a very ironical thing. But I guess thats part of the fun of being alive and wanting to make a change.

# Technical Solution

LeanHub is a web application, it only needs a browser to run, even the digital white boards did not need any special kind of software, just a browser to open LeanHub. That said, LeanHub had a back-end in Java (Play! Framework) and a front-end made essentially with Scala.

It's database was in MySQL and there was an index built with Solr that was intended to make the search experience a smooth one.

In regards to the live meeting room where people in different devices and different places could interact, we used WebSockets and the Atmosphere framework that smoothly integrates with Play! Framework and our Scala + JavaScript interface.
