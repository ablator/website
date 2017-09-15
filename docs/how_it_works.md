---
title: How Ablator Works
layout: docs
---

{:.lead}
A not so quick overview that goes into depth at times. 

- some features should be switched
	- because they are untested or hard to test
	- because only certain user groups – QA testers, clients, etc – should get them 
	- because they threaten to overwhelm your servers
- define these features in ablator
	- short intro to functionalities
	- short into to flavours
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