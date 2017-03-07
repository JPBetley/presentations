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

