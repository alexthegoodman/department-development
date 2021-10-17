# Security Checklist
### Sales Development
Communicate the various Security areas

### Project Prep
Consult legal on Security requirements as related to this specific client

### Task Approval
Web and App: https://airtable.com/tbl2A0ANbMDJCDLkw/viwIfJAxIOis53Exb
Infrastructure: N/A

### Maintenance
Re-Test against common security pitfalls

### Notes
* Sales / Marketing implications
* How do corporations value these sorts of security measures/options during the bidding process?
* DDoS Protection:
* https://www.akamai.com/uk/en/products/cloud-security/prolexic-solutions.jsp
* Cloudflare also helps here
* 3rd Party Security Firms / Consultants
* This *may spill over into IT. [[IT / Cyber Security / IT Security]]
* We take care of internal (on-site) site security, but our consultant will take care of the server administration, mail server, databases, and other vulnerable touch points.
* This is a higher-level package unlikely to be as useful to Express projects, but only Transitional or Transformational ones.
* Google undergoes several independent third party audits on a regular basis to provide this assurance. Their customers and regulators expect independent verification of security, privacy, and compliance controls.
* Working with External User Researchers: Part I · An A List Apart Article a smart article on consultants and external contractors
* Credential Management (CM) Web API
* Credential Management Level 1
* Automated 2-factor authentication?
* Communicating Security
* How Much Security Is Enough? | US-CERT
* Product and tool provided features such as
* cPanel
	* Leech Protection (handle compromised accounts)
	* IP Blocker
	* Hotlink Protection (akin to CSP) (handle <img> tag on another site with src of your site)
	* SSH Access (curious how many low level operations are available, such as sudo)
	* Resource Usage Overview (see levels for DDoS)
	* Raw Access (a log of site visitors, no graphs or extras)
	* Encrypted Email (good selling point)
	* Virus Scanner (probably not of good quality)
	* Patchman (supposed to watch for malware and software vulnerabilities)
	* Track DNS (a mini DNS ping-er)
	* PHP Selector (like PEAR packages, but things like imagemagick, also php.ini settings)
	* Server Rewind

### Platform Docs: 
#department/development/security
**General Web**
https://simplesecurity.sensedeep.com/web-developer-security-checklist-f2e4f43c9c56
Top 5: Security risks associated with web apps - TechRepublic - Broken authentication, injection, XML injection - Test against each of these
[https://www.hacker101.com/]
**Google Cloud**
https://cloud.google.com/security/compliance
**Node / Express**
https://github.com/shieldfy/API-Security-Checklist
https://expressjs.com/en/advanced/best-practice-security.html
https://blog.risingstack.com/node-js-security-checklist/
Express Rate Limits: ( https://www.npmjs.com/package/express-limiter )
https://securityonline.info/pentesters-framework/
https://www.manning.com/books/understanding-api-security
**Heroku**
https://www.heroku.com/policy/security
https://devcenter.heroku.com/categories/security
become a Heroku Partner
**Craft**
https://craftcms.com/support/securing-craft
(ex. Change the cpTrigger)
**AWS**
Securing Amazon S3 - (directories are private, individual files may be public and un-guessable… or, try signing)
(Like Lob’s signed URLs https://s3-us-west-2.amazonaws.com/assets.lob.com/psc_ea9eb6038681c215.pdf?AWSAccessKeyId=AKIAIILJUBJGGIBQDPQQ&Expires=1489180005&Signature=lWyUVw9EKnfKum%2BPCk%2BlGN11tI4%3D )

<a href='Security%20Checklist/MPAA-Best-Practices-App-and-Cloud_V1-0-20150507-RELEASE-CANDIDATE-6.pages'>MPAA-Best-Practices-App-and-Cloud_V1-0-20150507-RELEASE-CANDIDATE-6.pages</a>

### Tools
See Airtable

Examples
![](Security%20Checklist/Screen%20Shot%202018-02-14%20at%207.28.52%20PM.png)
![](Security%20Checklist/Image-1-1.jpg)
![](Security%20Checklist/Image-1.jpg)

#department/development/security