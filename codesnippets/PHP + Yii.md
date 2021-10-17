# PHP + Yii
**PHP**
* use _path_here/NameSpace as SpaceName
	* Namespaces can be referenced by full path, but the “use” keyword shortens and renames it (like an import)
	* autoloaders negate the need for use and/or include statements
	* “use” does not include anything, it just loads the class into the namespace
	* “include” can take any kind of PHP and insert it there
	* use can be used to include 2 namespaces with same name as having different names also
	* may need to do both
	* include inherits the variable scope
* [PHP: Scope Resolution Operator (::) - Manual](http://php.net/manual/en/language.oop5.paamayim-nekudotayim.php)
* self, parent and static are used to access properties or methods from inside the class definition
	* $this ?
* [PHP: Function arguments - Manual](http://php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration)

**Yii 2**
* Actions like _create-comment_ will map to the actionCreateComment function in your Controller (route format: ControllerID/ActionID)
	* $this->render for rendering a view with a set of context variables
* Views are scripts to generate content using the Yii templating system, a PHP based output system (<?= Html::encode($message) ?>)
* Model is usually used for data not associated with database tables, while ActiveRecord is normally the parent for those that do (in Yii, both go in _models_ but extend different classes)
	* Active Record is an ORM wrapper which enables all sorts of database actions
	* Active Record inherits all model features including validations, serialization, and data attributes
* Yii comes with the ActiveForm widget, and fields as well, which when attached to a model, will reflect that models validation
* Using the Paginiation data object, you can chop up a query, and pass in pagination related params to maintain that query conveniently. Then use LinkPager widget to output the pagination HTML

#department/development/codesnippets