---
title: Meta Partner Reports
permalink: projects/meta_prg/
breadcrumb: Meta Partner Reports
---

![Logo](/assets/imgs/meta/logo.svg){:class="project-logo"}

# What is it?

Its an internal report generation platform that enables all the business verticals technical teams (20+ at the moment of writing this article) to build onto it to quickly generate reports with insights to support the business teams meeting with Meta's partners / clients.

It is only available internally at Meta, so I cannot link it here, and I'll have omit relevant confidential details in order to talk about it here.

## Story that led to Partner Reports

This story starts when I was hired to work for Meta.

In November 2018 I was set on changing country, changing jobs and starting my exciting adventure at one of the [FAANG](https://en.wikipedia.org/wiki/Big_Tech) companies. I couldn't believe at that time that it was really happening to me.

When I joined, I had to go through a 6 weeks bootcamp onboarding process (that was amazing and really well thought off). As part of this process I ended up learning all I needed to relating to the Facebook stack and how to ship code at Meta.

Here are some pictures of my first days in office in London:

{% include figure.html url="/assets/imgs/meta/cafeteria.jpg" description="First lunch at the Meta (then Facebook) Rathbone office in London (November 2018)" %}
{% include figure.html url="/assets/imgs/meta/emojis.jpg" description="Partner Center at the Meta (then Facebook) Brock office in London (November 2018) - this was where I worked on a daily basis" %}

{% include figure.html url="/assets/imgs/meta/insta_background.jpg" description="Instagram office in London" %}

{% include figure.html url="/assets/imgs/meta/instacart.jpg" description="There used to be an Instagram chariot right behind my desk in the London Brock office" %}

{% include figure.html url="/assets/imgs/meta/pingpong.jpg" description="Where we used to play some ping pong" %}

{% include figure.html url="/assets/imgs/meta/work_office.jpg" description="My desk at the London Brock office" %}

After the first couple of weeks, I was flown to Meta HQ (then Facebook) to continue my bootcamp, besides the code stack we also ramped up on the company culture and work style.

Here are some pictures of my first visit to Meta HQ while a bootcamper:

{% include figure.html url="/assets/imgs/meta/entrance.jpg" description="Meta HQ (then facebook) in Menlo Park (December 2018)" %}

{% include figure.html url="/assets/imgs/meta/games_room.jpg" description="Meta HQ (then Facebook) has a games room on the classic campus in Menlo Park (December 2018)" %}

{% include figure.html url="/assets/imgs/meta/hired_for_brain.jpg" description="We biked from building to building at Meta HQ, here is what is says on the inside of the bicycle basket (December 2018)" %}

{% include figure.html url="/assets/imgs/meta/bootcampers.jpg" description="Bootcampers having breakfast at classic campus (used to be the Sun Microsystems HQ before becoming Meta's HQ)" %}

{% include figure.html url="/assets/imgs/meta/meta_hug.jpg" description="As part of onboarding we had to replicate pictures Mark Zuckerberg had taken, this one was on Classic Campus at Meta HQ" %}

{% include figure.html url="/assets/imgs/meta/alcatraz.jpg" description="Alcatraz Island visit while in San Francisco for Bootcamp (December 2018)" %}

{% include figure.html url="/assets/imgs/meta/golden_gate.jpg" description="Quick stop to see the Golden Gate Bridge (December 2018)" %}

{% include figure.html url="/assets/imgs/meta/muir_woods.jpg" description="Visiting the amazing sequoia tree's forest of Muir Woods (December 2018)" %}



I had a very uncommon path up until then: I wasn't the best student at university and I think that because of it I was more prone to risk when I started my professional career. I started as a researcher just to quickly realize I wanted to build things instead. This leads me to building 2 startups and being the first employee of another. 

But this was exactly what Meta was looking for, someone with a strong technical background, demonstrated willing to build things and a business acumen. For the role I was going to embark on this mixture would be crucial. I joined Meta as a "Partner Engineer" - a software engineer that is able to speak with the technical teams of our partners / clients and support them with alpha / beta product launches.

When I joined Meta, it was at a very special time. People where starting to become extremely aware of their privacy and Meta had just undergone the  [Cambridge Analytica Data Scandal](https://en.wikipedia.org/wiki/Facebook%E2%80%93Cambridge_Analytica_data_scandal). 

Before this, people typically didn't care much about their privacy and likewise, Meta didn't invest too much into it as it wasn't a problem people wanted solved. But at this pivotal moment in time, Meta was deeply invested in changing everything towards a privacy first approach for every product they built, and that included all internal systems. Also after the FTC agreement that Meta reached as a consequence of the scandals, implied Meta needed to think much more about user privacy and consent upfront and every step of the way.

Shortly after joining Meta, all internal business employees lost access to all data tools, from one moment to the other - including people who needed to use them on a daily-basis to be able to manually produce slide decks (like quarterly business reviews or QBRs) with insights to have constructive conversations with partners / clients.

So it became a top priority for the company to provide them with the same insights without re-enabling access to these data tools. Having access to these data tools directly and building their own slide decks was prone to human error, and we needed to make sure our insights matched those of our partners / clients and were consistent across reports. Our biggest partners (like Disney) are extremely professional with understanding their usage numbers and engagement numbers, we need to provide insights at the same quality they are used to.

I volunteered to solve this problem, and along with 2 other engineers and my manager, we were the founding team of what was to become the CSDT team - Central Systems and Data Tools team. This team eventually grew and merged with another team to become a 300+ people organization. 

The very first problem we were tasked to tackle led to the development of the Partner Reports platform. 

It felt like working on a startup again, but this time with an incomparable level of impact and a solid wage at the end of the month!

# Deciding to build a new platform

To my surprise, we didn't have already a unified platform to generate business reports automatically.

When we were first tasked to solve this problem we just had to build 2 business reports:
- the Facebook QBR (Quarterly Business Review);
- and the Instagram CPR (Content Performance Review).

The result for these 2 reports needed to be essentially 2 slide decks. Both would include charts / insights and an automatic analysis of the content that was being produced by a certain partner on their Facebook Pages / Instagram Accounts. These reports would have to be produced dynamically, given a certain input (like partner account / facebook page list / instagram account list) they would have to generate a slide deck analysis based on the partner's accounts.


{% include figure.html url="/assets/imgs/meta/qbr.png" description="Illustration of a QBR meeting presentation" %}

Even though we only had 2 reports to build as a top priority as of that moment, we knew the other 20+ business verticals (examples could be the Platform-Partnerships Team, Workplace Team, WhatsApp for Business Team, etc...) would also need to produce similar reports and we were a team of just 3 engineers, we would not be able to scale fast enough to support all the business verticals by making each report itself manually. 
So we focused on building a platform that would instead enable other engineering teams to work on top of and produce business reports as fast as possible.

Before investing in building a completely new platform to generate these reports, we looked to other teams / projects at Meta to find out if anything like this was ever built so that we could leverage it to speed up our goals.

We found a similar project that had started a few time before we looked into the same problem. Our sister team in Sales had decided to build a platform to generate reports that was supported by a team in Hyderabad, India.

We did an in-depth analysis of their platform and decided not to leverage it and instead build a new one from scratch as it had some limitations that were blockers for us:
- it was built outside of our internal network, meaning we would not be able to source insights directly without exporting them outside of intern (security risk for us)
- each template could only be used to generate one report type (their approach didn't allow to dynamically adding / removing slides according to the report)
- the system was designed to scale with their team, as they had an extensive contractor team available to manually produce each new report (instead of leveraging other engineering teams to add reports) - so it wasn't built in a way that other engineers could leverage
- they way they were sourcing data was hardcoded, meaning for each new report an engineer had to code sourcing all the data all over again, even if from the same data sources









# My contribution to Partner Reports

As one of the first 3 volunteers on this project, I took part in defining how it would be setup.
Besides taking part in all major engineering decisions across the board, I ended up originally owning the exporter layer which I will detail further bellow. Throughout the evolution of the project, because I was interacting directly with new teams onboarding onto Partner Reports, I ended up owning all the scope of the project and became the de-facto tech-lead and go-to person for it.

Besides the technical responsibilities, I also detailed a thorough onboarding guide wiki for new teams / developers to use. I then used it to on-board new hires of our own team, to be able to understand which parts were more prone to questions to improve the wiki itself. 
I effectively on-boarded all the new teams working on Partner Reports and studied where teams where investing most of their times, with the intent of optimizing the platform itself. This ended up leading me to develop a new project called Partner Metrics that I talk about [here](https://www.google.com).

{% include figure.html url="/assets/imgs/meta/prg_dinner.jpg" description="Early-days picture of a dinner with the PRG (Partner Reports Generator) team (and friends)" %}

## First technical challenges


## Clients define our roadmap

# Success

At Meta we used to say that headcount was currency. The more people the company would invest in your team, the clearer the signal that your strategy was being successful.

In the first couple of years we grew from 3 to roughly 5 and then we grew exponentially to 40+ engineers.

We got to heavily multiply our team and we became the fastest growing team within the Partnerships Organization because we were successful with the first version and the consequent new reports that kept being added by other software engineering teams.

With this investment we gained a new identity: the CSDT team (Central Systems and Data Tools team). This was the period I most enjoyed while working at Meta, and probably of my whole career up to this point.

## CSDT

As a direct consequence of out inital work (remember: 3 engineers and 1 manager) we were able to start a new Organization called CSDT within Meta (Central Systems and Data Tools team).



# Technical Solution

## Data Layer

## Presentation Layer

## Putting it all together

## Time spent to deliver a new report and follow ups

## Management Tool