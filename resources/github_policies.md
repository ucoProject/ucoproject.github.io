---
title: GitHub Policies
jumbo_desc:
---

This page describes policies to make stable addresses for software repositories on [https://github.com/ucoProject/](https://github.com/ucoProject/).

Types of repositories on GitHub/ucoProject
----------------------------------------

### Implementation

An Implementation converts tool output to UCO. There is an inherent tie of a UCO Implementation to a specific tool or data format.

Originally, UCO had considered using "Proof of Concept," or "Implementation," for these repositories. On considering a "Development status" annotation for each repository, "Proof of Concept" no longer seemed worthwhile, as it could cause a repository rename if a proof of concept would gain sufficient interest.

### Utility

An intermediary tool not necessarily meant for end users, instead meant for adopting developers or intermediate workflow steps. A Utility is not tied to any particular tool, as that would be an Implementation. Framework tools would typically be Utilities.

### Bindings

Bindings provide support for generating UCO data for a programming language, not necessarily tied to any particular consumer tool.

NOTE - UCO does not use the term "API" here on account of "API" being overloaded, appearing in several usage situations for UCO. For instance, ontologies have an API, over REST. Some parties also consider providing a REST endpoint to be providing an API. "Bindings" is generally understood to be more scoped to just programming languages.

When does a repository go under github/ucoProject?
------------------------------------------------

Either a code repository is hosted under ucoProject, or would be hosted by a community member.

Hosting under ucoProject:

-   There is an expectation that community members may participate in evolving the code.

-   To ease community-based maintenance and reduce decision points, the "Support requirements" section will be followed.

Hosting under the community member:

-   The organization expects to maintain the code themselves.

Support requirements of code repositories on github/ucoProject
------------------------------------------------------------

These are graded support requirements, aligning with the repository's Development Status.

### Development Statuses

We have observed a software packaging ecosystem, Pypi, designate the Development Status of a project with these levels:

1 - Planning\
2 - Pre-Alpha\
3 - Alpha\
4 - Beta\
5 - Production/Stable\
6 - Mature\
7 - Inactive

UCO recommends adoption of these statuses for any repository hosted on github/ucoProject, by specifying requirements to consider a repository having met a support level.

### Support requirements once a project reaches a development status

#### 3 - Alpha

-   Designation of versions of UCO and UCO the project supports.

-   Follow Semantic Versioning (SEMVER).

#### 4 - Beta

-   Tests are implemented to confirm conformance with the specified versions of UCO and UCO.

#### 5 - Production/Stable

-   Continuous Integration testing is implemented and reported for the main branch in the repository's README.

-   Branches are managed with the Gitflow branching policy.
