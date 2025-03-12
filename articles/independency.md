# Independency

Clifford Carnmo, March 2025

## Background

The zeitgeist of modern software development is mostly about relying on internet strangers and distant communities to provide building blocks for you to add business logic to and call it a day. By adding these layers upon layers of code, libraries, and packages, we generate a complex hierarchy of dependencies that makes your code vulnerable, less performant, and incomprehensible. One dependency brings in two dependencies that bring in twelve, and so on. For each of these dependencies, you have to rely on real people to maintain, secure, and keep them updated. You rely on them being reasonably sane, stable, and that they take software development seriously, since they now live inside your codebase and their behavior and actions can instantly reflect on you and your codebase.

## The Problem

People are volatile by nature and easily distracted by **The New Thing&trade;**. People are also lazy, sometimes ignorant, and often could not care less about the quality and security of the codebase they hammer away at during office hours. A simple Node.js frontend project with a web form and a few buttons has hundreds of dependencies out of the box. These are created and maintained by people, and we need to rely on them. A single rogue action by one of these random people on the internet can have catastrophic consequences for you and your organization.

### Enter politics, cultural movements, social engineering, impersonation, and typosquatting

* https://github.blog/security/vulnerability-research/security-alert-social-engineering-campaign-targets-technology-industry-employees/
* https://blog.phylum.io/the-great-npm-garbage-patch/
* https://www.securityweek.com/hundreds-download-malicious-npm-package-capable-of-delivering-rootkit/
* https://www.securityweek.com/dozens-of-malicious-npm-packages-steal-user-system-data/
* https://www.reversinglabs.com/blog/r77-rootkit-typosquatting-npm-threat-research

### Security risks

For every added dependency, you expose yourself to potential security risks. Every change from every dependency that you pull in while updating your dependencies can introduce new security risks, and it's not humanly feasible to study them all in order to make sure that your codebase is secure. You would effectively be spending more time reading the code of dependencies than writing your own code.

## A possible solution

* Minimize the number of dependencies to an absolute minimum.
* Do not use closed-source dependencies.
* Ask yourself if you really need a dependency to achieve that simple thing you could easily write yourself.
* Do not blindly pull in dependencies without understanding the consequences.
* Research the developers and communities behind dependencies.
	* Do they seem reasonable?
	* What are their activity and commit history like?
	* Are they politically or ideologically loud?

## Also

If you do use a dependency that is actually useful to you (there are great ones out there!), involve yourself in the community and be a positive part of the development process. This benefits the whole ecosystem.