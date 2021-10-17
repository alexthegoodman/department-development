# Code Review Procedure
**Primary Concerns:**
* Everything works
* Thorough testing (testing negatives, coverage %, etc etc)
* Quality Assurance items (relevant lists)

**Secondary Concerns:**
* Formatting
	* Organization
	* Reusable and DRY
	* Clean
	* Precise names (UseCtrl < ThisUseHereCtrl)
* Quality Assurance
	* Pixel perfection
	* Check all relevant checklists
* Code Smells (violations of Principles)
	* Common Smells:  [Code smell - Wikiwand](https://www.wikiwand.com/en/Code_smell#/Common_code_smells)  (ex. Large classes, Large functions)
	* Error handling
* Smart conventions and alternatives
* Check SOLID
	* Check [How to apply SOLID principles in React applications](https://blog.usejournal.com/how-to-apply-solid-principles-in-react-applications-6c964091a982)
	* Principles
		* SRP - Single-Responsibility Principle for small functions
		* OCP - Open-Closed Principle
		* LSP - Liskov segregation principle
		* ISP - Interface segregation principle
		* DIP - Dependency Inversion principle

**Approach:**
* Gain understanding
	* Ask questions about the code
	* Investigate their decision against alternatives (ex. Do you think ____ would be better? If not, why?)
	* Research individual lines to find smart conventions and alternatives
* Assure that comments are positive, constructive, and avoid harshness
	* Avoid too many suggestions at once, pick the most valuable, perhaps only 1 major point
* Separate concerns when figuring suggestions (ex. Regarding formatting…)
* Keep reviews small (PRs too)
	* Max 500 LoC/hr
	* Max 1 60-minute review session daily
* Consider setting goals
	* Decrease in defect or error rate
	* Increase in KPIs
* Have the engineer annotate the PR ahead of the review
	* They can walk you through the changes and explain their reasoning
* Consider developing Review specific checklists regarding the Primary and Secondary Concerns

**Further Reading:**
*  [http://guides.beanstalkapp.com/code-review/guide-to-code-review.html](http://guides.beanstalkapp.com/code-review/guide-to-code-review.html) 
*  [https://smartbear.com/learn/code-review/best-practices-for-peer-code-review/](https://smartbear.com/learn/code-review/best-practices-for-peer-code-review/) 
*  [https://www.atlassian.com/blog/software-teams/5-tips-great-code-reviews](https://www.atlassian.com/blog/software-teams/5-tips-great-code-reviews) 
*  [How to do code reviews - Server Density Blog](https://blog.serverdensity.com/how-to-do-code-reviews/) 
	* Assumes a review / approval with each PR (Push, can hold several commits) this may be good for master, if done max once a day, but not if people are merging throughout the day - better done in waves
	* Talks about having a good template for each PR, testing each PR, not as much on searching for code smells

#department/development/review
#items/procedures
#items/procedures/qa
