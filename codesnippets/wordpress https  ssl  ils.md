# wordpress https / ssl / ils
www redirect and https redirect

* Make sure SSL certificate is installed
* Clear DNS records of www references (a DNS record cannot usually be made to point root domain to www, but only the reverse) - and make sure the www domain is visitable
* Simply change the WordPress site URL through the dashboard
* Then put in .htaccess:
```
RewriteCond %{HTTPS} off
RewriteRule .* https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
```
* Double-check sub-pages for proper redirection and enumerable variations
* 

#department/development/codesnippets