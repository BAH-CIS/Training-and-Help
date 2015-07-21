---
layout: base
title: "Guidance on software versioning"
exclude_from_search: false
---

# Guidance on Software Versioning

This document will define how we version our software and make the case for continual attention to quality 
(as opposed to prior-to-release "gates").

## Versioning

We version our software based on the effect changes have on **consumers** of the software


# Software Versioning and Version-Change Events

Here, I'll answer the question "What should happen when a version number increases?"

Let's start with "Quality".

## Quality

> "Any philosophic explanation of Quality is going to be both false and true precisely because it is a philosophic explanation. 
> The process of philosophic explanation is an analytic process, a process of breaking something down into subjects and predicates. 
> What I mean (and everybody else means) by the word 'quality' cannot be broken down into subjects and predicates. 
> This is not because Quality is so mysterious but because Quality is so simple, immediate and direct." 
> -- [Robert Pirsig](http://en.wikipedia.org/wiki/Software_quality), *Zen and the Art of Motorcycle Maintenance*


High-quality software tends to manifest these properties:
 
 - meets all requirements for which the software is designed
 - resilience / fault-tolerance in production
 - idiomatic, readable, and maintainable by the team
 - thwarts attacks against unwanted data exposure and systems access (privacy, information security, etc)
 - testable, and tested
 
That is to say, software that demonstrates more of these traits is more likely to be higher quality than software that demonstrates fewer.

Software that is beautiful to behold and highly readable, but which leaks user information or is vulnerable to 
[Little Bobby Tables](http://xkcd.com/327/), cannot be considered high quality.

Likewise, an impenetrable fortress of code that is inscrutable and unmaintainable by reasonably skilled team members
cannot be considered high quality, in that future attempts to modify the software will be more likely to introduce defect.

## Guiding Principles

 - We seek a very high level of quality for our software
 - We seek to release more frequently, not less. Each team decides its release cadence. 
 - Special, more rigorous, end-of-version, blocking "events" are an anti-pattern: if it's worth doing, it's worth doing early and continuously
 - If something is painful to do, do it more frequently
 - Every pull request is an opportunity for improvement, learning, collaboration, and praise
 

## Agile Team Practices

 - Thoughtful, collaborative code review should happen through pair programming and/or pull requests
 - Merging a pull request without commentary is an anti-pattern
 - A team's "Definition of Done" for a feature must adhere to the definition of quality, above
 - We apply "systems thinking"... we think about all the environments in which our software will live,
   and the "Definition of Done" encompasses the safety and soundness of that software in its operating environments
 - Every team member is responsible for quality
 - The product owner, in collaboration with the team, decides when something ships.
 - "Scope" of a code review does not depend on a version number: it is simply a function of how much code has changed
 - Teams are encouraged to build in practices that incentivize high quality, such as Bug Days, Test Days, README Rot Days,
   vulnerability bounties, and the like
 - Teams should avail themselves of local experts (Lamin, CM, etc) and training opportunities (Dev team Hack Lab, eg)
 - Teams must take care to identify parts of the system where they always want multiple sets of eyes 
   (for example, authentication mechanisms). This is an exercise in risk classification.

## Developer Habits

 - We are mindful of quality as outlined above, and not just idiomatic code that satisfies feature requirements
 - Before submitting a pull request, we follow our [pull request guidance](git-pull-requests.html)
 - When reviewing a pull request, we follow the same guidance
 - When working on a known potentially risky part of an application, developers are responsible for consulting with 
   subject matter experts

## Automation Aspirations

 - We write unit, integration, load, and functional tests that exercise the software for correctness, 
   resilience, safety, and security
 - We use commit hooks to scan our commits for vulnerabilities, using tools such as 
   [Clouseau](https://github.com/virtix/clouseau#running-as-a-post-commit-hook), both during development
   and as part of git commits and/or pushes
 - We use tools such as Checkmarx and [Django SCA](https://bitbucket.org/jsthyer/djangosca) to do constant static analysis and 
   generate reports that surface potential vulnerabilities
 - We use tools such as Nessus, where appropriate, to do web-based penetration testing to ferret out end-user
 attack vulnerabilities such as XSS, SQL Injection, XSRF, and the like
 - Our code lives in well-known places (github.com/cfpb and github.cfpb.gov), and any member of any team is always
 free to inspect our code in whatever manner they deem fit

