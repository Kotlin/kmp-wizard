# Kotlin Multiplatform Wizard Template

## Why this exists

To address the delay in AGP 9 support for IJ, we want to roll out the new project structure in the wizard as a
standalone
GitHub repo, so that Android Studio users can start using it. At the same time, the standard project generator
at [https://kmp.new](https://kmp.new)
continues to generate projects with the old structure and AGP 8, which is supported in IntelliJ and Android Studio.

## How to use

Use this repo as a template for your own project. It contains the branches with the following configurations:

| Branch Name          | Project Configuration                              |
|----------------------|----------------------------------------------------|
| mobile-shared        | Android + iOS (CMP)                                |
| mobile-native        | Android + iOS (SwiftUI)                            |
| all-frontends-shared | Android + iOS (CMP) + Desktop + Web (CMP)          |
| all-frontends-native | Android + iOS (SwiftUI) + Desktop + Web (React)    |
| all-targets          | Android + iOS (CMP) + Desktop + Web (CMP) + Server |

After using the template, you probably want to change the project name and package name,
since this repository contains the default values from the standard project generator.
Search for `org.example.project` and `KotlinProject` to reconfigure this manually if you need custom values.