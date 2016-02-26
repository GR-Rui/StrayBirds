---
layout: post
title: React Native Learning (一)
category: React Native
comments: true
---

## get started

*This guide assumes OS X you have and Homebrew installed. We recommend periodically running brew update && brew upgrade to keep your programs up-to-date.*

1.  Install nvm, with nvm you can install multiple versions of Node.js and easily switch between them.
	
	Start by :
	
	```
	brew update
	brew install nvm
	mkdir ~/.nvm
	nano ~/.bash_profile
	````
	In your `.bash_profile` file (you may be using an other file, according to your shell), add the following:
	
	```
	export NVM_DIR=~/.nvm
	source $(brew --prefix nvm)/nvm.sh
	```
	Back to your shell, activate nvm and check it (if you have other shells opened and you want to keep them, do the same) :
	
	```
	source ~/.bash_profile
	echo $NVM_DIR
	```
	
2.  Install Node.js 4.0 or newer

	```
	nvm install node && nvm alias default node
	```
	
3.  `brew install watchman`. We recommend installing watchman, otherwise you might hit a node file watching bug

	```
	nvm install node && nvm alias default node
	```
4.  `brew install flow`, if you want to use flow.


## Initialized App

```
$ npm install -g react-native-cli
$ react-native init AwesomeProject
```

To run the iOS app:

* $ cd AwesomeProject
* Open ios/AwesomeProject.xcodeproj and hit run in Xcode.
* Open index.ios.js in your text editor of choice and edit some lines.
* Hit ⌘-R in your iOS simulator to reload the app and see your change!

	Or else:

* cd AwesomeProject
* react-native run-ios

To run your app on Android:
   
   * Have an Android emulator running (quickest way to get started), or a device connected
   * cd AwesomeProject
   * react-native run-android


*   Abacus
    * answer
*   Bubbles
    1.  bunk
    2.  bupkis
        * BELITTLER
        * dcddd
    3. burper
*   Cunning

