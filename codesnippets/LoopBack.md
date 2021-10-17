# LoopBack
* Datasources are LoopBack’s way of connecting to various sources of data, such as databases, APIs, message queues and more
* application.ts sets up main config
	* determine location and naming convention for controllers
	* integrate models
* index.ts boots the app with the config
* seuqence.ts describes what should happen on each request (middleware?)
* Dependency Injection is a technique where the construction of dependencies of a class or function is separated from its behavior, in order to keep the code loosely coupled.
	* Seems like an alternative approach to certain dependencies with a few benefits
	* [Dependency injection | LoopBack Documentation](https://loopback.io/doc/en/lb4/Dependency-injection.html)
* controllers
	* The @repository decorator will retrieve and inject an instance of the TodoRepository whenever an inbound request is being handled. 
	* most business logic
	* You can customize the lifecycle of all bindings in LoopBack 4! Controllers can easily be made to use singleton lifecycles to minimize startup costs. For more information, see the Dependency injection section of our docs
* LoopBack’s boot module will automatically discover our controllers, repositories, datasources and other artifacts and inject them into our application for use.
* [Key concepts | LoopBack Documentation](https://loopback.io/doc/en/lb4/Concepts.html)
* 

#department/development/codesnippets