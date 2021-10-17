# Apache Terminal + PHP setup
* Assure all required modules installed
* Apache config
* Transfer all hostnames to correct file, record file name
* Assure correct PHP version, extensions / modules, logs, cache
* Apache log file
* Ports for Apache (80, ssl 443) and MySQL (3306)
* Run servers as _____ (alex)

**Installing and Upgrading MySQL and Apache:**
* “ps -aef | grep httpd” to see running Apache (httpd) processes 
* update Xcode and OS Environment
* xcode-select —install (to install cli tools)
* “brew upgrade” to upgrade php and apache versions
* brew services list (to see all home-brew services)
* [Install MySQL on Sierra using Homebrew · GitHub](https://gist.github.com/nrollr/3f57fc15ded7dddddcc4e82fe137b58e)
	* ERROR 2002 (HY000): Can’t connect to local MySQL server through socket ‘_tmp_mysql.sock’ (2)
		* Find the my.cnf file in _usr_local_etc_my.cnf for home-brew
		* _usr_local_var_ contains the Home-brew database data (back this up)
		* _usr_local_Cellar_ holds all of the Home-brew packages, this is what should be updated
		* brew switch mysql 5.7.18_1 (to run 5.7 over 8)
* [How to Install Apache on macOS via Homebrew – TecAdmin](https://tecadmin.net/install-apache-macos-homebrew/)
	* check on the running apache processes to see if service is working
	* should be within _usr_local_opt_httpd_bin_httpd
	* brew install php71 --with-httpd24
	* _usr_local_etc_php_7.1_php.ini
	* brew services stop httpd
	* —— **COME BACK TO THIS LATER**, Apache may start just fine, same with MySQL, currently working with its httpd.conf file to get localhost displaying correctly (.conf file nearly same as MAMP’s, except Py’ WSGI disabled for example) (will use MAMP apache in meantime, config, app data, and storage data are kept protected w/ home-brew)
		* Compare: _usr_local_opt_httpd_bin_httpd -v
		* and: apachectl -v (seems to use same .conf, but not same version)
		* and: httpd -v (so use this)
		* See _www_working-httpd.conf for copy of last working version
		* Set up Apache for autostart at macOS Sierra (re)boot - alter the paths in this section
		* The .plist is a property list, see by listing brew services
* httpd -V | grep SERVER_CONFIG_FILE
	* -D SERVER_CONFIG_FILE=“_private_etc_apache2_httpd.conf”
	* open the config file
	* this file should resemble MAMP’s when finished (keep in mind the edits recommended by Install Apache instructions)
* Move _www_ folder to new doc root, backup MAMP configuration files and put in _www_
	* DocumentRoot is _usr_local_var_www
	* The default ports have been set in _usr_local_etc_httpd_httpd.conf to 8080 and in /usr_local_etc_httpd_extra_httpd-ssl.conf to 8443 so that httpd can run without sudo.

* [Server Requirements | Craft 3 Documentation](https://docs.craftcms.com/v3/requirements.html#checking-your-server)

Example:
* open _Library_Application\ Support_appsolute_MAMP\ PRO_conf_httpd.conf
* open _private_etc_apache2_httpd.conf

possible to control these PHP and Apache versions? 
Host names with specific PHP version?

https://gist.github.com/DragonBe/0faebe58deced34744953e3bf6afbec7
[linux - Lost httpd.conf file located apache - Stack Overflow](https://stackoverflow.com/questions/12202021/lost-httpd-conf-file-located-apache)

#department/development/codesnippets