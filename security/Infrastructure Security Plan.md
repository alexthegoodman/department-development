# Infrastructure Security Plan
##  Version 001:
* Summary
	* The **On-Site Security Plan** 1 of 3 Security related plans, Security Strategy
	* Describe its role within the larger [[General Infrastructure Plan]]
	* Define the boundaries of generated Working Plan
		* Hosting servers, Service servers (CDN, image processor, etc) ?
		* VoIP, Printers, Office Keys and Phones, and other IT related items ?
		* Physical security (perhaps mention access to resources) ?
	* Using boundaries to grade the correct areas against stand security benchmarks - guarantee your security grade within high priority areas
	* Consider as a double check even if IT should be handling it
	* A multi-tiered Plan (2 or 3 tiers)
* Objectives
	* Prevent hacking and ransomware
	* Protect user data and user privacy
	* Protect your brand for long-term damage
	* [Security Made Simple for Business. Centralized Data Protection for Networks, Endpoints, Encryption, Mobile, Web, Servers and the Public Cloud. Next Gen Security to Prevent Against Email Phishing Attacks, Ransomware, Exploits and Advanced Threats | sophos.com](https://www.sophos.com/en-us.aspx)
	* Does not aim to solve extended Infrastructure needs such as mobile phone distribution / management, VoIP or office technology needs.
	* Pass all inspections and exams performed on a regular basis to assure compliance with all
* Management
	* Same as [[On-Site Security Plan]]
	* Commonly handled by external Security consultants ?
	* Consider involvement of IT departments and partners as highly likely
* Timeline / Milestones
	* Pre-Production
	* Production
	* Maintenance
	* Support / Emergency Response
* Regimen Index
	* Protect all infrastructure services 
		* Database security (IAM)
		* Host / Server provider (AWS could have many Plans, S3, RDS, DynamoDB, data processing)
		* 	recommended item is a CASB 
			* which secures cloud services like Slack and Salesforce, seems to show very clearly the value of compliance and security to enterprises 
			* ( [https://www.netskope.com/](https://www.netskope.com/) )
			* and a leading brand: [https://www.skyhighnetworks.com/](https://www.skyhighnetworks.com/)
	* Implement security measures for all storage handling or processing points
		* Show configuration diagram
	* Proxies and firewalls
	* Mail server encryption
	* Test using automated systems and / or real penetration testers
		* Test regularly (with a Schedule attached and assigned)
		* Monitor both tests and real usage regularly
	* Verify all measures carefully and deliver thorough records as results of Production QA processes
	* 3rd Party Reviews may required and / or desired
		* Especially as an investment force to gain value from their advice early on and produce better plans sooner (may need individuals)
		* Helps future clients see the value - just as producing plans for BB or CG help to sell clients of tomorrow
	* FLSM(HR) Impacts
		* Legal
			* Special storage, transfer, or handling procedures as required by law
			* Special approvals, permissions, information collection
			* All related to cybersecurity laws and compliance issues
		* Finance
			* Avoid legal challenges


* How does a standalone Security Plan fit BN’s design-centric image and positioning? Does it balance our offering, is it wasteful, is it distracting?
	* [[Ad Messaging / Brand Positioning]]
	* [[Positioning Plan]]
	* [[Competitive Positioning Map - Notion]]


#items/plans
#items/strategies/security
#items/plans/external
#department/development/security