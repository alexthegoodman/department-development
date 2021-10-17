# C# / ASP.NET / Xamarin
* Open _dotnet-console_
* “dotnet restore” to install dependencies
* “dotnet run” terminal
* “curl http://localhost:5000” in another tab and it will output a context text
* dotnet watch run will watch or file changes

* Open ASPCoreTestAPI
* ControllerBase is leaner than Controller, Controller is used when also creating views, ControllerBase is for APIs
* ASP.NET Web API is older than ASP.NET Core, Core has what you need for Web APIs
* Use Postman or Insomnia to test API

* Many C# syntaxes are identical to JS, and so are built-in APIs (.IndexOf, .Length, arr[0], for loop, try block is similar, etc)
* Arrays apparently have a set size, while Lists can grow in size (a better choice) List<int> means a List of ints when type casting
	* List.Add
	* easy to create a List which holds an array
	* List.Insert to insert / replace at a specific index
	* use List.Count to get length
	* .Where for .filter, use lambda shorthand arrow function within
	* [List<T> Class (System.Collections.Generic) | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2)
* static means ALL instantiations of the class or object share this as a singleton
	* non-static cannot access static, but static can access non-static
* Class : ExtendedClass
* public Construction : base()
	* like calling super()
* 2 constructors (or more, maybe) can be created, where 1 has no passed in values and the other does
* “new public string” on an extended class will override that property definition
	* override is for methods
* abstract class cannot have new instantiations, but its methods can be used
* public interface InterfaceName can be used, the interface will require anything that extends it to have certain properties
* operator keyword can be used to override an operation, such as addition +
* ClassObj<passing,values> thing = new ClassObj(passVal, valueVal)
* structs, delegates
* C# does support arrow functions as short hand, run with funcName.Invoke()
	* lambda expression?
* Dictionaries are equivalent of objects

* [.NET API Browser | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/api/?view=aspnetcore-2.0)
* IIS can’t be run on Mac and can probably be removed from launchSettings.json
* 



#department/development/codesnippets