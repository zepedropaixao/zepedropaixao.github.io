---
layout: post
title: Android Lifecycle Overview
breadcrumb: Android Lifecycle
---


{% include figure.html url="../assets/imgs/android-lifecycle.jpg" description="The Android Lifecycle defines the programming paradigm" %}

As I ventured into the Android world as a Developer, one of the first things I had to understand was the lifecycle of an Android App. 

<!-- more -->
It is a big paradigm shift from traditional Java programming. Typically a Java app has a single entry point and everything happens there after in a kind-of sequential manner. An Android App can have multiple entry points, and it can be interrupted by any reason, like a phone call suddenly coming in, a memory manager killing your app when it goes to the background or just because the user wants to open another app from a notification.

This is a new paradigm that implies having in consideration foreground lifecycles. These lifecycles are represented by a set of specific callbacks that will be executed by their classes according to the lifecycle moment it is in, meaning, when an Activity (Android Framework type class with a lifecycle) is instantiated it will go through functions like onStart(), onResume(), onPause(), onStop(), onDestroy() throughout its lifecycle.

## Activities


As a user navigates through, out of, and back to your app, the Activity instances in your app transition through different states in their lifecycle. 

The Activity class provides a number of callbacks that allow the activity to know that a state has changed: that the system is creating, stopping, or resuming an activity, or destroying the process in which the activity resides.


## Fragments

## Between them


## Services

## Between Them


 
