# immutable objects
$.extend(true, {}, state); true is for deep copies!

update(state, {}); [https://github.com/kolodny/immutability-helper](https://github.com/kolodny/immutability-helper)

[https://www.npmjs.com/package/deepcopy](https://www.npmjs.com/package/deepcopy)

* -in your redux reducer, note that "On a `deep`extend, Object and Array are extended, but object wrappers on primitive types such as String, Boolean, and Number are not. Deep-extending a cyclical data structure will result in an error.” so it may be converted to an array-

After objects were converted to arrays in redux, the better answer: with Redux, it’s important to make a deepcopy() in your reducer - but also make sure to make a deepcopy() of a connected prop in your render() function. See note “force re render redux"

#department/development/codesnippets