# Kotlin Multiplatform Wizard Template

This repository contains Kotlin Multiplatform template projects updated to AGP 9 and using the new multiplatform
project structure we'll be introducing soon.

## Why this exists

This is provided to address the delay in AGP 9 support for IntelliJ IDEA. While that work is ongoing, you can use these
updated starter templates in Android Studio.

The KMP wizard on [https://kmp.new](https://kmp.new) and in the IDEs will continue to generate projects with AGP 8 and
the old structure for now. This way, those projects will continue in both IntelliJ IDEA and Android Studio.

Once IntelliJ IDEA support for AGP 9 is shipped, we'll update the KMP wizard everywhere and archive this repository. 

## How to use

Use this repository as a template for your own project. It contains branches with the following configurations:

| Branch Name             | Project Configuration                              |
|-------------------------|----------------------------------------------------|
| [mobile-shared]         | Android + iOS (CMP)                                |
| [mobile-native]         | Android + iOS (SwiftUI)                            |
| [all-frontends-shared]  | Android + iOS (CMP) + Desktop + Web (CMP)          |
| [all-frontends-native]  | Android + iOS (SwiftUI) + Desktop + Web (React)    |
| [all-targets]           | Android + iOS (CMP) + Desktop + Web (CMP) + Server |

After using the template, you probably want to change the project name and package name,
since this repository contains the default values from the standard project generator.
Search for `org.example.project` and `KotlinProject` to reconfigure this manually if you need custom values.

[mobile-shared]: https://github.com/Kotlin/kmp-wizard/tree/mobile-shared
[mobile-native]: https://github.com/Kotlin/kmp-wizard/tree/mobile-native
[all-frontends-shared]: https://github.com/Kotlin/kmp-wizard/tree/all-frontends-shared
[all-frontends-native]: https://github.com/Kotlin/kmp-wizard/tree/all-frontends-native
[all-targets]: https://github.com/Kotlin/kmp-wizard/tree/all-targets
