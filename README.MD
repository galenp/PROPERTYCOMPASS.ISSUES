Property Compass Issue Tracking
===

Because the Property Compass platform is distributed across many, many repositories we will use this aggregated repository for internal issue tracking. (For Now)

# Links
 * Property Compass - [App](https://app.propertycompass.com.au)
 * API Docs - [Swagger](http://api-docs.propertycompass.com.au/)
 * Discussion - [Slack](https://landlordcentral.slack.com/messages/propertycompass/)
 * Project Management - [ScrumDo](https://app.scrumdo.com/projects/property-compass/board#/view) 

# How to reference an issue in a commit message?

When committing code to reference an issue use the following:

* `galenp/PROPERTYCOMPASS.ISSUES/<#issuenumber>`

# How to reference a commit from another repository?
The format GitHub users for smart commit linking is:
`https://github.com/<username>/<reponame>/commit/<sha>`

So for linking to commits from various Property Compass repos:

* UI : `https://github.com/galenp/PROPERTYCOMPASS.APP/commit/<sha>`
* Component: `https://github.com/galenp/PC.Component.<Component>/commit/<sha>`
* Platform: `https://github.com/galenp/PC.Platform/commit/<sha>`


# How to label an issue?


#### 1. Select one type: 
	* bug
	* question
	* suggestion

#### 2. Select one priority:
	* low
	* medium
	* high

#### 3. Developer will then respond with a Status
	* confirmed
	* in-progress
	* non-issue
	* wont-fix
	* resolved
	* reopened

# Versioning / Milestones
Property Compass will use Semantic Versioning [http://semver.org/](http://semver.org/) which defines the specific methodology for versioning releases. However due to the component nature of the overall platform each individual component will have its own versioning.

For example:
> * PC.Components.Orders 0.1.0-CI00001
> * PC.Components.Payments 0.1.5-CI0022

This makes an abstract version number for the platform overall a bit difficult since the platform is a collection of versioned components. 

What we'll do is continue to use the semantic versioning system for releases to production based on the PC.Platform repository. This will be the 'public' facing version reference for the system.

For example:
> * PC.Platform 1.0.0 will be what we've internally named 'release 1'

We will then increment the version number based on:
> Patch version Z (x.y.Z | x > 0) MUST be incremented if only backwards compatible bug fixes are introduced. A bug fix is defined as an internal change that fixes incorrect behavior.

> Minor version Y (x.Y.z | x > 0) MUST be incremented if new, backwards compatible functionality is introduced to the public API. It MUST be incremented if any public API functionality is marked as deprecated. It MAY be incremented if substantial new functionality or improvements are introduced within the private code. It MAY include patch level changes. Patch version MUST be reset to 0 when minor version is incremented.

> Major version X (X.y.z | X > 0) MUST be incremented if any backwards incompatible changes are introduced to the public API. It MAY include minor and patch level changes. Patch and minor version MUST be reset to 0 when major version is incremented.

So going by the above :
> * bug fixes to release will that are deployed to the live environment will be PC.Platform 1.0.1, 1.0.2 etc
> * 'release 2' will likely be represented as PC.Platform 1.1.0
