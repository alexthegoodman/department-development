# App and API Versioning
There are many approaches to take.

* Separate instances for each version (different Heroku app)
	* This is expensive and in-compatable with a highly iterative app (many releases 1.x.x)
	* Each Version has its own dependencies and environment configuration also - though old versions can be updated so long as its very small compatibility patches
* Duplicate and alter root directory for each version, 1 instance
	* This creates a ton of extra copies of files, since even endpoints that aren’t altered are duplicated in each _1.1.3_ directory
	* But keeps the sub-directory structure as simple as now, and allows straightforward new versions.
* Duplicate and alter each endpoint (organized with 1 endpoint per file), have all versions of it in the file
	* [https://www.npmjs.com/package/express-routes-versioning](https://www.npmjs.com/package/express-routes-versioning)
	* Overly complicated: commonly requires multi-level directories like _get_users_______________/ and may be more difficult to keep separate.
	* There is an appeal to deal with that one endpoint and see its history there

* When to release new version - New API versions can be released on its own, or due to a new demand placed on by 1 of the apps (web, mobile, tv). The benefit is that those apps do not have to be updated by us or the consumer, thanks to have the old version available. This means that reliable use not only exists between app versions, but entirely separate apps as well. iOS v1.1 might use API v 1.2.3, while tvOS v1.4 might use API v1.7.2, while another user has an old version of tvOS v1.3.1 which is on API v 1.2.5.
	* A version is needed due to new features, requirements, and architectures - not bug fixes
	* Does this mean that API versions must be large? One would not a directory like:
	* _1.1.1_
	* _1.1.2_
	* _1.1.3_
	* _1.1.4_ - **so long as its the newest version, not in Live use, it need not be incremented. Increment upon the version’s first Live use.**
* When to archive an old version - User analytics show that no apps are currently accessing that API. Show a warning message ahead of time.
* How does dependency updates affect all API versions?
	* You could say that old versions are ONLY updated for dependency updates, not to change function or what’s needed, but small patches which do not change the actual version number. Yes.
	* Just be careful to update dependencies because it could break the whole chain. Ideally, old automated tests would be preserved as well.
* What about changing the database?
	* If changing the database, all versions will need to change. If an unlikely database re-design takes place, you should create a whole new instance.
		* Save API version on each row, helps to detect needed on-the-fly updates / migrations
		* - But look into MongoDB and templated object shapes. Would be nice to update the shape for each version and perform the migration upon Heroku push.
* Public releases that require new things from the API should be rare. During the internal alpha stage, keep it all on 1.0.0 and make everybody update their Testflight app. Let them know that versioning will start upon public release, at which point the API should be updated in larger increments. (Perhaps monthly)
* A version is needed due to new features, requirements, and architectures - not bug fixes
* Update changeling file, consider auto-generated documentation (like more than Swagger? [http://apidocjs.com/#preface](http://apidocjs.com/#preface) simpler and nice, although a Graph Explorer style interface would be nice as well [https://www.npmjs.com/package/express-api-doc](https://www.npmjs.com/package/express-api-doc) ?)

<a href='App%20and%20API%20Versioning/CA%20Technologies%20-%20OReilly%20Microservice%20Architecture%20eBook.pdf'>CA Technologies - OReilly Microservice Architecture eBook.pdf</a>

#department/development/codesnippets
#department/development/apps
#department/development/backend/api