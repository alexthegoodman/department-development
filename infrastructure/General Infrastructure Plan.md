# General Infrastructure Plan
[[Infrastructure Security Plan]] and one for Performance? Less important?

* Web Sites and Apps Infrastructure needs are tied to their Scaling Plans or realized loads
* Hosting styles
	* Self-hosted (IT supported, may be important or overly expensive)
	* Your own provider (may not always be appropriate)
	* Ours
		* Private server (apache server for most web sites)
		* Distributed system (API server for large apps and some sites)
		* Comparing providers (Google Cloud, AWS, RackSpace)
* Hosting requirements and standards
	* Security and Performance implications
* Database requirements
* Image and asset management, Search, big data processing, supporting various database types, and other capabilities are made available
* Common use of 3rd parties
* Transferring from old system to new one
* Considerations
	* Client access location
	* Updates and configuration
	* Monitoring and integration with Production
	* Planning ahead (Scaling Plan, possibly Mitigation Plan)
* Estimating costs
	* 1-time, subscription, our fees, client time
* Determine Host Type
		* Hybrid, Cloud, On-Premise / On-Site

### Important Considerations:
* Speed
	* HTTP2 / protocols
	* Response Time
* Security
	* SSL
	* Proxies
	* Firewalls
* Maintenance
	* Mail transfer
	* Domain transfer
	* Backups
	* Mail hosting support
	* PHP Mail support
	* Timing and notices, updates
* NGINX vs Apache

#items/plans
#items/plans/external
#department/development/infrastructure