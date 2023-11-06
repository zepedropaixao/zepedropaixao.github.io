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

In November 2018 I was set on changing country, changing jobs and start my exciting adventure and one of the FAANG companies. I couldn't believe at that time that it was really happening to me.

{% include figure.html url="/assets/imgs/meta/entrance.jpg" description="Meta HQ (then facebook) in Menlo Park" %}

I had a very uncommon path up until then: I wasn't the best student at university and I think that because of it I was more prone to risk when I started my professional career. I started as a researcher just to quickly realize I wanted to build things instead. This leads me to building 2 startups and being the first employee of another. 

But this was exactly what Meta was looking for, someone with a strong technical background, demonstrated willing to build things and a business acumen. For the role I was going to embark on this mixture would be crucial. I joined Meta as a "Partner Engineer" - a software engineer that is able to speak with the technical teams of our partners / clients and support them with alpha / beta product launches.

When I joined Meta, it was at a very special time. People where starting to become extremely aware of their privacy and Meta had just undergone the  [Cambridge Analytica Data Scandal](https://en.wikipedia.org/wiki/Facebook%E2%80%93Cambridge_Analytica_data_scandal). 

Before this, people typically didn't care much about their privacy and likewise, Meta didn't invest too much into it as it wasn't a problem people wanted solved. But at this pivotal moment in time, Meta was deeply invested in changing everything towards a privacy first approach for every product they built, and that included all internal systems. Also after the FTC agreement that Meta reached as a consequence of the scandals, implied Meta needed to think much more about user privacy and consent upfront and every step of the way.

Shortly after joining Meta, all internal employees lost access to making queries on their own, from one moment to the other - including business people who needed to make them on a daily-basis to be able to manually produce slide decks (like quarterly business reviews or QBRs) with insights to have constructive convos with partners.

So it became a top priority to provide them with the same insights without allowing them to query our internal systems on their own. Making individual queries was prone to human error, and we needed to make sure our insights matched those of our partners / clients and were consistent across reports. Our biggest partners (like Disney) were extremely professional with understanding their usage numbers and engagement data, we needed to provide insights at the same quality they were used to.

I volunteered to solve this problem, and along with 2 other engineers and my manager, we were the founding team of what was to become the CSDT team - Central Systems and Data Tools team. This team eventually grew and merged with another team to become a 300+ people organization. 

The very first problem we were tasked to tackle led to the development of the Partner Reports platform. 

It felt like working on a startup again, but this time with an incomparable level of impact and  a solid wage at the end of the month!

# Deciding to build a new platform

To my surprise, we didn't have already a unified platform to generate business reports automatically.











# My contribution to Partner Reports

I entered Infraspeak in its early days as a company. Although Luís, our co-founder, had been working to create Infraspeak for some years, it only became a company in the end of 2015. I joined up in April of 2016. I was the second employee, and we were still not invested at the time. The company managed to bootstrap and make money from new sales each month allowing for us to regularly employ new people from that moment on.

I entered Infraspeak with the objective to lead the company in developing its mobile app, which was essential for the business.

I am responsible for the development of all the mobile applications of the company:
- **Infraspeak mobile app** (main application) - aimed for technicians to use it on their daily operations
- **Infraspeak direct app** - aimed for non-maintenance technicians to be able to report failures to the maintenance team
- **Infraspeak operations app** - aimed for stationary technicians that perform maintenance tasks on the same equipments everyday

## First technical challenges

When I got in, an app already existed. This app had been developed by Luís for the past years. It had all the core features already in it. But it was developed over time, while Luís was also learning about Android Development. My first challenge when I got in Infraspeak was to start with this legacy code, convert it to better and more recent best practices, add offline capabilities to the main tasks performed by the app, while keeping the regular releases of new features. We were moving fast, but the challenge was amazing and the team was small but very motivated.

We managed to launch an app version quite fast with a simple offline workflow, where all the tasks that were allowed to be performed offline would wait in a priority queue of offline jobs until the app would have access to the internet to sync all these offline tasks. This was all done without bothering the technician with any offline details, meaning he could operate as he usually did when he had internet, not even noticing he was offline. The tasks would sync as soon as the phone had connectivity again.

This was a major breakthrough as it allowed technicians that worked in basements to do their jobs without any issue.

## Clients define our roadmap

We worked in cycles of 3 weeks, we had a development sprint of 2 weeks and an inter-sprint of one week. 

This inter-sprint was a creation of ours inspired by the [Google Ventures Design Sprint](http://www.gv.com/sprint/) but then again, completely altered for our needs. In this inter-sprint we would re-test everything, do some minor fixes, release the app, plan for the next sprint and it was the week where all the teams interacted with each other. 

As part of the development team, in the inter-sprint we had a designated time to speak with:
- the **customer success team** to understand which were the main necessities of our current clients, 
- the **sales team** to know which were the main requested features that would convert sales leads into clients 
- the **communication team** do give them all the details of the newly developed features for them to communicate
- the **development team** (between ourselves) to identify development needs that could not be communicated but still had to be done at some point

After these interactions between the teams, we negotiated what would be communicated in the next sprint. Marketing defined what we built each sprint, taking in consideration all the voices. But in the end, we always developed focusing on the headlines and minor improvements that were communicable to our current or future clients. 

## Caixa Capital & 500 startups investment

Our communication strategy and product development strategy according to clients real needs worked out really well for us and we were selling really fast and to great names (SIEMENS, Intercontinental, Crown Plaza, Savoy, Four Seasons). 

Besides this, with each big client, a lot of new leads would emerge because of our NFC strategy - all the tags had our name and it was easy for technical assistance providers that visited one of our new clients to wonder what Infraspeak was and bite the bait. In a way we had a bootstrapping strategy that was financing our early team with each new client we made.

We were not looking to be invested.

In LIS (Lisbon Investment Summit) we managed to greatly showcase our success, in such a way that we convinced one of the co-founders of 500 Startups (that was present) to invite us to participate in their 18th batch in San Francisco (which was going to happen 15 days from the moment we were invited). Although we were not looking for investment, we couldn't say no to such a great opportunity and got invested by Caixa Capital and 500 startups for a pre-seed investment and went to San Francisco for 4 months to participate in their acceleration program, which was a great learning opportunity for us.

{% include figure.html url="/assets/imgs/infraspeak/winner-yeoty.jpg" description="Infraspeak's team when we won the Young Entrepreneur of the Year Award by ANJE" %}

## Team spirit

{% include figure.html url="/assets/imgs/infraspeak/team.jpg" description="Infraspeak's team is very united." %}

The team is clearly the best asset of Infraspeak. Infraspeak managed for 2 years in a row to overcome more than 200% in sales growth and evolved from a 3 people team into a 15+ team in those 2 years.

Infraspeak won many award like the Young Entrepreneur of the Year award, the top 25 companies from Portugal (we got a free stand in WebSummit thanks to this award) and many company acceleration program awards (programs that selected companied to become providers of a certain brand). 

{% include figure.html url="/assets/imgs/infraspeak/team-websummit.jpg" description="Infraspeak's team at WebSummit." %}

Infraspeak has a tradition that motivated the whole team to sell more. For each new client we would drink a different beer. This evolved into a ritual called Beer Celebration where we got to rate each of the beers we drank for each client with Infraspeak's app itself. After the ritual was over we would save the beer in our beer showcase.

{% include figure.html url="/assets/imgs/infraspeak/founders.jpg" description="Infraspeak's founders showing off the beer showcase." %}

## 15 minutes of fame (much more than 15 minutes actually :muscle:)

Thanks to getting invested and participating the 500 Startups acceleration program, along with all the big client names and all the awards we won, Infraspeak got a lot of media coverage. Some examples:

 - [Público](https://www.publico.pt/2017/12/06/economia/noticia/um-software-para-edificios-e-a-melhor-ideia-de-negocio-em-2017-1795093)
 - [Diário de Notícias](https://www.dn.pt/lusa/interior/startup-infraspeak-vence-premio-do-jovem-empreendedor-da-anje-8953986.html)
 - [RTP](https://www.rtp.pt/noticias/economia/startup-infraspeak-vence-premio-do-jovem-empreendedor-da-anje_n1043546)
 - [ECO - Economia Online](https://eco.pt/2017/11/29/vila-gale-no-brasil-vao-ter-plataforma-da-infraspeak/)
 - [Dinheiro Vivo](https://www.dinheirovivo.pt/fazedores/infraspeak-entra-no-reino-unido-a-acelerar-manutencao-de-centros-comerciais/)
 - [Observador](http://observador.pt/2017/01/19/infraspeak-como-nasceu-a-startup-do-porto-que-cresceu-243-em-2016/)

 We even got mentioned on the TechCrunch favorite list of the 18th batch of 500 Startups:
 - [TechCrunch favorite list](https://techcrunch.com/gallery/our-favorite-startups-from-500-startups-18th-class/slide/11/)

# Technical Solution

On the technical side, Infraspeak is constituted by a back-end a front-end, a main mobile app used for technicians and two support mobile apps: direct app and operations app.


## Infraspeak Back-Office and Back-End

The back-end is built using PHP (Laravel) and between several other technologies Vue.js is used to built the back-office interface.

{% include figure.html url="/assets/imgs/infraspeak/backoffice.jpg" description="Infraspeak's back-office allows managers to control the whole operation" %}

## Infraspeak Mobile App

The main mobile app is a Native Android app, primarily built with Java. Of the technology stack I could give emphasis to:
- DBFlow - the ORM used,
- EventBus - to fire events making it easy to communicate between background threads and the UI thread
- Android Priority Job Queue - used to simplify background jobs and the order through which they should be executed
- Retrofit - used to make requests to our API

This application is built following the MVP architecture. At some point we used MVVM architecture to simplify the handling of the models in some RecyclerViews.

{% include figure.html url="/assets/imgs/infraspeak/app.jpg" description="Infraspeak's mobile app is used by thousands of technicians every day" %}

## Infraspeak Direct App

This app was built using the ionic framework, which is a framework based on JavaScript and Angular that has many components that look like native mobile components. We then encapsulated this web application into an app for iOS and Android using Cordova.

{% include figure.html url="/assets/imgs/infraspeak/direct.jpg" description="Infraspeak's direct app is focused in allowing non-maintenance technicians to report new failures" %}

## Infraspeak Operations App

This app was built using the Quasar Framework, which is a View.js based framework focused on creating mobile applications, much like ionic but this time based on View.js.

{% include figure.html url="/assets/imgs/infraspeak/operations.jpg" description="Infraspeak's operations app targets stationary technicians" %}