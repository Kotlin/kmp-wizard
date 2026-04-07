# Kotlin Multiplatform Wizard Template

This repository contains Kotlin Multiplatform template projects updated to AGP 9 and using the new multiplatform
project structure we'll be introducing soon.

## Why this exists

This is provided to address the delay in AGP 9 support for IntelliJ IDEA. While that work is ongoing, you can use these
updated starter templates in Android Studio.

The KMP wizard on [https://kmp.new](https://kmp.new) and in the IDEs will continue to generate projects with AGP 8 and
the old structure for now. This way, those projects will continue in both IntelliJ IDEA and Android Studio.

Once IntelliJ IDEA support for AGP 9 is shipped, we'll update the KMP wizard everywhere. 

## How to use

Use this repository as a template for your own project. It contains branches with the following configurations:

| Branch Name                                                                            | Project Configuration                              |
|----------------------------------------------------------------------------------------|----------------------------------------------------|
| [mobile-shared](https://github.com/Kotlin/kmp-wizard/tree/mobile-shared)               | Android + iOS (CMP)                                |
| [mobile-native](https://github.com/Kotlin/kmp-wizard/tree/mobile-native)               | Android + iOS (SwiftUI)                            |
| [all-frontends-shared](https://github.com/Kotlin/kmp-wizard/tree/all-frontends-shared) | Android + iOS (CMP) + Desktop + Web (CMP)          |
| [all-frontends-native](https://github.com/Kotlin/kmp-wizard/tree/all-frontends-native) | Android + iOS (SwiftUI) + Desktop + Web (React)    |
| [all-targets](https://github.com/Kotlin/kmp-wizard/tree/all-targets)                   | Android + iOS (CMP) + Desktop + Web (CMP) + Server |

After using the template, you probably want to change the project name and package name,
since this repository contains the default values from the standard project generator.
Search for `org.example.project` and `KotlinProject` to reconfigure this manually if you need custom values.

## Project description

This is a Kotlin Multiplatform project targeting Android, iOS, Web, Desktop (JVM).

* [/iosApp](./iosApp/iosApp) contains iOS applications. Even if you’re sharing your UI with Compose Multiplatform,
  you need this entry point for your iOS app. This is also where you should add SwiftUI code for your project.

* [/shared](./shared/src) is for code that will be shared across your Compose Multiplatform applications.
  It contains several subfolders:
  - [commonMain](./shared/src/commonMain/kotlin) is for code that’s common for all targets.
  - Other folders are for Kotlin code that will be compiled for only the platform indicated in the folder name.
    For example, if you want to use Apple’s CoreCrypto for the iOS part of your Kotlin app,
    the [iosMain](./shared/src/iosMain/kotlin) folder would be the right place for such calls.
    Similarly, if you want to edit the Desktop (JVM) specific part, the [jvmMain](./shared/src/jvmMain/kotlin)
    folder is the appropriate location.

### Build and Run Android Application

To build and run the development version of the Android app, use the run configuration from the run widget
in your IDE’s toolbar or build it directly from the terminal:
- on macOS/Linux
  ```shell
  ./gradlew :androidApp:assembleDebug
  ```
- on Windows
  ```shell
  .\gradlew.bat :androidApp:assembleDebug
  ```

### Build and Run Desktop (JVM) Application

To build and run the development version of the desktop app, use the run configuration from the run widget
in your IDE’s toolbar or run it directly from the terminal:
- on macOS/Linux
  ```shell
  ./gradlew :desktopApp:run
  ```
- on Windows
  ```shell
  .\gradlew.bat :desktopApp:run
  ```

To launch the desktop app in 'hot reload mode', use the run configuration from the run widget
in your IDE’s toolbar or run it directly from the terminal:
- on macOS/Linux
  ```shell
  ./gradlew :desktopApp:hotRun --auto
  ```
- on Windows
  ```shell
  .\gradlew.bat :desktopApp:hotRun --auto
  ```

### Build and Run Web Application

To build and run the development version of the web app, use the run configuration from the run widget
in your IDE's toolbar or run it directly from the terminal:
- for the Wasm target (faster, modern browsers):
  - on macOS/Linux
    ```shell
    ./gradlew :webApp:wasmJsBrowserDevelopmentRun
    ```
  - on Windows
    ```shell
    .\gradlew.bat :webApp:wasmJsBrowserDevelopmentRun
    ```
- for the JS target (slower, supports older browsers):
  - on macOS/Linux
    ```shell
    ./gradlew :webApp:jsBrowserDevelopmentRun
    ```
  - on Windows
    ```shell
    .\gradlew.bat :webApp:jsBrowserDevelopmentRun
    ```

### Build and Run iOS Application

To build and run the development version of the iOS app, use the run configuration from the run widget
in your IDE’s toolbar or open the [/iosApp](./iosApp) directory in Xcode and run it from there.

---

Learn more about [Kotlin Multiplatform](https://www.jetbrains.com/help/kotlin-multiplatform-dev/get-started.html),
[Compose Multiplatform](https://github.com/JetBrains/compose-multiplatform/#compose-multiplatform),
[Kotlin/Wasm](https://kotl.in/wasm/)…

We would appreciate your feedback on Compose/Web and Kotlin/Wasm in the public Slack channel [#compose-web](https://slack-chats.kotlinlang.org/c/compose-web).
If you face any issues, please report them on [YouTrack](https://youtrack.jetbrains.com/newIssue?project=CMP).