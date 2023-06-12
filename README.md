# mopinion-sdk-android-web
The Mopinion Native Android SDK web version has been developed 100% in native Kotlin, powerful tool to collect users feedback from an Android App based on events on a webview.

## <a name="release_notes">Release notes for version 1.0.0-beta</a>
First beta version of this SDK.

## <a name="install">Installation</a>
- Install the Mopinion Native Android SDK Web Library by following the next steps.
- Download our [Mopinion Forms](https://play.google.com/store/apps/details?id=com.mopinion.mopinion) app from the Google Play Store to preview what your mobile forms will look like in your app.
  
### Step 1:

Add the JitPack repository to your `build.gradle` root file. Add it at the end of repositories:

```
allprojects {
		repositories {
		    ...
			maven { url 'https://jitpack.io' }
		}
	}
```

In newer versions of Android Studio this repository will have to be set in `settings.gradle` file of
the project as the following:

```
dependencyResolutionManagement {
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
    repositories {
        google()
        mavenCentral()
        maven {
            ...
            url 'https://www.jitpack.io'
        }
    }
}
```

### Step 2:

Install the Mopinion Android SDK Web Library by adding it to the `build.gradle` module level of
your project. The minimal required Android API is 21.

```groovy
dependencies {
    implementation 'com.mopinion:sdk-android-web:1.0.0-beta'
}
```

### Step 3:

The library needs to communicate with Mopinion Servers, please make sure you have the Internet
permission in your `AndroidManifest.xml`:

```
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.app">
    
		<uses-permission android:name="android.permission.INTERNET" />
		
		<application
		...
```