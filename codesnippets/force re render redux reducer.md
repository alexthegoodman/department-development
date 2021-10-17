# force re render redux reducer
Latest render not displaying? Make sure that your object is not just a brand new immutable object, but also has a different shape. This can be done by creating some junk data with uuid’s so that the shape is different. You may or may not save history data with each updateAction[uuid.v4()], but it, along with either deepcopy(), $.extend(true, {}, state), or sometimes Object.assign and update() will assure a complete and through visual render every time.

watch out:
* declaring out of state this.phaseDataLength
* not doing real deep copies
* not changing state shape for redux
* proper keys off the bat will solve many problems... or else it will re mount and the code in componentDidMount will run only once
* quite possibly a combination of these things
* make sure to deepcopy() your connected redux props inside the render() function - if you map() it, the reference inside your redux store is also updated - except sometimes this isn’t desirable

#department/development/codesnippets