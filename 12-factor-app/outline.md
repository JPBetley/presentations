note: images from 12factor.net

- title page
- opinion warning
	- This is not a presentation of rules. This is a presentation full of opinions. These opinions are guided by the experiences of some smart and experienced people, but are still opinions. Not every project we work on can adhere to all of these items. Some may not even be capable of any. I certainly haven't used them all. In fact there are some that I may disagree with. The goal is to utilize this information to make our jobs easier. Absorb what we'll go over, and apply what's possible to your work where appropriate.
	- Who is this talk for: developers building applications, PMs who want to understand the technical targets for developers, and IT Operation Engineers who manage the applications and infrastructure that run them
- 12 Factor App intro
	- Methodology for building software, most commonly in the form of web apps these days
	- Goal: Raise awareness of systemic problems in app dev, provide shared vocab for discussion, and offer conceptual solutions to those problems

- 1: Codebase
	- img/codebase-deploys.png
	- "One codebase tracked in revision control, many deploys"
	- Here we're saying that everything we work on in relation to an app is in a central version control system.
	- We have the capability to see all the history of the codebase, as well as all the different versions of it (branches)
	- One-to-one correlation between codebase and app
		- If there are multiple codebases, it's a distributed system. Each component may be an app
		- Multiple apps sharing the same code is a violation of twelve-factor. Shared code should be combined into a library that is distributed to the app through a dependency manager
			- Who's developed a module for a site before, and ended up copying it into other sites?
			- Example: we develop a sitecore module that we use in multiple sites. Instead of changes to that module being made in each site individually, they would be made in a central library, and distributed to all the sites. The development of that module should live in the library, not in the site
	- Will be many deploys of the codebase. A deploy is a running instance of the app. Each deploy uses the same codebase, but not necessarily the same version fo that codebase. Production may only run the stable version of the codebase, whereas every developer may be running their own individual versions with the features they are building

- 2: Dependencies
	- "Explicitly declare and isolate dependencies"
	- 

- 3: Config
	- "Store config in the environment"
	- Config varies widely on deploys
		- Connection info for database, services, etc
		- Credentials and keys
	- This config is loaded into the environment variables
		- Example: editing PATH in Windows, or using Java System Properties
	- Good litmus test for whether something should be in an environment:
		- If the codebase was made open source, would any credentials be compromised
		- Does it change depending on the deploy
	- Don't group config like this together as dev, test, prod in the codebase. It does not scale cleanly as each deploy will need an individual config group. 
		Instead, use env vars that live with each individual deploy, not with the codebase.
	- Popular tool to manage this is called dotenv, to load values into environment variables from a text file. A number of languages have versions, including PHP, ruby, python, nodejs, etc.

- 

- 5: Build, Release, Run
	- "Strictly separate build and run stages"
	- Growing Object Oriented Software Guided by Tests (GOOS) talk about the cycle of software development: build, deploy, test. They stress the importance and value of determining each one of these steps as early on in the process as possible. The risks of leaving it to later are too high. Building we ususally got down pretty well. Deploy and test are the lesser focused steps. We usually only care about deploy at the end of the project when we need to hand it over to the customer, or test when we need to customer to tell us it's working. 
	- GOOS talks about starting out with a "Walking Skeleton". Build just enough that we can test, deploy it, and test it. Use this to help formalize this process
	- This factor talks to the "deploy" step that GOOS discusses, and how best to go about that process
