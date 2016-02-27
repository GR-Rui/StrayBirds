---
layout: post
title: React Native Learning - Android Setup (二)
category: React Native
comments: true
---

## Android Setup

### Install Git

On Mac, if you have installed XCode, Git is already installed, otherwise run the following:

```
brew install git 
```
### Install the Android SDK (unless you have it) 

1. Install the latest JDK
2. Install the Android SDK:

    On Mac:  `brew install android-sdk`
    
### Define the ANDROID_HOME environment variable 

On Mac, add this to your `~/.bashrc`, `~/.bash_profile` or whatever your shell uses:

```
# If you installed the SDK via Homebrew, otherwise ~/Library/Android/sdk
export ANDROID_HOME=/usr/local/opt/android-sdk
```
*NOTE: You need to restart the Command Prompt (Windows) / Terminal Emulator (Mac OS X, Linux) to apply the new Environment variables.*

### Use gradle daemon

For Mac users, you can use Homebrew to install the latest package:

```
$ brew install gradle
```

On UNIX-like operating systems, the following Bash shell command will enable the Daemon for the current user:

```
touch ~/.gradle/gradle.properties && echo "org.gradle.daemon=true" >> ~/.gradle/gradle.properties
```
Once the Daemon is enabled for a build environment in this way, all builds will implicitly use a Daemon.

*The --daemon and --no-daemon command line switches enable and disable usage of the Daemon for individual build invocations when using the Gradle command line interface. Typically, it is more convenient to enable the Daemon for an environment (e.g. a user account) so that all builds use the Daemon without requiring to remember to supply the --daemon switch.*

### Configure your SDK

Open the Android SDK Manager (on Mac start a new shell and run android); 

```
$ android
```

in the window that appears make sure you check:

    * Android SDK Build-tools version 23.0.1
    * Android 6.0 (API 23)
    * Android Support Repository
    
Click "Install Packages"

![image 1](http://gr-rui.github.io/blog/images/docs/android-package-1.png)

*Note: Android SDK Build-tools version number must match with gradle build script*

![image 1](http://gr-rui.github.io/blog/images/docs/android-package-2.png)

![image 1](http://gr-rui.github.io/blog/images/docs/android-package-3.png)




