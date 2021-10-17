# General Troubleshooting / Debugging
New to system:
* Delineate all versions and purposes of all related packages
* Isolate and reproduce
* Carefully read each sentence of documentation for gotchas
* Consider alternatives rather than rabbit hole
* Update all systems at once o avoid compatibility circles
* Does this affect the entire system?
* What can be removed to disable the issue?
	* Can you remove another package and disable that way? Perhaps the feature depends on both.
* Consider a higher level system, such as the framework at play - it may have an example to build from in isolation
* Are 2 packages being used together? Google their unique integration issues
* Rather than take an approach and solve problems within it, consider attacking the largest definition of the problem differently

Debugging (#department/development/debugging):
* Did you recently restructure the code?
* Update permissions
* Remove parts 1 at a time to narrow problem
* Break points (view all variable states at any time during execution) (RN: [https://nuclide.io/](https://nuclide.io/) )
* Try/catch call stack careful examination
* Enable Dev Mode and make sure errors are enabled
* Work from bottom up rather than top down
* 

Node (#department/development/backend/node):

PHP (#department/development/backend/php:

Front-End (#department/development/frontend:

Troubleshooting (#department/development/debugging:
* Follow standard methods / processes (unique for different languages)
* See the Snippets Notebook

* Pinpoint problems source (unique for blocking vs non-blocking languages)
* Test simpler version of problematic item
* Double check for syntax errors which may not be revealed
* Employ a workable debugging solution
* Check all available logs
* Enable error display (in blocking languages)
* Use console logs and var dumps
* Use breakpoints and PHP tools
* Follow stack traces with a keen eye
* Google items sooner for quick background info
* Quarantine the Library or Addition giving issues to see if the environment is the issue

![](General%20Troubleshooting%20%20Debugging/Screen%20Shot%202018-01-31%20at%202.25.15%20PM.png)
