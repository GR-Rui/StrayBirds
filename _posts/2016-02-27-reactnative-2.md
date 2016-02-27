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

![android-package-1](http://gr-rui.github.io/blog/images/docs/android-package-1.png)

*Note: Android SDK Build-tools version number must match with gradle build script*

![android-package-2](http://gr-rui.github.io/blog/images/docs/android-package-2.png)

![android-package-3](http://gr-rui.github.io/blog/images/docs/android-package-3.png)

*Note: "Android Support Repository" in Extras has now been renamed to "Local Maven repository for Support Libraries", require installed, otherwise, got the following errors: *

```
 A problem occurred configuring project ':app'.
 Could not resolve all dependencies for configuration ':app:_debugCompile'.
 Could not find com.android.support:appcompat-v7:23.0.1.
 Searched in the following locations:
```

### Create a stock Google emulator 

1. Start a new shell and run `android`; in the window that appears make sure you check:
    * Intel x86 Atom System Image (for Android 6.0.1 - API 23)
    * Intel x86 Emulator Accelerator (HAXM installer)
2. Click "Install Packages".
3. Configure hardware acceleration (HAXM), otherwise the emulator is going to be slow.
4. Create an Android Virtual Device (AVD):
   1. Run android avd and click on Create... 
   2. With the new AVD selected, click Start...
   ![android-avd](http://gr-rui.github.io/blog/images/docs/android-avd.png)
5. To bring up the developer menu press F2 

*Note: It must click android avd start first, then run `react-native run-android`*




