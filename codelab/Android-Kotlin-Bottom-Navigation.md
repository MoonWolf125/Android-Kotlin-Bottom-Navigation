summary: Android in Kotlin: Bottom Navigation
id: Android-Kotlin-Bottom-Navigation
categories: Android
tags: Android
status: Draft
authors: Kyle Dahn
Feedback Link: https://github.com/MoonWolf125/Codelabs

# Android in Kotlin: Bottom Navigation

<!-- ------------------------ -->
## Welcome 
Duration: 5

This codelab is part of the Android in Kotlin series! This series covers the most common features,
implementations, and best practices of Android using the Kotlin programming language. The codelabs
in this series are listed on the [Android in Kotlin series welcome page](../Android-Kotlin-Series-Welcome/index.html?index=..%2F..index).

### Introduction
Welcome to the Android in Kotlin lesson on Bottom Navigation!

Bottom Navigation is one of the most common implementations that allows users to move between
primary destinations. The `BottomNavigationView` displays a single bar at the bottom of the screen
that displays three to five destinations.

For each destination there is a corresponding icon and optional text that are displayed together in
the `BottomNavigationView`. When a destination's icon is selected the user is navigated to that
destination. It is recommended that a destination **always** have an icon, display a label; should
space allow, and that labels be short and meaningful while avoiding any text wrapping.

These icons and labels can be in one of two states, selected and unselected. When an item is selected
it's said to be "active," corresponding to the actively displayed destination whereas an unselected
item is said to be "inactive." Active items are highlighted to distinguish that they are the selected
item and the corresponding destination is shown. Inactive items are semi-opaque to distinguish
themselves from the active item.

Bottom Navigation is preferred because of it's proximity to the user's thumb, consistency between
selectable destinations, and clear icons and labels. 

positive
: **Note:**
- Bottom Navigation should be utilized for destinations that need to be accessible from anywhere in
the app, when there are three to five destinations, and only on mobile platforms.

negative
: **Note:**
- Bottom Navigation should **not** be used utilized when there are less than three destinations
or more than five. When there are less than three destinations, use tabs instead. When there are more
than five destinations, use scrolling tabs or a Navigation Drawer.
- Only **one** item should be active at a time since only one destination should be
shown on a screen at a time.

### What you should know
- The Kotlin programming language
- How to use Android Studio

### What you’ll learn 
- How to create a menu for Navigation 
- How to add a `BottomNavigationView`
- How to set an `OnNavigationItemSelectedListener`
- How to navigate to the Home Fragment using the Listener

<!-- ------------------------ -->
## Getting Started 
Duration: 8

### What you'll need
- [Android Studio](https://developer.android.com/studio)
- A Virtual or Physical Device (connected via USB)

### Get the Code
Clone the navigation codelab from GitHub:

```
git clone https://github.com/MoonWolf125/Android-Kotlin-Bottom-Navigation.git
```

Alternatively you can download the repository as a Zip file:

[Download Zip](https://github.com/MoonWolf125/Android-Kotlin-Bottom-Navigation/archive/0c8042c55a2702ae00b04a23477db1ec315c13a2.zip) 

#### Frequently Asked Questions
- [How do I install Android Studio?](https://developer.android.com/studio/)
- [How do I create a Virtual Device?](https://developer.android.com/studio/run/managing-avds)
- [How do I set up a device for development?](http://developer.android.com/tools/device.html)
- [How do I use Android Studio's Version Control Integration?](../Android-Studio-Version-Control-Basics/index.html?index=..%2F..index)

<!-- ------------------------ -->
## Code Overview
Duration: 2 