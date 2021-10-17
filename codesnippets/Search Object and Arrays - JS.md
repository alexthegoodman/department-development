# Search Object and Arrays - JS
 JSON w/certain structure: let thisProject = jsonQuery('[project_id="' + projId + '"]', { data: userProjects });
 arrays: let thisProject = query('project_id').is(projId).on(userProjects);

 exotic JSON search, grabs parents
thisProject = new JefNode(userProjects).filter(function(node) {
if (node.key == 'project_id' && node.value == projId) {
return node.parent.value;
}
});
array.includes()

maybe best for simpler objects, also great for mixed arrays:

```
let city = dataComponents.filter(function( obj ) {
```

if (obj.types[0] == 'locality') {
return obj.short_name;
}

```
});
```

```
eval(metaData.filter(function( obj ) { if (obj.metaName == 'latitude') { return obj } } ))[0]['metaValue'];
```

#department/development/codesnippets