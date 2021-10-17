# Craft Plugins
* [[Install Craft 3 Procedure]] 
* [[Craft Databases]] 
* [[PHP + Yii]]

* https://pluginfactory.io/
* https://github.com/taylordaughtry/plugin-starter

* [QueryBuilder, yii\db\mysql\QueryBuilder | API Documentation for Yii 2.0 | Yii PHP Framework](https://www.yiiframework.com/doc/api/2.0/yii-db-mysql-querybuilder)
* How craft commerce migrations generated?
![](Craft%20Plugins/Screen%20Shot%202018-08-22%20at%209.50.14%20PM.png)

* Having your Craft Plugin in a separate directory, the best way to work on it during development is with a “path repository” which allows you to install the plugin to your Craft project via a symlink in your composer.json
	* https://docs.craftcms.com/v3/extend/plugin-guide.html#loading-your-plugin-into-a-craft-project
	* this symlink will keep the _vendor_plugin/ updated in the craft project while working on it from its own folder (this is probably good for node_modules also)
* Craft auto checks for new migrations when the schema version number changes, and I believe migrate/create is an optional command to do this manually - ultimately I believe changing your models and schema number should do the trick
* Settings in the Settings module are saved in the craft_plugins table in the settings column, but other models should receive their own table
* _templates_ hold the admin side templates
	* [Control Panel Templates | Craft 3 Documentation](https://docs.craftcms.com/v3/extend/cp-templates.html#page-templates)
* Register admin side pages with EVENT_REGISTER hooks in the main plugin file, or in a spot more convenient to the size
* Asset Bundles (by Yii) allow plugins to expose src CSS, JS, and images to the site front-end
	* https://docs.craftcms.com/v3/extend/asset-bundles.html
* [Working with Databases: Active Record | The Definitive Guide to Yii 2.0 | Yii PHP Framework](https://www.yiiframework.com/doc/guide/2.0/en/db-active-record)


#department/development/codesnippets