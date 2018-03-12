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

Activities are a single focused thing a user will do. Because of this, activities normally implement some sort of UI - through the method setContentView(layout) you can inflate your XML layout to the view.

As a user navigates through, out of, and back to your app, the Activity instances in your app transition through different states in their lifecycle. 

The Activity class provides a number of callbacks that allow the activity to know that a state has changed: that the system is creating, stopping, or resuming an activity, or destroying the process in which the activity resides.



{% include figure.html url="../assets/imgs/activity-lifecycle.png" description="Activity Lifecycle - source: developer.android.com" %}

All the lifecycle callbacks are shown in the following code excerpt. All of these are hooks that you can override to do appropriate work when the activity changes state. Normally we do not override all of them, only the ones we really need for our use cases. You should make sure though that you save all the necessary information to rebuild your view when you do onPause() or onStop(). Meaning, you need to persist your ids or whatever information you need to ask your repository and rebuild your view on configuration changes (when you rotate screen for example).

``` kotlin

open class BaseActivity : AppCompatActivity() {
     fun onCreate(savedInstanceState: Bundle?);

     fun onStart();

     fun onRestart();

     fun onResume();

     fun onPause();

     fun onStop();

     fun onDestroy();
 }

```

Fot the purposes of this blog, all Android code samples will be in kotlin.
An example implementation of a very simple Activity could be as follows:

``` kotlin

class UserDetailActivity : BaseActivity() {

    private lateinit var userId: Long
    private lateinit var binding: ActivityUserDetailBinding

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)

        // Databinding related inits
        binding = DataBindingUtil.setContentView(this, R.layout.activity_user_detail)
        binding.setLifecycleOwner(this)
        supportActionBar!!.setDisplayHomeAsUpEnabled(true)

        // Get user from intent
        userId = intent.getLongExtra("user_id", 1)

        getUser(userId)
    }

    private fun getUser(userId: Long) {
        binding.model = getUserWithId(userId)
        binding.executePendingBindings()
    }

}

```


## Fragments

To better modularize our code and to build more sophisticated user interfaces for larger screens we make use of the Fragment class. A Fragment represents a behavior or a portion of user interface in an Activity. 

A Fragment has a lifecycle of its own, but ultimately always respects the parent Activity's lifecycle. Meaning, when the activity pauses, all its fragments pause also, when the activity resumes all its fragments resume also. Likewise when the activity is destroyed, all its fragments are destroyed as well. 

But this doesn't necessarily mean that when a fragment is destroyed, the activity is also destroyed. Fragments can also be instantiated later in the lifecycle of the activity.


{% include figure.html url="../assets/imgs/fragment-lifecycle.png" description="Fragment Lifecycle - source: developer.android.com" %}



## Between them


## Services

## Between Them


 
