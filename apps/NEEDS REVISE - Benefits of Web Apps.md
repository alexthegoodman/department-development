# NEEDS REVISE - Benefits of Web Apps
This is all Technical. Only Business- and Role-Oriented Benefits are needed in the. [[Solution Index]].

- - - -

Benefits of React:

* **Load time** - Get all of the data once and have a State Object on the front end. The State Object is a live, complete representation of all the data powering your app instance. This means a Browse page with all of it’s data will appear almost _instantaneously_. (like an actual app) There is only a loading screen upon launching, which is characteristic of any application, including web applications like we’re discussing now.
* **Dynamic templating** - Due to the fact that all data is available to the SPA (Single Page Application), and all of the markup is created within it also, every DOM node that is associated with a data point will automatically update.
* **Standardization** - Knowing a common framework like React allows developers to get up to speed more quickly, produce quality more consistently, and work better together as a team.
* **Components** - React is essentially based upon Components, indivisible pieces of the app, much like template partials in a PHP or server-side CMS set up. The Components are nested and commonly work closely together.
* **Community** - The React community is the ES7+ community. This means they are on the cutting edge of web technology, and it’s a good place to hang around.
* **Versatility** - React Native allows the creation of iOS and Android apps, Windows and macOS apps, as well as real-time in-browser web apps — all with the same technology which great decreases costs.
* **Scalability** - React is prepared for as little as 2 components and as many as 2000

Benefits of API, Server, SPA structure:

* Redesigns can remain separate from server logic
* The API can be hooked up to a mobile app, native app, and be opened up to 3rd parties with relative ease
* Separation of concerns

	* Different configuration settings on API and Server
	* The Server simply serves up the SPA bundle (large, compressed JS file and other resources)
	* The API provides the CRUD interface for the database

Some Benefits of Web Applications In General:

* An API is built along with but separately from your app right from the get-go

	* You save time and money down the road if you need to redesign the app, have new apps connect to the same data, or open up the API to the public (like Facebook’s Graph API)

* We can server our apps at lightning speed

	* HTTP2 is leveraged so app resources (code, images, media) are loaded 3x as fast ( [http://www.http2demo.io/](http://www.http2demo.io/) )
	* Your app only loads once

* Your web app works in any browser at any place
* Achieve real-time, butter-smooth user experiences

API:

* oAuth 2.0 provides industry-leading security
* Consistent CRUD interfaces and JSON responses for every major endpoint
* Optional documentation and support
* Optional developer or administrator dashboard / API Console
* Optional features for filters, sorting, page cursors, rate limiting, versioning

Should my components be so reusable that they’re called independent? Should the InviteModal be transferrable between projects needing only configuration (email options, etc) I say the answer is yes, and for the most part they are. Would the modal simply dispatch actions when you interact with one of the invite options (all options are optional), and then the redux logic would be different for each app? Or, since the redux files are broken up according to the components they are involved with, you can decide whether to bring over one, both, or pieces of both on the next project. The goal should simply be to try to keep them separated, but sometimes intertwined components are unavoidable to accomplish a unique task.
It’s also worth considering whether or not a dependency like materialize is a good idea or not….

#misc/archive/Up Next/ideas/business-misc#
#department/sales/talkingpoints
#department/development/apps