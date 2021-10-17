# On-Site Security Plan
[[Defensive Security Handbook]]

## Version 001:
* Summary
	* The **On-Site Security Plan** 1 of 3 Security related plans, Security Strategy
* Objectives
	* Quantitative
		* Protect your brand and reputation investments
		* Protect your valuable research investments (IP)
	* Qualitative (though can usually be Measured in other ways)
		* Implement best practices
			* Understand the attacker: Mimic / emulate attacks
		* Deter attacks
		* Terminate and obstruct attacks
			* Protect all access points, Encrypt data in transit and in storage
			* Update regularly
			* Remedy outages (may reference [[Maintenance / Support Plans]])
			* Emergency response
		* Trace attacks
			* Target suspect users and deploy “smart” controls such as a timed blockers
* Management
	* Client access to a potential client collaboration app which could house additional apps
	* For Transformational Projects, a Dedicated Manager or Engineer will be available on-call
		* This person will often acts as the controller and operator for several 3rd party services and consultants
		* This person may be the communication point for all Technical collaboration (feedback, comments, email)
	* The Project Manager will handle 
		* QA verifications
		* Assignment of contractors, content providers and service providers
		* Responsible for project completion on-time
		* Client project-related communications
	* Benchmark against strict budgets and thresholds in all stages of the production process and provide verification records for storage
* Timeline / Milestones
	* Pre-Production
	* Production
	* Maintenance
	* Support / Emergency Response
* Regimen Index
	* Pre-Production
		* Security Assessment
	* Production
		* Each layer (like Support and Maintenance)
		* _Data sources_
		* _Infrastructure / Host_
		* _Back-end Code_
		* _Transport Layer_
		* _Front-end Code_
		* _User Device_
	* QA and Production Verification 
		* Independent 3rd party validation / testing results (“Obtain independent 3rd party verification” in Base Plan + Literature)
		* implementation details (“Define the processes, timelines and people involved”)
		* Inspiring: [http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53r4.pdf](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53r4.pdf)
	* Maintenance / Monitoring
		* Coordination with Heroku on test windows
		* Continuous scanning and intelligent detection
		* Logging systems and monitoring schedule
	
**Additional Information:**
	* Optional Deliverables
		* _Could do input -> output diagram with a lock icon in between, the high level visual for securing all incoming and outgoing data_ 
		* Provide platform-specific training manual(s) on cPanel, Plesk, Heroku? **deliverable sample**
		* Test against all attacks and provide test result data **deliverable sample**
		* Deliver Something which actually delineates all of this site’s potential holes (big 10 * 10), shows how they’re plugged?  (CG would like this) **mark as deliverable sample**
		* All important pieces mapped (data pipe from database outward), categorized, labelled, and visualized
			* show example
	* Specific Security Controls
		* Timed Blockers
		* WebSocket Security / Real-Time Data In-Transit
		* Permissions and file structure and database things are[[Infrastructure Security Plan]]
			* Protect file systems, servers, DNS access
			* Limit access by IP, user name, type
			* Encrypt data in transit with SSL
		* Integrated Features / Authentication Layers
			* 2-factor authentication (phone, email)
			* TouchId, FaceId
		* Protect all technical services
			* Payment Processors, Providers, and Merchant services
			* Application security (protecting the back-end and CMS)
				* Consider best practices and recommendations from respected institutions
				* User permission systems, groups, email and other communications integrations
				* Encrypt all sensitive data
				* AWS, Heroku, Media Temple
				* Craft, Wordpress (?) (show icons, do list?)
				* API headers, data handling
		* Front-end security (protecting the contact forms and user interface  elements displayed in the browser)
		* Encrypt all data with above-standard hashing algorithms (unauthorized database access would still not reveal the data contents)
		* Auto-logouts
		* Other items listed in checklists

**Inspiration:**
	* For Literature:
		* High and Low Level layers provide backup security protection
		* Imagine a security-specific process like this one
	* Process diagram for large systems:![](On-Site%20Security%20Plan/Screen%20Shot%202018-01-20%20at%202.50.35%20PM.png)
	* Roles: ??![](On-Site%20Security%20Plan/Screen%20Shot%202018-01-20%20at%202.50.40%20PM.png)

#items/plans
#items/strategies/security
#items/plans/external
#department/development/security