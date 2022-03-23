# compose-state-codelab

# Using State in Jetpack Compose Codelab

This folder contains the source code for the [Using State in Jetpack Compose codelab](https://developer.android.com/codelabs/jetpack-compose-state).


In this codelab, you will explore patterns for working with state in a declarative world by building a Todo application. We'll see what unidirectional
data flow is, and how to apply it in a Jetpack Compose application to build stateless and stateful composables.

## Screenshots

![Finished code](screenshots/state_movie.gif "After: Animation of fully completed project")

## License

```
Copyright 2020 The Android Open Source Project

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    https://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```


https://developer.android.com/codelabs/jetpack-compose-state?continue=https%3A%2F%2Fdeveloper.android.com%2Fcourses%2Fpathways%2Fcompose%23codelab-https%3A%2F%2Fdeveloper.android.com%2Fcodelabs%2Fjetpack-compose-state#0

## [1\. Introduction](#0)

In this codelab you'll learn about state and how it can be used and manipulated by Jetpack Compose.

Before we dive in, it's useful to define what exactly _state_ is. At its core, state in an application is any value that can change over time. This is a very broad definition, and encompases everything from a [Room](https://developer.android.com/topic/libraries/architecture/room?gclid=Cj0KCQjwhIP6BRCMARIsALu9LfmJc9vMtMHKOtFlbE9kyzwZCYZsz89FYyEfpeyOLR2jvVMCKaFAkd8aAqgoEALw_wcB&gclsrc=aw.ds) database to a variable on a class.

**State** in an application is **any value that can change** over time.

For example it may be a value stored in a Room database, a variable on a class, or even the current value read from an accelerometer.

All Android applications display state to the user. A few examples of state in Android applications:

1.  A Snackbar that shows when a network connection can't be established
2.  A blog post and associated comments
3.  Ripple animations on buttons that play when a user clicks
4.  Stickers that a user can draw on top of an image

In this codelab you will explore how to use and think about state when using Jetpack Compose. To do this, we will build a TODO application. At the end of this codelab you'll have built a stateful UI that displays an interactive, editable, TODO list.

![b5c4dc05d1e54d5a.png](/codelabs/jetpack-compose-state/img/b5c4dc05d1e54d5a.png)

In the next section you'll learn about Unidirectional Data Flow – a design pattern that is core to understanding how to display and manage state when using Compose.

## **What you'll learn**

*   What is unidirectional data flow
*   How to think about state and events in a UI
*   How to use Architecture Component's `ViewModel` and `LiveData` in Compose to manage state
*   How Compose uses state to draw a screen
*   When to move state to a caller
*   How to use internal state in Compose
*   How to use `State<T>` to integrate state with Compose

## What you'll need

*   [Android Studio Bumblebee](https://developer.android.com/studio)
*   Knowledge of Kotlin
*   Consider taking the [Jetpack Compose basics codelab](https://codelabs.developers.google.com/codelabs/jetpack-compose-basics/) before this codelab
*   Basic understanding of Compose (such as the `@Composable` annotation)
*   Basic familiarity with Compose layouts (e.g. Row and Column)
*   Basic familiarity with modifiers (e.g. Modifier.padding)
*   Basic understanding of Architecture Component's [`ViewModel`](https://developer.android.com/topic/libraries/architecture/viewmodel?gclid=Cj0KCQjwhIP6BRCMARIsALu9LfmXmU5iTaUvGwPlXUzuDdM7owMPHyLrMGN1JXavO8rxamW7vWvKthoaAuvtEALw_wcB&gclsrc=aw.ds) and [`LiveData`](https://developer.android.com/topic/libraries/architecture/livedata)

## **What you'll build**

*   An interactive TODO app using unidirectional data flow in compose
