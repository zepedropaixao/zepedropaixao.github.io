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

{% include figure.html url="/assets/imgs/meta/pingpong.jpg" description="Where I used to play some ping pong" %}

{% include figure.html url="/assets/imgs/meta/work_office.jpg" description="My desk at the London Brock office" %}

After the first couple of weeks, I was flown to Meta HQ (then Facebook) to continue my bootcamp, besides the code stack I also ramped up on the company culture and work style.

Here are some pictures of my first visit to Meta HQ while a bootcamper:

{% include figure.html url="/assets/imgs/meta/entrance.jpg" description="Meta HQ (then facebook) in Menlo Park (December 2018)" %}

{% include figure.html url="/assets/imgs/meta/games_room.jpg" description="Meta HQ (then Facebook) has a games room on the classic campus in Menlo Park (December 2018)" %}

{% include figure.html url="/assets/imgs/meta/hired_for_brain.jpg" description="Biking from building to building at Meta HQ, here is what it says on the inside of the bicycle basket (December 2018)" %}

{% include figure.html url="/assets/imgs/meta/bootcampers.jpg" description="Bootcampers having breakfast at classic campus (used to be the Sun Microsystems HQ before becoming Meta's HQ)" %}

{% include figure.html url="/assets/imgs/meta/meta_hug.jpg" description="As part of onboarding I had to replicate pictures Mark Zuckerberg had taken, this one was on Classic Campus at Meta HQ" %}

{% include figure.html url="/assets/imgs/meta/alcatraz.jpg" description="Alcatraz Island visit while in San Francisco for Bootcamp (December 2018)" %}

{% include figure.html url="/assets/imgs/meta/golden_gate.jpg" description="Quick stop to see the Golden Gate Bridge (December 2018)" %}

{% include figure.html url="/assets/imgs/meta/muir_woods.jpg" description="Visiting the amazing sequoia tree's forest of Muir Woods (December 2018)" %}



I had a very uncommon path up until then: I wasn't the best student at university and I think that because of it I was more prone to risk when I started my professional career. I started as a researcher just to quickly realize I wanted to build things instead. This leads me to building 2 startups and being the first employee of another. 

But this was exactly what Meta was looking for, someone with a strong technical background, demonstrated willing to build things and a business acumen. For the role I was going to embark on this mixture would be crucial. I joined Meta as a "Partner Engineer" - a software engineer that is able to speak with the technical teams of our partners / clients and support them with alpha / beta product launches.

When I joined Meta, it was at a very special time. People where starting to become extremely aware of their privacy and Meta had just undergone the  [Cambridge Analytica Data Scandal](https://en.wikipedia.org/wiki/Facebook%E2%80%93Cambridge_Analytica_data_scandal). 

Before this, people typically didn't care much about their privacy and likewise, Meta didn't invest too much into it as it wasn't a problem people wanted solved. But at this pivotal moment in time, Meta was deeply invested in changing everything towards a privacy first approach for every product they built, and that included all internal systems. Also after the [FTC agreement](https://about.fb.com/news/2020/04/final-ftc-agreement/) that Meta reached as a consequence of the scandals, implied Meta needed to think much more about user privacy and consent upfront and every step of the way.

Shortly after joining Meta, due to this FTC agreement, it suddenly became a top priority for the company to provide insights in a privacy aware and secure way consistently to all business colleagues. We needed to make sure our insights matched those of our partners / clients and were consistent across reports. Our biggest partners (like Disney) are extremely professional with understanding their usage numbers and engagement numbers, we needed to provide insights at the same quality they are used to.

I volunteered to solve this problem, and along with 2 other engineers and my manager, we were the founding team of what was to become the CSDT team - Central Systems and Data Tools team. This team eventually grew and merged with another team to become a 300+ people organization. 

The very first problem I tackled led to the development of the Partner Reports platform. 

It felt like working on a startup again, but this time with an incomparable level of impact and a solid wage at the end of the month!

# Deciding to build a new platform

To my surprise, the company didn't have already a unified platform to generate business reports automatically.

When we were first tasked to solve this problem we just had to build 2 business reports:
- the Facebook QBR (Quarterly Business Review);
- and the Instagram CPR (Content Performance Review).

The result for these 2 reports needed to be essentially 2 slide decks. Both would include charts / insights and an automatic analysis of the content that was being produced by a certain partner on their Facebook Pages / Instagram Accounts. These reports would have to be produced dynamically, given a certain input (like partner account / facebook page list / instagram account list) they would have to generate a slide deck analysis based on the partner's accounts.


{% include figure.html url="/assets/imgs/meta/qbr.png" description="Illustration of a QBR meeting presentation" %}

Even though I only had 2 reports to build as a top priority as of that moment, I knew the other 20+ business verticals (examples could be the Platform-Partnerships Team, Workplace Team, WhatsApp for Business Team, etc...) would also need to produce similar reports and we were a team of just 3 engineers, we would not be able to scale fast enough to support all the business verticals by implementing each report manually. 
So I focused on building a platform that would instead enable other engineering teams to work on top of and produce business reports as fast as possible.

Before investing in building a completely new platform to generate these reports, we looked to other teams / projects at Meta to find out if anything like this was ever built so that we could leverage it to speed up our goals.

We found a similar project that had started some time before us tackling the same problem. Our sister team in Sales had decided to build a platform to generate reports that was supported by a team in Hyderabad, India.

We did an in-depth analysis of their platform and decided not to leverage it and instead build a new one from scratch as it had some limitations that were blockers for us:
- it was built outside of our internal network, meaning we would not be able to source insights directly without exporting them outside of intern (security risk for us)
- each template could only be used to generate one report type (their approach didn't allow to dynamically adding / removing slides according to the report)
- the system was designed to scale with their team, as they had an extensive contractor team available to manually produce each new report (instead of leveraging other internal engineering teams to add reports) - so it wasn't built in a way that other engineers could leverage
- the way they were sourcing data was hardcoded, meaning for each new report an engineer had to code sourcing all the data all over again, even if from the same data sources

We wanted to build a platform system that:
- would enable us to scale by leveraging other teams work (business engineering teams adding reports)
- would enable everyone to avoid repeating the same work all over again (templates and "data providers" that are reusable in other reports)
- that would live in our internal network so we could source internal data sources directly without externalizing any data

This is how Partner Reports was born.

# My contribution to Partner Reports

As one of the first 3 volunteers on this project, I got to help define how it would be setup.
Besides taking part in all major engineering decisions across the board, I ended up originally owning the exporter layer which I will detail further bellow. Throughout the evolution of the project, because I was interacting directly with new teams onboarding onto Partner Reports, I ended up owning all the scope of the project and became the de-facto tech-lead and go-to person for it.

Besides the technical responsibilities, I also detailed a thorough onboarding guide wiki for new teams / developers to use. I then used it to on-board new hires of our own team, to be able to understand which parts were more prone to questions to improve the wiki itself. 
I effectively on-boarded all the new teams working on Partner Reports and studied where teams where investing most of their times, with the intent of optimizing the platform itself. This ended up leading me to develop a new project called Partner Metrics that I talk about [here](https://www.google.com).

{% include figure.html url="/assets/imgs/meta/prg_dinner.jpg" description="Early-days picture of a dinner with the PRG (Partner Reports Generator) team (and friends)" %}

## Clients / Users define our roadmap

I worked right next to the business people that belonged to the partnerships organization in the London Brock Street office. I was literally sitting right next to the people that were our target using the first 2 reports that we were developing (the Facebook QBR and the Instagram CPR).

This was great as it enabled us to test and iterate quickly with our first 2 reports.

Having no middle layer between us and our users proved extremely useful to attain market-fit at record speed.

We had a great fit and because we involved these people in building these reports, they became champions for our platform with other teams across the company globally.

# Technical Solution

At this point we were just 3 engineers and each one took part in developing one of the layers:
- Data Layer
- Aggregation Layer (later deprecated)
- Export Layer

I quickly understood that the Aggregation layer was a counter productive layer.

If we source data in a standardized way, it should the data providers getting all data, in a consistent format, given a certain input. The data providers aggregate data the way they need according to the input (with time aggregations that are convenient and filters / breakdowns according to the use case).

So I'll focus on these 2 layers, Data Layer and Export Layer. Each report also had an orchestrator class to join all these data providers with their respective output layers.

All of these layers and capabilities had to be tackled from scratch so I ended up having to deal with a lot of issues.

## Data Layer

The whole data layer later evolved into a new product that I called Partner Metrics that standardized data sourcing across the sales organization and overall company internal needs.

But the base premise that led to its existence was: as a company we need a consistent way to source data and reuse the code we write for any number of reports we may need to produce as a lot of these metrics were being reused in other reports, just with a slightly different take or breakdown for a different analysis.

With that in mind we created originally something we called "Data Providers" that needed to spit out data in a consistent format. This consistent format enabled us to specify a "language" that was common so the data providers could send data to different reports or slides consistently.

With this consistent output we were able to add a bunch of automation on top.

Some of the automation we ended up working on are: the charting framework (which I talk more about below) and the data-quality health checks - these tests were crucial to assert the quality of our metrics at all times. 

These tests worked somewhat like this:
1. Create a sample output for a data provider with a given input (time frame, time aggregation, breakdown and filter)
2. Store it in a safe internal JSON format
3. Periodically (chronos job) run a job to assert that the output was still consistent

This would at least help us catch immediately if a metric changed for a given past period - which should never happen.

## Export Layer

The export layer was built in a way that enabled us to ignore the actual export file / type. I developed a language and an internal framework to render slide decks (PowerPoint) that developers could leverage, but they didn't have to, I developed other export types (like CSV transformers, JSON encoders, etc) that would enable developers to export data in different formats.



### Charts

I also had to develop ways to generate plots / charts that would illustrate business insights in a safe manner. I opted for generating pictures that were then embedded into the PowerPoint decks instead of generating native charts so this way I could avoid sharing the raw data with any partner / client. That enabled us to also enforce a narrative without enabling business people to change the chart and content of it.


### PPTX Export

I developed a complete language to specify a powerpoint deck slide. Essentially, with code, developers using our framework were able to specify a new text box inside a slide by passing X,Y coordinates and a text along with text transformations (like bold, italic, underline) and font configurations (like font, size, color, etc). I also added the capability to embed pictures in a slide and scale / place them wherever they were needed using just code.

Developers could also easily add new PowerPoint templates and use them across different reports that would share the same look and feel (like the Facebook or Instagram default templates).

This was probably the most used type of export.


### Video Report

Because of the export layer's flexibility, I developed a Video Report using a technology called React Media (developed internally). This technology enabled us to code videos and render them live in react. 

I initially built it in a hackathon with [Pauli Ojala](https://github.com/pojala) (thanks Pauli for being so keen in making this happen!) - the original idea was to produce reports similar to the Spotify Year in review report - video reports that could have different endings according to the insights of each partner / client. 

I ended up using this video report technology on a real MCD (partnerships organization team responsible for smaller creators that do not have a dedicated account manager) Marketing campaign, reaching 150K+ creators with it in app (Facebook app) attaining never seen before engagement (comparing to the typical email campaign that most creators just dismiss).


## Privacy and Security Compliance

We leveraged internal infrastructure which was great to enable us to easily be compliant in terms of privacy and security. Between other considerations, as an example all the generated reports had a time to live in our blob storages, automatically deleting after a certain period. Also, for example, we could only generate reports for entities that were effectively enrolled in our Partnerships / Sales programs.

## Putting it all together

As mentioned before, because the Data Layer was responsible for delivering data in a consistent output format agnostic from its UI usage, and the Export Layer was supposed to be able to render a PPTX slide deck from a configuration, we needed an orchestrator class to put all of these data pulls and render configurations into one place.

This was the responsibility of the orchestrator class, which was just: pulling data and then sending it to chart generation utils and pushing them to the final slide with the proper narrative and context in text / pictures around it.


## From Hardcoded to Configuration Based

After we had this technology up and running for the first reports, we started having many teams adding their own reports onto it.

Originally each report had to add their own entry to the list of reports manually for this to work. After a while we "entified" the whole configuration ("entified" is a term we used internally to represent creating entities, or modelling them as objects that would store the configurations needed, instead of coding them in a hardcoded list). Once the whole configuration was modeled and we migrated the existing reports into it, we were able to provide much better insights and controls to each report type.

## Management Tool

Once we moved everything from a hardcoded configuration into a model we were able to build an internal back-office for developers to manage their reports. Along side normal day-to-day management features, like disabling the report or changing its name of Point of Contact, we also enabled some debugging features (where we gave visibility of failed reports for report admins) and also some insights for performance tracking.

## Time spent to deliver a new report and follow ups

By onboarding the first developer teams into Partner Reports, I took notice of what task was taking the longest to overcome when adding a new report. I quickly realized that developers were using more than 80% of their time figuring out the data layer part.

So I decided to figure out a way to cut development time of new reports on our platform, by focusing on improving the data sourcing problem.
Data at Meta is broken in many different data platforms, that exist for different purposes.

* Some data platforms are slower to query and have less daily shards available, but because they were built for data analysis they enable complex joins of data a lot of inferences can be made from these data structures at the cost of speed. These metrics were called "offline metrics" as they were typically for internal work and not for consumers to have access to.
* Some other data structures and APIs were much faster, enabled longer time bucket comparisons but because they were built to power some consumer based insights surfaces (like Instagram in-app insights panel for creators) they didn't allow for complex joins or any new inferences in the data as they tended to be already consolidated metrics ready for consumption and already externalized (went through thorough reviews before being made available). These metric were called internally as "online metrics" as they were typically available to creators / clients / partners. When building reports that were meant to be shared with clients / partners we needed to make sure our data matched the metrics our clients already had access to.

Taking all these systems into consideration it was obvious then that I needed to build a middle layer that would unify all these different data formats under a consistent output format so I could scale new reports being added to the reporting platform:

This is how Partner Metrics came to be, I talk about that project on another article [here]{www.google.com}.


# Success

At Meta we used to say that headcount was currency. The more people the company would invest in your team, the clearer the signal that your strategy was being successful.

In the first couple of years we grew from 3 to roughly 5 and then we grew exponentially to 40+ engineers.

We got to heavily multiply our team and we became the fastest growing team within the Partnerships Organization because we were successful with the first version and the consequent new reports that kept being added by other software engineering teams.

With this investment we gained a new identity: the CSDT team (Central Systems and Data Tools team). This was the period I most enjoyed while working at Meta, and probably of my whole career up to this point.

## Numbers

We ended up having 16+ different teams add their own reports to the Platform and once we release Live Reports (which I'll talk about in another article) we ended up having hundreds of reports leveraging this same technology.

Overall, when writing this article this technology had already been responsible for an estimated $75M+ savings calculated given the time we saved our users from having to produce these reports manually as before.

## CSDT

As a direct consequence of out initial work (remember: 3 engineers and 1 manager) we were able to start a new Organization called CSDT within Meta (Central Systems and Data Tools team).



{% include figure.html url="/assets/imgs/meta/csdt.jpg" description="CSDT team swag backpack" %}





