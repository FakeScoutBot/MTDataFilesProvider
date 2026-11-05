# MTDataFilesProvider

[![](https://jitpack.io/v/L-JINBIN/MTDataFilesProvider.svg)](https://jitpack.io/#L-JINBIN/MTDataFilesProvider)

Quickly inject MT's file provider into your own app, so you can manage the app's private directory files on your phone without ROOT.

## Usage

### ① Add the jitpack.io repository

Add the jitpack.io address to the `settings.gradle` file in the project root directory:

```groovy
dependencyResolutionManagement {
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
    repositories {
        mavenCentral()
        maven { url 'https://jitpack.io' }
    }
}
```

Some projects may instead need it added in the `build.gradle` file in the root directory:

```groovy
allprojects {
    repositories {
        mavenCentral()
        maven { url 'https://jitpack.io' }
    }
}
```

### ② Add the MTDataFilesProvider dependency

Add the dependency in your module's `build.gradle`:

```groovy
dependencies {
    debugImplementation 'com.github.L-JINBIN:MTDataFilesProvider:v1.0.0'
}
```

Here, `debugImplementation` means MTDataFilesProvider is injected only in the debug build and is automatically removed when you compile the release build. If you want it injected in the release build as well, change it to `implementation`.

### ③ Add local storage in MT Manager

- Download and install [MT Manager](https://mt2.cn/download/)
- On the main screen, open the side drawer and tap the "Add local storage" menu in the top-right corner
- In the screen that pops up, find and select your app in the side drawer, then tap "Select" at the bottom
- Return to MT Manager and you will see the local storage you just added; tap it to access

For detailed steps, see [MT Manager - Inject a Documents Provider](https://mt2.cn/guide/reverse/inject-documents-provider.html#%E6%B7%BB%E5%8A%A0%E6%9C%AC%E5%9C%B0%E5%AD%98%E5%82%A8)
