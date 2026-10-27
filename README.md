# Lab: Dessert Clicker Architecture

## 1. Before you begin

### Introduction

Dessert Clicker works with inline state and data. In this lab, you will remove the inline state, data, and logic out of the MainActivity and move it to a `ViewModel`.

Abstracting app logic away from the view and into a ViewModel is a modern practice for Android development. This practice offers the following benefits:

- The code becomes more readable for other developers.
- The code becomes more testable.
- Multiple developers can work simultaneously on an app without interfering with other developers' work.

### What you'll build

In these practice problems, you will improve the architecture of the Dessert Clicker app by adding a `ViewModel` to handle the data and app logic.

The practice problems are split into sections where you will complete the following steps individually:

- Update and add the necessary dependencies.
- Create a `ViewModel` class.

## 2. Set up dependencies
Add the following dependency to the `app/build.gradle.kts` file:

```kotlin
dependencies {
    ...
    implementation("androidx.lifecycle:lifecycle-viewmodel-compose:2.10.0")
}
```

## 3. Create a UI state class

Currently, the `DessertClickerApp()` composable in the `MainActivity` contains the data and state that drive the UI.

Create a data class that holds all the necessary data for the UI. The data within this class replaces the data that the `DessertClickerApp()` composable currently manages.

## 4. Create a ViewModel

Create a `ViewModel` class using the Jetpack ViewModel component. You use the ViewModel to manage the UI state.

## 5. Relocate the app logic and data to the ViewModel

Relocate the logic from the `MainActivity` to the ViewModel and make the UI state data accessible using the UI state class you created. Delete all the data and state management logic from `MainActivity`.

Try to approach this task on your own.

## 6. Call the ViewModel

Use the data and methods that the ViewModel provides to drive the UI in the `MainActivity`.

## 7. Build, Run, and Submit

**Verify your app:**

1. Click the **Run** button in Android Studio to build and launch the app on an emulator or physical device.
2. The app should look and function exactly as it did before. The core difference is that the architecture is now correctly separated.
3. Test the app by clicking the dessert and verify the score and dessert images update properly.
4. Rotate the device. Because you are now using a `ViewModel`, your score and state should survive the configuration change.

**Submission:**

1. Commit all your changes.
2. Push your commits to your GitHub repository.