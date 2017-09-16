---
title: How Ablator Works
layout: docs
---

{:.lead}
Some features should not be switched on for all your users as soon as they update to a new version of your app.

Maybe they would absolutely **trash** your server if all users accessed them at once after release. Maybe they are untested prototypes. Maybe they are hard to test with conventional quality assurance or unit tests, and you want only a small number of your users to be subjected to them until you are more certain that they work properly.

Maybe your feature is unit-tested, passed quality assurance, and you still want the option to quickly disable it for all your users if an unforeseen problem arises.

Maybe you have two different variations of a feature, and want to use A/B-testing to present a one variation to half of your users, and another variation to the other half. 

For these and more use cases, you can use **feature switching** [^1]. Feature Switching means that your app is asking a server wether to enable a certain feature. 

[^1]: Also called functionality switching, feature toggles, or feature flags.[^2]

The server in this case is Ablator.

A good feature switching server allows you to 
- define when to roll out the feature
- define how quickly to roll out the feature
- quickly revert or pause the rollout
- enable a feature globally once you are sure of its maturity

It is also important that, as long as you don't explicitly tell it to change something, the server always gives the same answer for a specified user. This way, users don't experience features that flash on and off every now and then. 

Ablator give you all of the abilities and more. Here's how you use Ablator together with the app that you are creating:

## Step 1: Define Functionalities in Ablator
In the [Ablator web interface](http://ablator.space/), create a new App, then inside the app create a new Functionality[^2]. On the Functionality overview page, you'll see how many users you have in total, and how many of those have the Functionality switched on.

[^2]: For a variety of reasons, but mostly to distinguish them from features **of** Ablator, features are called *Functionalities* in Ablator.

A Functionality has one or more *Flavors*. Flavors are used to enable A/B-testing in your app using Ablator. If you only want to switch a feature on and off, a single Flavor named "On" (or something similar) is enough.

Once you have defined one or more Functionalities, it's time to include Ablator into your app. 

## Step 2: Integrate Ablator in Your Code
There are a number of libraries available to include Ablator into your code:

- For Python, there's [Karman](https://github.com/ablator/karman)
- For Swift, there's [Shepard](https://github.com/ablator/shepard)
- For NodeJS and TypeScript, there's [Herschel](https://github.com/ablator/herschel)
- You can also just make a simple web request to Ablator's API.

Whichever is the right way for you, once you want to 
----

- include an ablator client in your app
	- define a user string
		- it gets hashed on the server before storing
	- on startup, or periodically, request the list of active features or flavours
	- write your features in a way that you can easily switch them on and off using an `if` or `switch` statement
	- use the `caniuse` or `which` method to detect wether to show the feature or not, and which flavor 
- Roll out and manage your features
	- Select a Roll out Strategy
	- Create or Edit a Release
	- Watch your feature roll out


## Further Reading
- Concepts of Ablator
- Tutorials