# keyboards (recat antive)
[https://medium.freecodecamp.com/how-to-make-your-react-native-app-respond-gracefully-when-the-keyboard-pops-up-7442c1535580#.hge4l5qrp](https://medium.freecodecamp.com/how-to-make-your-react-native-app-respond-gracefully-when-the-keyboard-pops-up-7442c1535580#.hge4l5qrp)

Good to push fields out of way, not so good for most forms - not needed either. a scrollview or an auto-focusing view is better. <KeyboardAvoidingView behavior="position" keyboardVerticalOffset={-135} contentContainerStyle={[styles.formStep, { height: (height - 135) }]}>

done and arrow buttons not native, implementable from scratch.

KeyboardAwareScrollView is good except the Auto Scroll. Auto Scroll would be good if a fork were made that disabled positive Y values. The top input need not scroll to the middle when in focus, only inputs underneath the keyboard not to scroll into view via a negative Y. Besides that, it’s nice.

The native Keyboard module is good for getting good animations and the like.

[https://www.npmjs.com/package/react-native-keyboard-manager](https://www.npmjs.com/package/react-native-keyboard-manager)

#department/development/codesnippets
#department/development/react-native