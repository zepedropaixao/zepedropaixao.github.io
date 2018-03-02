---
title: OntoExtract
permalink: projects/ontoextract/
breadcrumb: OntoExtract
---

![Logo](/assets/imgs/ontoextract/logo.png){:class="project-logo-oe"}

# What is it?

OntoExtract is a system that automatically collects biographical data on the web for public personalities.


It was developed within the scope of my Master of Science Dissertation project.

## Abstract

In the last decades we have been living in an era of ever-growing information. With the evolution of information technologies and communication, the human being has been generating more and more data and, likewise, is being overloaded with ever more data.

Given that 80% of the available information in the world is in text format, it makes sense to try to extract the information that matters to us by performing effective searches in these sets.

To provide search engines or any other system that uses information in text format with the ability to understand synonyms of public entities, first we need a new system able to acquire the relations between persons and roles / ergonyms. Person’s roles / ergonyms can be seen as synonyms or words that refer to the same entity.

This thesis is focused in providing machines with the ability to understand relations between names and their respective professions / jobs / occupations. This was accomplished by building a prototype that can accomplish the collection of biographical data on the web for public personalities in a semi-automatic way.

Similar projects like Freebase preform this task through manual introduction of information as a community based effort. In our case, the main motivation for a semi-automatic system is due to the fact that we do not have the community nor the resources that these projects have. To implement a similar system for the Portuguese language, a semi-automatic system is needed because a totally manual system is unviable due to the lack of possible users.

The new system has three main components: a database where all relations and entity information are stored; an automatic information extraction system able to extract new relations along with the entity names and their binding roles; and a graphical user interface that allows the manual validation of information by an human operator. Additionally a biographical information retrieval system needs to acquire extra information like article abstracts from wikipedia, article links and photos.

Having the complete system specification, a prototype was developed with codename OntoExtract.

To evaluate OntoExtract, several tests took place. For these tests 30 persons volunteered and actively participated in them. All testers were able to accomplish the validations, and the results of their validations revealed that the main objective, acquiring person-role relations, was well accomplished with accuracy levels greater than 80%.

The developed work allowed us to conclude that OntoExtract implements most of the features and stands as a functional prototype that validates the proposed solution for the problem raised, which was of being able to, in a semi-automatic way, obtain biographical information for public entities.


# Technical Solution

OntoExtract is a set of Perl scripts that use patterns to extract automatically roles, people and organizations names and nicknames and stores all this extracted information in a MySQL database.

Some perl information retrieval scripts are then executed to enrich the information we have about each entity with photos and abstracts.

The OntoExtract interface for information validation was built with the [Catalyst Framework](http://www.catalystframework.org/), which is an MVC framework built in Perl.

You can find the source code for this project in this [GitHub repository](https://github.com/zepedropaixao/ontoextract).

{% include youtube.html url="https://www.youtube.com/embed/RU4R7TLzSRc?rel=0" description="OntoExtract's usage demonstration after parsing millions of news" %}

# Lampert Academic Publishing (LAP) Paperback Publication

My Master Thesis went very well and thanks to it, I stayed working at Sapo Labs right after finishing my course. 

[LAP Publisher](https://www.lap-publishing.com/), at the time, was scouting for the best thesis at my university. They contacted me showing their interest in publishing mine. I accepted and the final result is this book:

Automatic Extraction of Biographical Data :

- **Description**: In recent years there has been increasingly the need to take data, organise it and turn it into information. Given that 80% of the available information in the world is in text format, it makes sense to try to extract the information that matters to us. To be able to extract this type of information with quality from a text, it is necessary, first of all, to structure and organise it. To provide search engines or any other system with the ability to understand synonyms of public entities, first we need to be able to acquire the relations between persons and roles/jobs. We created a system that is composed by an automatic information extraction system able to extract new relations along with the entity names and their binding roles; a graphical user interface that allows the manual validation; and a biographical information retrieval system to acquire extra information like article abstracts from wikipedia, article links and photos. Human-validation tests were performed and the results revealed that the main objective, acquiring person-role relations, was well accomplished with accuracy levels greater than 80%.
- **Paperback**: 140 pages
- **Publisher**: LAP LAMBERT Academic Publishing (August 15, 2012)
- **Language**: English
- **ISBN-10**: 3659215740
- **ISBN-13**: 978-3659215742
- **Amazon link**: [Amazon link](https://www.amazon.com/Automatic-Extraction-of-Biographical-Data/dp/3659215740)


{% include figure.html url="/assets/imgs/ontoextract/book.png" description="OntoExtract's gave origin to a book that is published on Amazon" %}
