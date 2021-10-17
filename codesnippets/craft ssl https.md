# craft ssl https
* [Overview: Site moves with URL changes - Search Console Help](https://support.google.com/webmasters/answer/6033049) see section title Migrating from HTTP->HTTPS
	* must update the Search Console
* enforce through .htaccess
* double check other resources
* update site name
* update sitemap
* [Secure your site with HTTPS - Search Console Help](https://support.google.com/webmasters/answer/6073543) - additional recommendations and best practices
* Strict Transport Security Header to force HTTPS loading
* [Enforcing SSL for CP Requests | Support | Craft CMS](https://craftcms.com/support/force-ssl)
	* Although it is more secure, HSTS adds complexity to your rollback strategy. We recommend enabling HSTS this way:
	* Roll out your HTTPS pages without HSTS first.
	* Start sending HSTS headers with a short max-age. Monitor your traffic both from users and other clients, and also dependents' performance, such as ads.
	* Slowly increase the HSTS max-age.
	* If HSTS doesn't affect your users and search engines negatively, you can, if you wish, ask your site to be added to the HSTS preload list used by most major browsers.
* https://securityheaders.com/?q=baumannbuilding.com&followRedirects=on
* verify CORS resources
* s

[[Craft Databases]]

#department/development/codesnippets