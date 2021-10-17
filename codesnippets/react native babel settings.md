# react native babel settings
reset the packager cache node_modules_react-native_packager/packager.sh --reset-cache

"presets": [
"react-native",
"es2015",
"es2016",
"es2017",
"stage-0"
],

"plugins": [
"transform-decorators-legacy",
"transform-do-expressions",
"transform-function-bind",
"transform-class-constructor-call",
"transform-export-extensions",
"syntax-trailing-function-commas",
"transform-exponentiation-operator",
"transform-async-to-generator"
]

 perfect for react native on apple tv, likely anywhere native + es6
"presets": ["react-native-stage-0/decorator-support"]

#department/development/codesnippets
#department/development/react-native