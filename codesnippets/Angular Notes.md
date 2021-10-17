# Angular Notes
* Angular CLI
	* Start projects, initiate components
	* Run end-to-end tests (Protractor), run unit tests (Karma)
	* Linting
	* ng update for updating angular
	* Building and serving
	* Config schema: [angular cli · angular/angular-cli Wiki · GitHub](https://github.com/angular/angular-cli/wiki/angular-cli)
	* Can generate new scaffolding
		* [GitHub - angular/angular-cli: CLI tool for Angular](https://github.com/angular/angular-cli#generating-components-directives-pipes-and-services)
		* Components, Directives, Pipes, Services, Classes, Guards, Interface, Enum, Module
* Hot reloading built-in via CLI serve
	* See about webpack - is it a part of the CLI itself?
* Components 
	* may have inline templates and styles if they are too small, but Angular also provides a respectable separation of concerns by default
	* Components have lifecycle methods like React
	* Component selector works like jQuery’s
	* Global objects like window and document are not available in html template, but are in the component class where they can be passed down
* Angular testing?
	* How is the core angular_core_testing system integrated into a larger system?
* Decorator functions are used commonly to attach to follow class declarations
* [attr]=“var” is better than attr=“{{var}}” due to correctly updating properties on things like inputs, though {{var}} is great for text and other output
	* the var string can be a boolean (true), class property (defined as public _____ on the Component)
* It seems that Angular does not have the same state as React, but any component variable can be updated at any time to produce reactive effects
* [ngClass] as alternative to [class]
	* Provides ability to easily add/subtract classes via a className: boolean structure
	* [Angular Docs](https://angular.io/api/common/NgClass)
*  [Angular Docs](https://angular.io/api)
* ngSwitch and ngSwitchCase for radio buttons is best, see all built in Form components
* ngFor and ngif have various attributes and functions
* (click)=“function” or (click)=[function()]
* data binding
	* EventEmitter
* pipes
	* formatting (currency, percents, dates, string slice - lang?)
	* masks?
* Input() and Output() can be used to share data
* Services also are used for data sharing, they may implement app logic and interact with APIs
	* employee.service.ts and class EmployeeService
	* declare the class, use Angular Injector to include it
	* Best to register Services at top App Module, so all components can access it (but you can include it at any point in the tree of components)
	* Register it via the “providers” attribute
	* Define the service in a components constructor
	* in the ngOnInit function, you can do “this.employees = this._service.getEmployees()” - and most likely using async / await
	* To tie services together, you need the Injectable() decorator function from angular/core
	* can you update service data to update all connected components?
* RxJS assists with working with Observable and includes Reactive Extensions
* Observables provide changing / asynchronous data to subscribed components
	* In _app_ create employe.ts which simple does “export interface IEmployee” which is an object / array.
	* Then in the service, include the Employee via file and rxjs/Observable
	* alter your functions like “getEmployees(): Observable<IEmlpoyee[]> {}
		* what does this mean? Why?
	* this will make the function return like a promise, so in the component you can run the service call this._service.getEmployees().subscribe(data => this.employees = data)
	* very good! Clean and minimal
* HttpClient module provides a simple API
	* import it in App Module from angular_common_http
	* Then put in NgModule’s imports property
* 

TypeScript:
* “implements” keyword
* “public” required?
* type http?
	* or does constructor(private http: HttpClient) simply set this.http easily?
* 

#department/development/frontend
#department/development/codesnippets