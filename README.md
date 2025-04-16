![](/readme-media/graphic.png)

# 🍲 FoodStore (Kotlin Multiplatform Mobile)

FoodSore is a lightweight demo app crafted to showcase how to build cross-platform mobile applications using Kotlin Multiplatform Mobile (KMM) with a shared Jetpack Compose UI for both Android and iOS 🚀.



## About 

This application retrieves a list of posts from a remote API, syncs the data with local storage using SQLite, and always displays data from the local source. The app ensures data is available even when offline.

**Features:**

- [x] Offline capability 📵
- [x] Dark mode 🌓
- [x] Clean and Simple Material UI 🎨

The network API is a dummy (fixed) response which is _statically hosted
[here](https://patilshreyas.github.io/DummyFoodiumApi/api/posts/)_. The concept of this app is
originally taken from [this project](https://github.com/PatilShreyas/Foodium/).

### 📱 Preview

Currently, the app looks like this on the both platforms:

#### ▶️ Android

https://user-images.githubusercontent.com/19620536/235439485-b2d0e7c9-e7fd-4313-adbc-aa259aaed6ec.mp4

#### ▶️ iOS

https://user-images.githubusercontent.com/19620536/235439532-457f0ccf-d18f-467d-a3c8-8b2fc45d6e01.mp4

---

## Built with 

- [Kotlin](kotlinlang.org): Programming language
- [Kotlin Multiplatform](https://kotlinlang.org/docs/multiplatform.html): For building multi-platform applications in the single codebase.
- [Jetpack/JetBrains Compose Multiplatform](https://www.jetbrains.com/lp/compose-multiplatform/): For a shared UI between multi-platforms i.e. Android and iOS in this project.
- Kotlinx
  - [Coroutines](https://github.com/Kotlin/kotlinx.coroutines): For multithreading
  - [Serialization](https://github.com/Kotlin/kotlinx.serialization): For JSON serialization/deserailization
- [Ktor Client](https://github.com/ktorio/ktor): Performing HTTP requests, Creating image loading utility for iOS module.
- [SQLDelight](https://github.com/cashapp/sqldelight): For persisting posts data in the local database
- [Coil](https://github.com/coil-kt/coil): Image loading for Android

  
## Project structure 

This Compose Multiplatform project includes three modules:

### [`shared`](/shared)
This is a Kotlin module that contains the logic common for both Android and iOS applications, the code you share between platforms.
This shared module is also where you write your Compose Multiplatform code. In `shared/src/commonMain/kotlin/App.kt`, you can find the shared root `@Composable` function for your app.
It uses Gradle as the build system. You can add dependencies and change settings in `shared/build.gradle.kts`. The shared module builds into an Android library and an iOS framework.

### [`androidApp`](/androidApp)
This is a Kotlin module that builds into an Android application. It uses Gradle as the build system. The `androidApp` module depends on and uses the shared module as a regular Android library.

### [`iosApp`](/iosApp)
This is an Xcode project that builds into an iOS application. It depends on and uses the shared module as a CocoaPods dependency.

---

## Contribute

If you want to contribute to this library, you're always welcome!
See [Contributing Guidelines](CONTRIBUTING.md).

## Discuss 💬

Have any questions, doubts or want to present your opinions, views? You're always welcome.
You can [start discussions](https://github.com/PatilShreyas/Foodium-KMM/discussions).



```
Copyright 2023 Shreyas Patil

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
