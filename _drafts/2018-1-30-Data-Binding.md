---
layout: post
title: Android Data Binding Overview
---

<!-- more -->

## How to set it up

## How to use it

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

## Data-binding in RecyclerViews







 
