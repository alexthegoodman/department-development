# Javascript ES6/7 / TypeScript
Various notes on obscure or interesting features. May include Typescript notes also.

* Symbols
	* https://www.keithcirkel.co.uk/metaprogramming-in-es6-symbols/ 
	* useful for situations where a unique key needs a name (potentially replace uuid)
* Error Types
	* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypeError
* Set object
	* https://medium.com/front-end-hacking/es6-set-vs-array-what-and-when-efc055655e1a 
	* consider Set object when duplicate values in an Array need to be prevented (Sets cannot have duplicates)
	* It also has convenient prototype functions
* Map object
	* Retains correct order like Array, but acts as an Object with key-value pairs
	* Keys can be objects in addition to primitive values
	* I believe it is selectable by the Index AND the Key, which is awesome
	* Map is not directly supported in JSON, but may be encoded for transport
* Comparing strings of different languages
	* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Collator
	* [[Multi-Language / Localization]]
* https://developer.mozilla.org/en-US/docs/Web/CSS/:first-child
	* and :nth-child are great selectors when nth-of-type is not best
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function* combined with Promises, this could be a powerful way to transform a block of functions into an iterable
* Structuring and destructing objects in ES6
	* Best preference: [Lodash](https://lodash.com/)
	* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax indeed: ...arr will spread in air. [...arr] creates a new array with the same contents, [...arr, ...arr2] or [...arr, 'item1', 'item2'] creates a combined array like extend. coming soon for {...objects} !
	* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment 
		* {a='defaultVarValue', b: altVarName} = {a: 10, b: 20}
		* [a,b, ...c] = [0,1,2,3,4] (c = 2,3,4) (uses the spead operater in a variable decaration which takes its assignment from the value provided rather than something pre-defined.)
		* Could probably do [a,b,c, ...extra] = [...arr1, ...arr2]
		* Arrays are ordered, objects are grabbed by keyname.
* for … in and for … of
	* https://stackoverflow.com/questions/13632999/if-key-in-object-or-ifobject-hasownpropertykey
* super(extendedClassConstructorParam1, extendedClassConstructorParam2)
* x = 0; x = (x++, x--, x); (x is still 0)

#department/development/codesnippets
#department/development/apps