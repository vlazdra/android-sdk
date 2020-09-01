[![](https://jitpack.io/v/vlazdra/triton-android-sdk.svg)](https://jitpack.io/#vlazdra/triton-android-sdk) [![](https://circleci.com/gh/vlazdra/triton-android-sdk.svg?style=shield&logo=appveyor)](<LINK>)

# About this fork

This fork is maintained separately from Triton Digital. We will do our best to integrate any change
that Triton introduces into their original repository. We will also maintain our own version
system in order not to mix up things with the original repository, the changelog can be found in the releases of the [GitHub release page](https://github.com/vlazdra/triton-android-sdk/releases)

# Integrating this fork

In order to integrate this repo in your project, you can use a gradle dependency as described bellow. First thing that you need to add is the JitPack Maven repository in your **project root _build.gradle_** file:

``` gradle
allprojects {
    repositories {
        google()
        jcenter()
        mavenCentral()
        maven { url 'https://jitpack.io' } // Add this line as the last option
    }
}
```

And in your app level _build.gradle_ please add:

``` gradle
dependencies {
    implementation 'com.github.vlazdra:triton-android-sdk:1.0.0'
}
```

For the latest version of the SDK you can see check the [GitHub release page](https://github.com/vlazdra/triton-android-sdk/releases), or the JitPack badge up top.

# Integrating bleeding edge

Since we are using JitPack to distribute, JitPack offers a functionality that might be beneficial
to interested parties, and that is integration the bleeding edge code in your project. In order to integrate the most latest code from the master branch for example you will need to change the dependency implementation line like shown bellow:

``` gradle
dependencies {
    implementation 'com.github.vlazdra:triton-android-sdk:master-SNAPSHOT'
}
```

**Note: Using the latest code from the master branch is not recommended to be used in production.**

---

# Triton Digital® Mobile SDK for Android

The Triton Digital® Mobile SDK is designed to help you play your radio station or display on-demand advertisements very easily in your own application. There are two (2) versions of the mobile SDK; one for Android and one for iOS. This is the Android version.

The Triton Digital® Mobile SDK includes a [ZIP file](https://github.com/tritondigital/android-sdk/releases) that contains the API reference and a sample application that is ready to compile showing the most common uses of the SDK.

The Triton Digital® Mobile SDK adds about 330 kb to the size of your Android mobile application. This may vary with updates, and according to the parameters that you use.

The main features of the SDK include:

- Play Triton Digital® streams (including HLS mounts);
- Receive meta-data synchronized with the streams;
- Receive Now Playing History information; and
- Advertising:
  - Sync banners
  - On-demand audio and video interstitial ads
  - Support for VAST and DAAST formats

For complete documentation on using the Triton Digital® Mobile SDK for Android, visit our [online documentation](https://userguides.tritondigital.com/spc/moband/).

## Getting Started

The following instructions will get a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

- [Android Studio](https://developer.android.com/studio/)
- [Java OpenJDK](https://openjdk.java.net/)

### Installing

Install Android Studio (and an emulator if you want to use that instead of a physical phone).

Fork and clone the Triton Digital® Mobile SDK for Android project on GitHub

## Running the tests

In your terminal, navigate to where you forked or cloned the SDK:

``` bash
./gradlew test
./gradlew connectedAndroidTest
```

## Built the SDK

In order to build the SDK, you will need to run the following command via the terminal in the
root of the project:

``` bash
./gradlew sdk
```

Based on the `build.gradle` in the root of the project, that specific task depends on the `buildSdk`
task so the copy task will call the build task and build the project and prepare the `aar` file.

Once the gradle tasks finishes, you will have to navigate to `[project_root]/generated/libs`,
inside that folder you will find the build aar file with the corresponding version.

## Contributing

If you wish to contribute to this project, please see the [CONTRIBUTING.md](CONTRIBUTING.md) file for details.

## Versioning

We use an internal versioning system. All accepted contributions will be versioned under this versioning scheme.

For specifying the version manually you can go into the `gradle.properties` and change the major/minor/patch. The build system will use those values to generate all the required files.

## License

This project is licensed under the Apache 2.0 License - see the [LICENSE.md](LICENSE.md) file for details.
